
# Slurm

## Slurm Architecture Diagram

```plaintext
        +-----------------------+
        |   Slurm Controller     |
        |   (slurmctld)          |
        |   +-----------------+  |
        |   | Munge Key       |  |
        |   +-----------------+  |
        |   | Slurm DB Daemon |  |
        |   | (slurmdbd)      |  |
        |   +-----------------+  |
        |   | Slurm Daemon    |  |
        |   | (slurmd)        |  |
        |   +-----------------+  |
        +-----------------------+
                |
                | Munge Key
                |
         +---------------------+
         |   Compute Node      |
         |   (slurmd)          |
         |   +------------+    |
         |   | Munge Key  |    |
         |   +------------+    |
         +---------------------+
```
## Slurm Architecture Overview

## Controller (slurmctld)
- Manages job scheduling and resource allocation.
- Connects to Slurm DB Daemon (slurmdbd) for job accounting.
- Contains the Munge key for authentication with compute nodes.
- Runs Slurmd for local job execution (optional).

## Slurm DB Daemon (slurmdbd)
- Stores job accounting data in a database.

## Slurm Daemon (slurmd)
- Runs on both controller (for local jobs) and compute nodes (for worker node jobs).
- Coordinates job execution and resource management.

## Munge Key
- Used for secure authentication between the controller and compute nodes.

# Slurm Communication Setup

## 1. Change Hostname

### On Controller or Compute Node:
1. **Edit `/etc/hostname`** and set the new hostname.
   ```bash
   sudo nano /etc/hostname
   ```
   
2. **Edit `/etc/hosts`** to add/update hostname-IP mappings:
   ```bash
   sudo nano /etc/hosts
   ```
   Example:
   ```bash
   192.168.1.100    controller
   192.168.1.101    compute-node-01
   ```

3. **Restart Networking** or reboot:
   ```bash
   sudo systemctl restart networking
   ```

## 2. Secure Copy (SCP) Files

### Copy files from Controller to Compute Node:
```bash
scp /etc/slurm/slurm.conf user@compute-node-01:/etc/slurm/
```

### Copy files from Compute Node to Controller:
```bash
scp user@compute-node-01:/etc/slurm/slurm.conf /etc/slurm/
```

## 3. Restart Slurm Daemons
After copying files, restart Slurm services:
```bash
sudo systemctl restart slurmctld    # On controller
sudo systemctl restart slurmd      # On compute node
```

## imp Commands
- **`sinfo`**: Displays the status of Slurm nodes and partitions.
   - Example:  
     ```bash
     sinfo
     ```

- **`scontrol`**: Administrative tool for managing Slurm jobs, nodes, and other resources.
   - Example:  
     ```bash
     scontrol show job 12345
     ```

- **`squeue`**: Lists jobs in the queue with their current status.
   - Example:  
     ```bash
     squeue
     ```

- **`sacct`**: Provides accounting information for completed jobs.
   - Example:  
     ```bash
     sacct -j 12345
     ```

- **`scancel`**: Cancels a job or job array by job ID or other criteria.
   - Example:  
     ```bash
     scancel 12345
     ```

- **`saccountmgr`**: Manages Slurm user accounts and associations.
   - Example:  
     ```bash
     saccountmgr show accounts
     ```

- **`scontrol show job <id>`**: Displays detailed information about a specific job.
   - Example:  
     ```bash
     scontrol show job 12345
     ```

- **Difference between `sbatch` and `srun`**:
   - **`sbatch`**: Submits a batch job script to be executed later.  
     Example:  
     ```bash
     sbatch jobscript.sh
     ```
   - **`srun`**: Runs a job immediately, useful for interactive jobs.  
     Example:  
     ```bash
     srun --pty bash
     ```

## Important Paths in Slurm

- **Munge Key**  
  - **Path**: `/etc/munge/munge.key`  
  - **Description**: Used for secure authentication between Slurm components (controller and compute nodes).

- **Slurm Configuration File**  
  - **Path**: `/slurm/etc/slurm.conf` (or `/etc/slurm/slurm.conf`)  
  - **Description**: Main configuration file for Slurm, defining partitions, nodes, and job scheduling settings.


## Main Components of `slurm.conf` File

1. **ControlMachine**  
   - Defines the hostname of the Slurm controller node (typically `slurmctld`).
   - Example:  
     ```bash
     ControlMachine=controller
     ```

2. **SlurmdPort**  
   - Specifies the port on which Slurm daemons (`slurmd`) communicate.
   - Example:  
     ```bash
     SlurmdPort=7003
     ```

3. **SlurmctldPort**  
   - Specifies the port on which the Slurm controller (`slurmctld`) listens for connections.
   - Example:  
     ```bash
     SlurmctldPort=7002
     ```

4. **AuthType**  
   - Defines the authentication method used by Slurm (e.g., `auth/munge`).
   - Example:  
     ```bash
     AuthType=auth/munge
     ```

5. **MungeSocket**  
   - Defines the path to the Munge authentication socket.
   - Example:  
     ```bash
     MungeSocket=/var/run/munge/munge.socket.2
     ```

6. **ClusterName**  
   - Specifies the name of the Slurm cluster.
   - Example:  
     ```bash
     ClusterName=mycluster
     ```

7. **NodeName**  
   - Defines the compute nodes in the cluster, their CPU and memory configurations.
   - Example:  
     ```bash
     NodeName=compute[01-10] CPUs=8 RealMemory=32000 State=UNKNOWN
     ```

8. **PartitionName**  
   - Defines a partition, which is a set of nodes allocated for job execution.
   - Example:  
     ```bash
     PartitionName=normal Nodes=compute[01-10] Default=YES MaxTime=INFINITE State=UP
     ```

9. **SchedulerType**  
   - Defines the scheduling algorithm used by Slurm (e.g., `sched/backfill`).
   - Example:  
     ```bash
     SchedulerType=sched/backfill
     ```

10. **AccountingStorageType**  
    - Specifies the accounting storage method (e.g., `accounting_storage/slurmdbd` for using a database).
    - Example:  
      ```bash
      AccountingStorageType=accounting_storage/slurmdbd
      ```

### Example `slurm.conf` Snippet:
```bash
ControlMachine=controller
SlurmdPort=7003
SlurmctldPort=7002
AuthType=auth/munge
ClusterName=mycluster
NodeName=compute[01-10] CPUs=8 RealMemory=32000 State=UNKNOWN
PartitionName=normal Nodes=compute[01-10] Default=YES MaxTime=INFINITE State=UP
```


## sinfo wit parameter

### Display partition name
sinfo %p

### Display CPU count
sinfo %c

### Display node state
sinfo %d

### Display memory (in MB)
sinfo %m

### Display node feature/state
sinfo %s


# Slurm Troubleshooting Guide

## Logs to Check:
- **Controller Log** (`slurmctld.log`): Logs for the Slurm controller (`slurmctld`), which handles job scheduling and resource management.  
  Path: `/var/log/slurmctld.log`
  
- **Daemon Log** (`slurmd.log`): Logs for the Slurm daemon (`slurmd`) running on compute nodes.  
  Path: `/var/log/slurmd.log`

- **Database Log** (`slurmdbd.log`): Logs for the Slurm Database Daemon (`slurmdbd`), which handles job accounting and logs.  
  Path: `/var/log/slurmdbd.log`

---

# Slurm Troubleshooting Guide

## Log Files to Check:

1. **Controller Log (`slurmctld.log`)**  
   - **Path**: `/var/log/slurmctld.log`
   - **Use When**:  
     - You are troubleshooting the **Slurm controller**.
     - Errors related to job scheduling, controller communication, or overall cluster state.
     - Check for errors like job submission failures or partition issues.

2. **Daemon Log (`slurmd.log`)**  
   - **Path**: `/var/log/slurmd.log`
   - **Use When**:  
     - You are troubleshooting the **Slurm daemon** running on **compute nodes**.
     - Errors related to job execution on the compute nodes, such as node failures or job execution issues.
     - Issues with job dispatch, allocation, or node resource usage.

3. **Database Log (`slurmdbd.log`)**  
   - **Path**: `/var/log/slurmdbd.log`
   - **Use When**:  
     - You are troubleshooting **Slurm's accounting and database**.
     - Errors related to job accounting, job statistics, or database connectivity issues.

---

## Troubleshooting: Node Not Showing as Idle in `sinfo`

## Issue:
Node is not showing as **idle** in `sinfo` even though the service is running.

## Solution:

1. **Manually Set Node to Idle**:
   If the node is not idle, manually update its state to IDLE:
   ```bash
   scontrol update NodeName=compute1 State=IDLE
   ```

2. **Check Node State**:
   Verify the current state of the node with `sinfo`:
   ```bash
   sinfo -N
   ```

3. **Verify Slurm Daemon**:
   Ensure the `slurmd` service is running on the compute node:
   ```bash
   systemctl status slurmd   # Check status on compute node
   sudo systemctl restart slurmd   # Restart if needed
   ```

4. **Check for Node Issues**:
   If the node is in a **drained** or **down** state, investigate hardware or configuration issues.


## Common Errors and Solutions:

### 1. **Bit Error (Controller Can't Communicate with Compute Node)**  
   - **Symptoms**: If you encounter bit errors, it typically indicates a communication failure between the **controller (`slurmctld`)** and **compute nodes (`slurmd`)**.
   - **Action**:
     - **Check Munge Key**: Ensure the **Munge key** (`/etc/munge/munge.key`) is the same on both the controller and compute nodes.
     - **Check Firewall/Ports**: Make sure communication ports (default `7002` for `slurmctld` and `7003` for `slurmd`) are open and not blocked by firewalls.
     - **Restart Services**: Restart Slurm services if necessary:
       ```bash
       sudo systemctl restart slurmctld   # On controller
       sudo systemctl restart slurmd     # On compute nodes
       ```

### 2. **Node Not Idle (Node is Not in IDLE State)**  
   - **Symptoms**: If a node is not in the **IDLE** state (e.g., it’s stuck in **ALLOCATED** or **BUSY** state), Slurm cannot schedule jobs properly.
   - **Action**:
     - **Check Node State**: Use `sinfo` to check the node state:
       ```bash
       sinfo -N  # Check the state of nodes
       ```
     - **Manually Set Node to IDLE**: If a node is stuck, manually update the node state to **IDLE**:
       ```bash
       scontrol update NodeName=<node_name> State=IDLE
       ```
     - **Reload Environment**: Ensure proper environment setup by exporting and sourcing the bash configuration:
       ```bash
       export /etc/bash.bashrc
       source /etc/bash.bashrc
       ```

---

### Conclusion:
- **Controller Logs (`slurmctld.log`)**: Use for job scheduling and controller communication issues.
- **Daemon Logs (`slurmd.log`)**: Use for compute node issues like job execution or node resource failures.
- **Database Logs (`slurmdbd.log`)**: Use for job accounting and database-related issues.
- **Bit Errors**: Usually indicate a communication problem, check Munge and network ports.
- **Non-Idle Node**: Manually set node to IDLE or reset environment settings if needed.

## Quality of Service (QoS) in Slurm

**Quality of Service (QoS)** in Slurm allows administrators to manage job priorities, resource allocations, and time limits. It helps control how jobs are scheduled based on user, group, or other criteria.

## Key Features:
- **Job Prioritization**: Control job scheduling priority based on user or group.
- **Resource Limits**: Limit CPUs, memory, or other resources a job can use.
- **Time Limits**: Set maximum job run times to avoid indefinite execution.
- **Fair Share**: Ensures fair resource allocation over time.
- **Preemption**: High-priority jobs can preempt lower-priority ones.

## Example Configuration (`slurm.conf`):
```bash
QOS=highpriority
MaxCpuPerNode=32
MaxWallTime=02:00:00   # 2 hours

```

# Backfill and Fairshare in Slurm

## Backfill:
- **Definition**: A scheduling technique in Slurm that allows low-priority jobs to run on idle resources, without delaying higher-priority jobs.
- **How it works**: Backfill ensures that jobs with shorter run times or lower resource requirements are scheduled while waiting for higher-priority jobs to be allocated resources.
- **Benefit**: Maximizes resource utilization without delaying important jobs.

## Fairshare:
- **Definition**: A scheduling policy that ensures fair distribution of resources over time among users or groups.
- **How it works**: Fairshare adjusts job priority based on historical resource usage. Users or groups with less resource usage in the past are given higher priority for future jobs.
- **Benefit**: Prevents resource monopolization by a few users or groups, promoting equitable resource access.



