### Resource Management and Accounting: Theory for Session 1 Topics  

---

#### **1. Batch Systems**  
Batch systems are a method of processing jobs where tasks are grouped into batches and executed sequentially without user interaction during runtime.  

**Key Features:**  
- **Job Queues:** Jobs are submitted to a queue and processed based on priority or other scheduling criteria.  
- **Non-Interactive:** Once submitted, users cannot interact with the job.  
- **Efficient Utilization:** Maximizes resource utilization by running multiple jobs on available resources.  
- **Examples:** SLURM, PBS, LSF, and Torque.  

**Advantages:**  
- Effective for long-running, compute-intensive tasks.  
- Simplifies job management and accounting.  

**Disadvantages:**  
- Jobs must wait for resources to become available, leading to potential delays.  
- No real-time user feedback during execution.  

---

#### **2. Resource Manager**  
The resource manager is a critical component in HPC environments that handles resource allocation across a cluster or computing environment.  

**Responsibilities:**  
- **Resource Tracking:** Monitors available resources such as CPU, memory, and storage.  
- **Job Placement:** Allocates resources to jobs based on their requirements.  
- **Load Balancing:** Ensures balanced utilization of cluster resources.  
- **Enforcement:** Enforces policies like resource limits and priorities.  

**Examples of Resource Managers:**  
- **SLURM (Simple Linux Utility for Resource Management):** Widely used in HPC for scheduling and resource management.  
- **PBS (Portable Batch System):** Manages batch jobs in supercomputing environments.  
- **HTCondor:** Specialized for distributed computing environments.  

---

#### **3. Scheduler**  
Schedulers are responsible for deciding the order and timing of job execution based on predefined policies.  

**Functions:**  
- **Job Prioritization:** Determines which job to execute next based on priority, fairness, or deadlines.  
- **Dependency Management:** Manages dependencies between tasks or jobs.  
- **Optimization:** Minimizes wait times and maximizes throughput by optimizing resource usage.  

**Scheduling Policies:**  
- **First Come, First Served (FCFS):** Jobs are executed in the order of submission.  
- **Priority Scheduling:** Jobs with higher priorities are executed first.  
- **Fair Sharing:** Ensures fair resource distribution among users or groups.  
- **Backfilling:** Allows smaller jobs to fill gaps in resource availability to reduce idle time.  

**Examples of Schedulers:**  
- SLURM Scheduler (integrated with SLURM).  
- Maui Scheduler (often used with Torque).  
- Moab Workload Manager.  

---

### Summary  
1. **Batch Systems:** Manage and process groups of jobs sequentially without real-time interaction.  
2. **Resource Manager:** Allocates and monitors resources in a cluster, ensuring optimal utilization.  
3. **Scheduler:** Decides job execution order and timing based on policies to maximize efficiency and minimize delays.  




### Resource Management and Accounting  
### Session 2 & 3: Theory Notes  

---

#### **1. Submitting and Managing Jobs**  

Submitting and managing jobs in an HPC environment involves interacting with a **batch system** to queue, monitor, and manage tasks on a computing cluster.  

##### **Job Submission:**  
- **Batch System Command Line Tools:** Users typically submit jobs using commands provided by the batch system.  
  - Example:  
    - **SLURM:** Use `sbatch` to submit a job.  
    - **PBS:** Use `qsub` to submit a job.  
- **Job Queues:** When a job is submitted, it is placed in a queue and waits for the scheduler to allocate resources.  

##### **Job Management Commands:**  
- **View Queues:**  
  - SLURM: `squeue`  
  - PBS: `qstat`  
- **Cancel Jobs:**  
  - SLURM: `scancel <job_id>`  
  - PBS: `qdel <job_id>`  
- **Monitor Job Progress:**  
  - SLURM: `scontrol show job <job_id>`  
  - PBS: `qstat -f <job_id>`  

##### **Best Practices for Submitting Jobs:**  
- **Specify Resources:** Clearly define resource requirements (e.g., CPU, memory) to ensure efficient scheduling.  
  - Example (SLURM): `--cpus-per-task=4 --mem=4G`  
- **Optimize Job Dependencies:** Use job dependencies to ensure tasks execute in a specific order.  
  - Example: `--dependency=afterok:<job_id>`  
- **Interactive Jobs:** For debugging or testing, submit interactive jobs.  
  - Example (SLURM): `srun --pty bash`  

---

#### **2. Writing the Batch Script**  

A **batch script** is a shell script that specifies the commands and resource requirements for a job in the cluster.  

##### **Structure of a Batch Script:**  
A typical batch script contains:  
1. **Shebang Line:** Indicates the shell to interpret the script (e.g., `#!/bin/bash`).  
2. **Batch Directives:** Special comments used by the batch system to specify resource requirements and scheduling options.  
3. **Job Commands:** The actual commands to execute the job tasks.  

---

##### **Example 1: SLURM Batch Script**  
```bash
#!/bin/bash
#SBATCH --job-name=example_job         # Name of the job
#SBATCH --output=output_%j.txt         # Standard output log file
#SBATCH --error=error_%j.txt           # Standard error log file
#SBATCH --ntasks=1                     # Number of tasks
#SBATCH --cpus-per-task=4              # Number of CPUs per task
#SBATCH --mem=8G                       # Memory required
#SBATCH --time=01:00:00                # Maximum runtime (HH:MM:SS)
#SBATCH --partition=standard           # Partition/queue to submit to

# Job commands
echo "Starting job on $(hostname)"
module load python/3.8
python my_script.py
```


---

##### **Key Batch Script Components:**  
1. **Resource Allocation:**  
   - Specify the number of nodes, CPUs, memory, and time required.  
2. **Environment Setup:**  
   - Load necessary modules or set environment variables.  
3. **Execution Commands:**  
   - Specify the commands to run the application or script.  
4. **Output Management:**  
   - Redirect output and error logs to files for debugging.  

---

#### **Tips for Writing Batch Scripts:**  
- Test commands interactively before adding them to a batch script.  
- Use meaningful job names for easier management.  
- Include error handling and logging to debug issues efficiently.  
- Optimize resource requests to avoid wasting cluster resources.  

--- 

### Summary  
1. **Submitting Jobs:** Use commands like `sbatch` (SLURM) or `qsub` (PBS) to queue tasks and specify resources effectively.  
2. **Managing Jobs:** Monitor and manage jobs using commands like `squeue` (SLURM) or `qstat` (PBS).  
3. **Batch Scripts:** Write efficient scripts to automate resource requests and task execution, ensuring proper logging and error management.  

Prepare well by practicing writing and submitting scripts on your cluster environment!


In Sessions 4 and 5, we'll delve into the practical aspects of using Slurm, focusing on:

1. **Slurm Installation and Configuration**
2. **Submitting and Managing Jobs**
3. **Writing Batch Scripts**

### 1. Slurm Installation and Configuration

**Overview:**
Slurm (Simple Linux Utility for Resource Management) is an open-source workload manager designed for Linux clusters of all sizes. It handles job scheduling and resource allocation, ensuring efficient utilization of computational resources.

**Installation Steps:**

1. **Prerequisites:**
   - **Dependencies:** Ensure necessary libraries and tools are installed, such as `gcc`, `make`, and `munge` for authentication.
   - **User Accounts:** Create a `slurm` user on all nodes to manage Slurm processes.

2. **Download and Compile:**
   - Obtain the latest Slurm source code from the official website.
   - Extract the tarball and navigate to the directory.
   - Configure the build environment:
     ```bash
     ./configure --prefix=/usr/local/slurm --sysconfdir=/etc/slurm
     ```
   - Compile and install:
     ```bash
     make
     make install
     ```

3. **Configuration:**
   - Use the Slurm Configuration Tool to generate a `slurm.conf` file tailored to your cluster's specifications.
   - Distribute the `slurm.conf` file to `/etc/slurm/` on all nodes.
   - Ensure the `StateSaveLocation` directory exists and is writable by the `slurm` user:
     ```bash
     mkdir -p /var/spool/slurm
     chown slurm:slurm /var/spool/slurm
     ```

4. **Start Services:**
   - On the control node, start the Slurm controller:
     ```bash
     systemctl start slurmctld
     ```
   - On compute nodes, start the Slurm daemon:
     ```bash
     systemctl start slurmd
     ```
   - Enable services to start on boot:
     ```bash
     systemctl enable slurmctld
     systemctl enable slurmd
     ```

**References:**
- [Quick Start Administrator Guide - Slurm Workload Manager](https://slurm.schedmd.com/quickstart_admin.html)
- [Slurm Installation Tutorial - SchedMD](https://www.schedmd.com/slurm/installation-tutorial/)

### 2. Submitting and Managing Jobs

**Submitting Jobs:**
- **Batch Jobs:** Use the `sbatch` command to submit jobs defined in a batch script:
  ```bash
  sbatch my_job_script.sh
  ```
- **Interactive Jobs:** For interactive sessions, use `srun`:
  ```bash
  srun --pty /bin/bash
  ```

**Managing Jobs:**
- **View Job Queue:** Check the status of submitted jobs with `squeue`:
  ```bash
  squeue
  ```
- **Cancel a Job:** Remove a job from the queue using `scancel`:
  ```bash
  scancel <job_id>
  ```
- **Job Details:** Retrieve detailed information about a job with `scontrol`:
  ```bash
  scontrol show job <job_id>
  ```

**References:**
- [Submitting Jobs with Slurm - UAB Research Computing](https://docs.rc.uab.edu/cheaha/slurm/submitting_jobs/)
- [How to submit a job to Slurm - Batch Computing - JASMIN Help](https://help.jasmin.ac.uk/docs/batch-computing/how-to-submit-a-job/)

### 3. Writing Batch Scripts

**Structure of a Batch Script:**
A Slurm batch script is a shell script that includes Slurm directives and the commands to execute your job.

**Example Script:**
```bash
#!/bin/bash
#SBATCH --job-name=example_job
#SBATCH --output=output_%j.txt
#SBATCH --error=error_%j.txt
#SBATCH --ntasks=1
#SBATCH --cpus-per-task=4
#SBATCH --mem=8G
#SBATCH --time=01:00:00
#SBATCH --partition=standard

# Load necessary modules
module load python/3.8

# Execute your application
python my_script.py
```

**Key Directives:**
- `--job-name`: Sets the name of the job.
- `--output`: Specifies the file for standard output.
- `--error`: Specifies the file for standard error.
- `--ntasks`: Number of tasks to run.
- `--cpus-per-task`: CPUs allocated per task.
- `--mem`: Memory allocation.
- `--time`: Maximum runtime.
- `--partition`: Specifies the partition or queue.


 
 In Sessions 6 and 7, we'll explore advanced aspects of Slurm, focusing on:

1. **Managing Nodes**
2. **Setting Server Scheduling Policies**

### 1. Managing Nodes

**Overview:**
In Slurm, nodes represent individual compute resources within a cluster. Effective node management ensures optimal resource utilization and cluster performance.

**Key Node States:**

- **Idle:** The node is available for job allocation.
- **Allocated:** The node is currently assigned to one or more jobs.
- **Down:** The node is unavailable due to failure or maintenance.
- **Drained:** The node is intentionally set to prevent new job allocations, often for maintenance.

**Managing Node States:**

- **Viewing Node Status:**
  Use the `scontrol` command to display node information:
  ```bash
  scontrol show nodes
  ```

- **Setting a Node to Down:**
  To mark a node as down:
  ```bash
  scontrol update NodeName=<node_name> State=DOWN Reason="Maintenance"
  ```

- **Draining a Node:**
  To prevent new jobs from being scheduled on a node:
  ```bash
  scontrol update NodeName=<node_name> State=DRAIN Reason="Scheduled maintenance"
  ```
  Draining a node ensures that no new jobs are assigned, allowing current jobs to complete before maintenance. 

- **Resuming a Node:**
  To return a node to service:
  ```bash
  scontrol update NodeName=<node_name> State=RESUME
  ```

**Best Practices:**

- **Regular Monitoring:**
  Consistently check node statuses to identify and address issues promptly.

- **Automated Health Checks:**
  Implement tools like Node Health Check (NHC) to automatically detect and manage unhealthy nodes.

- **Documentation:**
  Maintain clear records of node maintenance activities, including reasons for draining or setting nodes down.

### 2. Setting Server Scheduling Policies

**Overview:**
Slurm's scheduling policies determine how jobs are prioritized and allocated resources within the cluster. Configuring these policies effectively balances workload and optimizes cluster utilization.

**Key Configuration Parameters:**

- **SchedulerType:**
  Defines the scheduling algorithm. Common options include `sched/backfill` for backfill scheduling.

- **PriorityType:**
  Determines how job priorities are calculated. Options include `priority/multifactor`, which considers multiple factors like job age, size, and user fairshare.

- **Scheduling Intervals:**
  - **sched_interval:**
    Sets the frequency of the main scheduling loop. A typical setting might be `sched_interval=30s`, meaning the scheduler runs every 30 seconds. 

**Setting Scheduling Policies:**

- **Configuring Priority Factors:**
  In the `slurm.conf` file, define weights for various factors influencing job priority:
  ```bash
  PriorityWeightAge=1000
  PriorityWeightFairshare=500
  PriorityWeightJobSize=200
  PriorityWeightPartition=100
  ```
  These weights adjust the influence of each factor on job prioritization.

- **Partition Configuration:**
  Partitions (analogous to queues) can have specific scheduling policies:
  ```bash
  PartitionName=short PriorityTier=10 MaxTime=01:00:00 State=UP
  PartitionName=long PriorityTier=5 MaxTime=48:00:00 State=UP
  ```
  Higher `PriorityTier` values indicate higher priority for job scheduling.

**Best Practices:**

- **Fairshare Configuration:**
  Implement fairshare policies to ensure equitable resource distribution among users or groups.

- **Job Limits:**
  Set limits on job sizes and runtimes to prevent individual jobs from monopolizing resources.

- **Regular Policy Reviews:**
  Periodically assess and adjust scheduling policies to align with evolving organizational priorities and workloads.



In Sessions 8 through 10, we'll delve into two critical components of Slurm:

1. **Scheduler Algorithms**
2. **Slurm Accounting**

### Session 8: Scheduler Algorithms

**Overview:**
Slurm employs sophisticated scheduling algorithms to manage job queues and allocate resources efficiently. Understanding these algorithms is essential for optimizing cluster performance and ensuring fair resource distribution among users.

**Key Scheduling Algorithms:**

1. **Immediate Scheduling:**
   - **Function:** Triggered by events such as job submissions or completions, this algorithm performs quick scheduling decisions for a limited number of high-priority jobs.
   - **Configuration Parameter:** `default_queue_depth` (default: 100) determines the number of jobs considered during these events.
   - **Purpose:** Ensures prompt allocation of resources for incoming jobs without extensive computation.

2. **Backfill Scheduling:**
   - **Function:** Allows smaller jobs to run ahead of queued high-priority jobs if they don't delay the start time of those high-priority jobs.
   - **Benefits:** Enhances overall system utilization and reduces job waiting times.
   - **Configuration Parameter:** `bf_interval` sets the frequency of backfill scheduling attempts.

3. **Gang Scheduling:**
   - **Function:** Enables time-sliced sharing of resources among multiple jobs, where jobs are alternately suspended and resumed.
   - **Use Case:** Beneficial in scenarios requiring concurrent job execution with limited resources.
   - **Configuration:** Requires specific setup to define time slices and job groups.

**Configuration Considerations:**

- **Scheduling Interval:**
  - **Parameter:** `sched_interval`
  - **Description:** Defines how frequently the main scheduling loop runs, considering all jobs in the queue.
  - **Default Value:** Typically set to a value like `30 seconds`, meaning the scheduler evaluates the queue every 30 seconds.

- **Partition Configuration:**
  - **Purpose:** Partitions (similar to queues) can have distinct scheduling policies to cater to different job types or priorities.
  - **Example Configuration:**
    ```bash
    PartitionName=short PriorityTier=10 MaxTime=01:00:00 State=UP
    PartitionName=long PriorityTier=5 MaxTime=48:00:00 State=UP
    ```
  - **Explanation:** Jobs submitted to the 'short' partition have a higher priority tier and a maximum runtime of 1 hour, while those in the 'long' partition have a lower priority tier and can run up to 48 hours.

**Best Practices:**

- **Regular Monitoring:** Consistently observe job queues and resource utilization to adjust scheduling parameters as needed.
- **Policy Adjustment:** Tailor scheduling policies to align with organizational goals, such as prioritizing short jobs during peak hours.
- **Documentation:** Maintain clear records of scheduling configurations and any changes implemented.

**References:**

- [Scheduling Configuration Guide - Slurm Workload Manager](https://slurm.schedmd.com/sched_config.html)
- [Gang Scheduling - Slurm Workload Manager](https://slurm.schedmd.com/gang_scheduling.html)

### Sessions 9 & 10: Slurm Accounting

**Overview:**
Slurm's accounting functionality enables the collection and analysis of detailed information about job submissions, resource utilization, and user activities. This data is crucial for resource management, usage reporting, and enforcing organizational policies.

**Key Components:**

1. **Slurm Database Daemon (slurmdbd):**
   - **Function:** Acts as the central point for collecting and storing accounting data in a database backend.
   - **Configuration:** Requires setup to connect with a database system (e.g., MySQL or MariaDB).

2. **Accounting Commands:**
   - **`sacct`:** Generates detailed reports on job and job step information, including resource usage metrics.
   - **`sreport`:** Produces aggregated reports, such as resource utilization by user, account, or cluster.
   - **`sacctmgr`:** Manages accounting data, including creating and modifying accounts, users, and associations.

**Setting Up Accounting:**

1. **Database Configuration:**
   - **Database Setup:** Install and configure a supported database system.
   - **User and Schema Creation:** Create necessary database users and schemas for Slurm's use.

2. **slurmdbd Configuration:**
   - **Configuration File:** Define database connection parameters in the `slurmdbd.conf` file.
   - **Starting slurmdbd:** Ensure the daemon is running and properly connected to both the database and the Slurm controller.

3. **Slurm Controller Configuration:**
   - **Enable Accounting:** Set `AccountingStorageType=accounting_storage/slurmdbd` in `slurm.conf`.
   - **Define Accounting Storage Parameters:** Specify `AccountingStorageHost`, `AccountingStorageUser`, and other relevant settings.


