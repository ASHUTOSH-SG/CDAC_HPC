### Quick Revision Guide for SLURM Resource Management Concepts:

**SLURM (Simple Linux Utility for Resource Management)** is a job scheduler used for managing and allocating resources on a computing cluster. Below is a breakdown of the key concepts and commands used for managing jobs, partitions, and resources in SLURM.

---

### **Assignment-2: Shell Script & Node Management**

#### **Key Concepts:**
- **Nodes:** Compute units in SLURM where jobs run. Each node has resources like CPU cores, memory, and disk storage.
- **Partitions:** Grouping of nodes based on their features or function. A partition can have specific properties like CPU, memory, and access restrictions.
- **sinfo:** A SLURM command to display information about partitions, nodes, and their status.
- **scontrol:** A command used to manage SLURM jobs, nodes, and partitions. It can show details like job status, reasons for node failure, and job scheduling information.

#### **Tasks:**
1. **Generating a row per node configuration**:
   - **Command:** `sinfo -o "%N %c %m %D"`
   - This will output a list of nodes, showing the number of CPUs, memory, and available resources.
   
2. **Generating a row per partition**:
   - **Command:** `sinfo -o "%P %C %m %D"`
   - This will list partitions along with CPU and memory usage, and available resources.

3. **Reasons for nodes being down, drained, etc.**:
   - **Command:** `scontrol show node <nodename>`
   - This provides detailed node information, including the reason for a node’s current state.

---

### **Assignment-3: Job Management and Resource Monitoring**

#### **Key Concepts:**
- **squeue:** Lists jobs in the queue with their status (running, pending).
- **srun:** Executes a job on a specified node or partition.
- **sbatch:** Submits a job script to the SLURM queue for execution.
- **Job Exit Code:** Indicates whether a job completed successfully (exit code 0) or encountered an error (non-zero exit code).

#### **Tasks:**
1. **Listing only pending jobs:**  
   - **Command:** `squeue --state=PENDING`
   
2. **Monitoring resource usage in real-time:**  
   - **Command:** `sstat -j <jobID>`
   
3. **Checking job exit code after completion:**  
   - **Command:** `sacct -j <jobID> --format=JobID,State,ExitCode`

---

### **Assignment-4: Detailed Job Information and Resource Constraints**

#### **Key Concepts:**
- **Job Scheduling:** Submitting jobs to SLURM with specific resource requirements (e.g., specific node, runtime, memory).
- **Job Exit Status:** Helps to understand if a job completed successfully or failed.

#### **Tasks:**
1. **Detailed job information after completion:**
   - **Command:** `sacct -j <jobID> --format=JobID,State,ExitCode,MaxRSS,MaxVMSize`
   
2. **Submitting a job on a specific node:**
   - **Command:** `sbatch --nodelist=<node_name> <job_script.sh>`
   
3. **Setting a maximum runtime for a job (3 hours):**
   - **Command:** `sbatch --time=03:00:00 <job_script.sh>`

---

### **Assignment-5: SLURM Commands and Concepts**

#### **Key Concepts:**
- **squeue, srun, sbatch:** Different SLURM commands used for managing jobs, running jobs, and submitting jobs, respectively.
- **Partitions in SLURM:** Group of nodes with specific configurations (e.g., CPU, memory). Partitions can be set up with time limits, node limits, etc.
- **slurmctld, slurmd, slurmdbd:** 
   - **slurmctld**: Central SLURM controller.
   - **slurmd**: Daemon running on each node to handle job execution.
   - **slurmdbd**: Database daemon for SLURM accounting.
- **Job States in SLURM:**
   - **PENDING:** The job is waiting for resources.
   - **RUNNING:** The job is currently running.
   - **COMPLETED:** The job has finished.
   - **FAILED:** The job encountered an error during execution.

#### **Important Commands:**
- **squeue:** Lists all jobs and their statuses.
- **scontrol:** Manages job states.
- **sinfo:** Provides information about partitions and nodes.

---

### **Assignment-6: Job Monitoring and Management**

#### **Key Concepts:**
- **Listing Running and Pending Jobs:**
   - **Command to list running jobs:** `squeue --state=RUNNING`
   - **Command to list pending jobs:** `squeue --state=PENDING`
   - **Command to list jobs by a specific user:** `squeue --user=<username>`
   - **Command to cancel all pending jobs:** `scancel --state=PENDING`

---

### **Assignment-7: Partition Management and Job Constraints**

#### **Key Concepts:**
- **Creating and managing partitions in SLURM.**
- **Specifying job resource requirements (walltime, CPU count).**

#### **Tasks:**
1. **Create a partition and assign a node to it:**  
   - **Command to create a partition:**
     ```bash
     scontrol create partition exam_partition Nodes=node1 TimeLimit=7-00:00:00
     ```
   
2. **Limit user job submissions to a specific number of jobs:**  
   - **Command:** Add restrictions in SLURM configuration or use `scontrol` to manage user job limits.
   
3. **Creating an SLURM account and submitting jobs under that account:**  
   - **Command:** `sacctmgr add account exam_account`
   - **Command to submit a job under an account:** `sbatch --account=exam_account <job_script.sh>`

---

### **Assignment-8: Resource Checks and Interactive Jobs**

#### **Key Concepts:**
- **Checking resource availability in a partition:**
   - **Command:** `sinfo -p <partition_name>`
   
- **Starting an interactive job:**
   - **Command:** `srun --partition=short --time=00:30:00 --cpus-per-task=2 --mem=4GB --pty bash`

- **Monitoring job progress:**  
   - **Command:** `squeue --job <jobID>`

---

### **Assignment-9: Job Reservation and Preemption**

#### **Key Concepts:**
- **Reservation:** Prevents other users from accessing resources for a certain time period.
- **Preemption:** Allows jobs to be suspended or cancelled to make room for higher-priority jobs.

#### **Tasks:**
1. **Creating a reservation:**  
   - **Command to create reservation:**  
     ```bash
     scontrol create reservation examres Partition=exam_partition Users=examuser Duration=00:10:00
     ```
   
2. **Preemption settings in `slurm.conf`:**
   - **PreemptType and PreemptMode settings** control how jobs are preempted to give priority to certain jobs or partitions.

---

### **SLURM Summary:**
- **squeue:** View job status.
- **sbatch:** Submit a job.
- **srun:** Run a job interactively.
- **scontrol:** Control job execution and node states.
- **sinfo:** Show system information about partitions and nodes.


### **Quick Revision Guide for SLURM Resource Management with QoS (Quality of Service)**

**QoS (Quality of Service)** is a feature in SLURM that allows the administrator to prioritize jobs based on certain parameters, such as job priority, time limits, and resource usage. By using QoS, you can define policies that can impact job scheduling, such as the maximum walltime, priority, and resource limits for jobs submitted under specific QoS levels.

---

### **Key Concepts - QoS in SLURM:**
- **QoS (Quality of Service):** A policy that determines job scheduling and resource allocation based on defined priority levels. It helps prioritize jobs according to various factors such as user, job size, or job urgency.
- **Setting QoS for Jobs:** You can assign a QoS to a job when submitting it, and it will affect its scheduling and execution.
- **Types of QoS:**
  - **Standard QoS:** Default setting where jobs are treated based on the usual priority, without additional restrictions or priorities.
  - **High Priority QoS:** Ensures that jobs with this QoS get preferential treatment in scheduling.
  - **Low Priority QoS:** Jobs with this QoS are scheduled only when resources are available after other jobs are scheduled.

---

### **Key Commands and Use of QoS:**

1. **Creating a QoS:**
   - **Command:**
     ```bash
     sacctmgr add qos high_priority Priority=1000 MaxWall=24:00:00
     ```
   - **Explanation:** This command creates a QoS called `high_priority` with a priority of `1000` and a maximum walltime of 24 hours.

2. **Assigning QoS to a Job:**
   - When submitting a job, use the `--qos` option to specify the QoS:
     ```bash
     sbatch --qos=high_priority <job_script.sh>
     ```
   - **Explanation:** This submits a job with the `high_priority` QoS. The job will have a higher priority in the scheduler compared to other jobs.

3. **Viewing Jobs with Specific QoS:**
   - **Command:**
     ```bash
     squeue --qos=high_priority
     ```
   - **Explanation:** This will list all jobs that have the `high_priority` QoS.

4. **Setting QoS Constraints on Job Submissions:**
   - You can also define QoS restrictions on users or accounts to limit the number of jobs or maximum runtime they can submit, such as:
     ```bash
     sacctmgr modify qos high_priority set MaxWall=48:00:00
     ```

5. **Viewing QoS for Jobs:**
   - **Command:**
     ```bash
     scontrol show job <jobID>
     ```
   - **Explanation:** This shows the details of the job, including which QoS is assigned to the job.

---

### **Preemption and QoS:**
- **Preemption in SLURM** can be controlled based on QoS settings. When preemption is enabled, jobs with a lower-priority QoS can be suspended to allow higher-priority jobs to run.
- You can configure preemption rules in the `slurm.conf` file using the `PreemptType` and `PreemptMode` options. QoS plays a critical role in the preemption process by determining which jobs are preempted and which are allowed to continue.

---

### **Example Configuration for Preemption and QoS in `slurm.conf`:**
```bash
PreemptType=preempt/qos
PreemptMode=SUSPEND,GANG
```
- **Explanation:** In this configuration, jobs with lower-priority QoS will be preempted (suspended) to make room for higher-priority jobs with different QoS settings.

---

### **Final Notes:**
- **QoS is used to manage job priorities and resource allocation**, making it a powerful tool for administrators to manage job scheduling based on user needs and system capacity.
- By applying **QoS policies**, you can ensure critical jobs are executed promptly, and non-critical jobs can be deferred or throttled based on available resources.
In the context of Slurm (a popular open-source job scheduler for high-performance computing environments), cgroups (control groups) are used to manage and limit the resources that can be allocated to jobs or tasks running on compute nodes. Slurm integrates with Linux cgroups to enhance resource management and ensure fair resource allocation, isolation, and accounting for jobs.
Key Concepts of Cgroups in Slurm:
1.	Resource Management:

○	Cgroups provide a way to group processes and allocate a set of resources (like CPU, memory, disk I/O) to these groups. Slurm uses cgroups to control the resource usage of individual jobs or job steps.
○	By integrating cgroups with Slurm, administrators can enforce limits on resources consumed by jobs, ensuring that no single job can consume excessive resources and affect others.
2.	Resource Isolation:

○	Cgroups help isolate jobs from each other by providing a mechanism to ensure that one job's resource usage (CPU, memory) does not interfere with another. This is especially important on shared systems where multiple users might be running jobs simultaneously.
3.	Resource Limits:

○	Slurm can use cgroups to enforce job resource limits, such as limiting the amount of CPU or memory a job can use. If a job exceeds these limits, Slurm can take actions like throttling the job or even killing it, depending on the configuration.
4.	Accounting:

○	Cgroups also allow for more accurate accounting of resources used by each job. Slurm can track how much CPU, memory, and other resources a job consumes, which helps with charging, fair-share scheduling, and job prioritization.
How Cgroups Work with Slurm:
When a job is submitted to Slurm, it can be configured with resource limits (e.g., CPU cores, memory, etc.). Slurm, in turn, uses Linux cgroups to enforce these limits by creating a cgroup for the job. The cgroup ensures that the job can only use the resources allocated to it and that it is isolated from other jobs running on the same machine.
1.	Job Submission: When a job is submitted to Slurm, the user can specify resource requirements such as the number of CPUs or the amount of memory. Slurm then creates a corresponding cgroup on the compute node to manage the resources.

2.	Resource Allocation: The cgroup associated with the job will be assigned the requested resources (e.g., CPU cores, memory limits). The cgroup enforces these limits by controlling the resources allocated to the job.

3.	Job Execution: During job execution, Slurm uses cgroups to ensure that the job cannot use more resources than it was allocated. If the job tries to exceed the limits (e.g., using more memory than requested), the cgroup can restrict the job, and Slurm can take predefined actions such as throttling the job or killing it.

4.	Job Completion: After the job completes, Slurm removes the cgroup, and resource usage accounting is updated, allowing the system administrator to track the job's resource consumption.

Benefits of Using Cgroups in Slurm:
1.	Fair Resource Allocation: Ensures that jobs do not exceed their allocated resources, preventing one job from monopolizing system resources and negatively affecting others.
2.	Enhanced Isolation: Provides a mechanism to isolate jobs from each other, which is particularly useful on shared systems.
3.	Resource Limits and Monitoring: Administrators can set strict resource limits, and Slurm can monitor and enforce these limits to avoid overconsumption and resource contention.
4.	Accurate Job Accounting: With cgroups, Slurm can track the resource usage of jobs accurately, which is important for job accounting, billing, and performance monitoring.
Example Use of Cgroups in Slurm:
Suppose a user submits a job to Slurm with the following resource requirements:
●	CPU cores: 4
●	Memory: 8 GB
Slurm will:
1.	Create a cgroup for this job.
2.	Assign 4 CPU cores and 8 GB of memory to the cgroup.
3.	Monitor the job to ensure it does not exceed the allocated resources.
4.	If the job exceeds the memory limit, the cgroup mechanism may throttle the job or kill it, depending on the Slurm configuration.
Slurm Configuration for Cgroups:
Slurm's cgroup integration is controlled by configuration parameters in the slurm.conf file. For example:
●	CgroupAutomount=yes: Automates the mounting of cgroups.
●	CgroupReleaseAgent: Specifies the agent used for releasing cgroup resources when a job is completed.
●	TaskPlugin=task/cgroup: Enables the task plugin that integrates cgroups with Slurm.
In conclusion, cgroups in Slurm provide a powerful mechanism for managing, isolating, and tracking the resources used by jobs in a high-performance computing environment. By using cgroups, Slurm ensures that system resources are distributed fairly, jobs are isolated, and administrators can monitor and control resource consumption more effectively.

