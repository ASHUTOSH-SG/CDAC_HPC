# Session 1: Batch Systems, Resource Manager, Scheduler

1. **What is the main function of a batch system?**
   - A) Real-time job processing
   - B) Handling large-scale batch jobs
   - C) Interactive job management
   - D) Network traffic control
   - **Answer:** B) Handling large-scale batch jobs  
   **Explanation:** A batch system is designed to handle jobs that do not require immediate execution.

2. **Which of the following defines a resource manager in an HPC system?**
   - A) Allocates resources to jobs
   - B) Manages disk space
   - C) Controls system backups
   - D) Provides network connectivity
   - **Answer:** A) Allocates resources to jobs  
   **Explanation:** A resource manager ensures that jobs are allocated the necessary computing resources.

3. **Which system is used to schedule jobs in a batch processing environment?**
   - A) Operating system scheduler
   - B) Job scheduler
   - C) Load balancer
   - D) Resource manager
   - **Answer:** B) Job scheduler  
   **Explanation:** The job scheduler organizes and queues jobs for execution in batch systems.

4. **What is SLURM used for in an HPC system?**
   - A) Network management
   - B) Job scheduling
   - C) Data backup
   - D) Task synchronization
   - **Answer:** B) Job scheduling  
   **Explanation:** SLURM (Simple Linux Utility for Resource Management) is primarily used for scheduling jobs in an HPC environment.

5. **In a batch system, which element is responsible for executing the jobs on assigned resources?**
   - A) Scheduler
   - B) Resource manager
   - C) Compute node
   - D) Job monitor
   - **Answer:** C) Compute node  
   **Explanation:** The compute node executes the job, while the scheduler and resource manager allocate resources.

6. **Which of the following is an example of a job scheduling policy?**
   - A) FIFO (First In First Out)
   - B) Round robin
   - C) Priority-based scheduling
   - D) All of the above
   - **Answer:** D) All of the above  
   **Explanation:** Different scheduling policies such as FIFO, round robin, and priority-based can be used in batch systems.

7. **In SLURM, which command submits a job to the scheduler?**
   - A) srun
   - B) sbatch
   - C) squeue
   - D) sinfo
   - **Answer:** B) sbatch  
   **Explanation:** The `sbatch` command is used to submit batch jobs to the SLURM scheduler.

8. **Which parameter in SLURM specifies the number of nodes required for a job?**
   - A) --nodes
   - B) --cpu
   - C) --partition
   - D) --time
   - **Answer:** A) --nodes  
   **Explanation:** The `--nodes` parameter specifies how many compute nodes are needed for job execution.

9. **Which command shows all jobs in the SLURM queue?**
   - A) squeue
   - B) sinfo
   - C) sstat
   - D) sacct
   - **Answer:** A) squeue  
   **Explanation:** `squeue` shows the status of all jobs in the SLURM job queue.

10. **In SLURM, what does the `sacct` command provide?**
    - A) Active job list
    - B) Job accounting data
    - C) Node status
    - D) Resource usage summary
    - **Answer:** B) Job accounting data  
    **Explanation:** `sacct` provides detailed accounting data, such as job completion, resource usage, and exit status.

11. **What is the role of a job scheduler?**
    - A) Allocating job resources
    - B) Organizing job execution order
    - C) Monitoring job completion
    - D) All of the above
    - **Answer:** D) All of the above  
    **Explanation:** The job scheduler is responsible for allocating resources, organizing execution order, and monitoring job completion.

12. **Which of the following is NOT a responsibility of the SLURM resource manager?**
    - A) Allocating computing resources
    - B) Monitoring job progress
    - C) Managing user permissions
    - D) Enforcing scheduling policies
    - **Answer:** C) Managing user permissions  
    **Explanation:** The resource manager allocates resources but doesn't manage user permissions, which is typically done by the operating system.

13. **In SLURM, which command allocates resources and runs a job?**
    - A) srun
    - B) sbatch
    - C) sinfo
    - D) squeue
    - **Answer:** A) srun  
    **Explanation:** The `srun` command is used to allocate resources and run the specified job.

14. **Which of the following scheduling strategies aims to allocate resources based on job priority?**
    - A) Round robin
    - B) Fair share
    - C) FIFO
    - D) Preemptive scheduling
    - **Answer:** B) Fair share  
    **Explanation:** Fair share scheduling allocates resources based on the priority and historical usage of users.

15. **In SLURM, which file defines the job scheduling and resource allocation parameters?**
    - A) slurm.conf
    - B) sbatch.conf
    - C) job.config
    - D) scheduler.conf
    - **Answer:** A) slurm.conf  
    **Explanation:** The `slurm.conf` file is the main configuration file for SLURM, defining job scheduling and resource allocation parameters.

16. **Which of the following is an example of a job's status in SLURM?**
    - A) RUNNING
    - B) PENDING
    - C) SUSPENDED
    - D) All of the above
    - **Answer:** D) All of the above  
    **Explanation:** Jobs in SLURM can have different statuses such as RUNNING, PENDING, or SUSPENDED, depending on their current state.

17. **Which SLURM command shows detailed job information including resource usage?**
    - A) sstat
    - B) sacct
    - C) sinfo
    - D) squeue
    - **Answer:** B) sacct  
    **Explanation:** `sacct` is used to display detailed accounting information, including resource usage and job completion details.

18. **What is a common reason for a job being in a "PENDING" state in SLURM?**
    - A) Job is waiting for resources to become available
    - B) Job is paused by the user
    - C) Job has been completed
    - D) Job was canceled by the scheduler
    - **Answer:** A) Job is waiting for resources to become available  
    **Explanation:** Jobs in the "PENDING" state are typically waiting for the required resources to become available.

19. **In SLURM, what does the "scontrol" command allow you to do?**
    - A) View job queue status
    - B) Submit jobs to the scheduler
    - C) Control job execution and state
    - D) Monitor resource usage
    - **Answer:** C) Control job execution and state  
    **Explanation:** `scontrol` allows users to control job execution, state, and configuration in SLURM.

20. **What does SLURM use to manage the execution of jobs on a cluster?**
    - A) Job queues
    - B) Resource allocation policies
    - C) Scheduling algorithms
    - D) All of the above
    - **Answer:** D) All of the above  
    **Explanation:** SLURM manages job execution using job queues, resource allocation policies, and scheduling algorithms.

21. **What SLURM command lists all available partitions?**
    - A) sinfo
    - B) squeue
    - C) scontrol
    - D) sbatch
    - **Answer:** A) sinfo  
    **Explanation:** `sinfo` provides information about available partitions, nodes, and their statuses.

22. **Which of the following can be set using SLURM's batch script?**
    - A) Maximum job run time
    - B) Number of nodes
    - C) Memory required
    - D) All of the above
    - **Answer:** D) All of the above  
    **Explanation:** SLURM batch scripts can be used to specify various job parameters, such as maximum runtime, number of nodes, and memory required.

23. **In SLURM, what does the "srun" command do?**
    - A) Starts a job in the background
    - B) Runs a job on available resources
    - C) Schedules a job for future execution
    - D) Submits a job to the queue
    - **Answer:** B) Runs a job on available resources  
    **Explanation:** `srun` is used to allocate resources and execute a job.

24. **Which file is used to specify node and resource configuration in SLURM?**
    - A) slurm.conf
    - B) node.conf
    - C) partition.conf
    - D) system.conf
    - **Answer:** A) slurm.conf  
    **Explanation:** The `slurm.conf` file defines the resource allocation and configuration of nodes.

25. **How are job dependencies managed in SLURM?**
    - A) By using job priority
    - B) By using the "after" directive in job scripts
    - C) By scheduling jobs in a specific order
    - D) By manual intervention
    - **Answer:** B) By using the "after" directive in job scripts  
    **Explanation:** The "after" directive allows users to define dependencies, ensuring that jobs execute in a specific order.

26. **Which command in SLURM is used to cancel a job?**
    - A) cancel
    - B) scancel
    - C) jobcancel
    - D) killjob
    - **Answer:** B) scancel  
    **Explanation:** `scancel` is the command used to cancel a running or pending job.

27. **What is a "node" in SLURM terminology?**
    - A) A user-defined process
    - B) A physical machine in the cluster
    - C) A job scheduling policy
    - D) A virtual machine used for computation
    - **Answer:** B) A physical machine in the cluster  
    **Explanation:** A node refers to a physical or virtual machine in an HPC cluster that runs jobs.

28. **Which option in SLURM allows a job to use a specific partition?**
    - A) --partition
    - B) --queue
    - C) --nodes
    - D) --time
    - **Answer:** A) --partition  
    **Explanation:** The `--partition` option allows the user to specify which partition the job should run on.

29. **Which of the following is a common job scheduling algorithm used in SLURM?**
    - A) First Come First Serve (FCFS)
    - B) Shortest Job First (SJF)
    - C) Priority-based scheduling
    - D) All of the above
    - **Answer:** D) All of the above  
    **Explanation:** SLURM can use various scheduling algorithms such as FCFS, SJF, and priority-based scheduling.

30. **Which command in SLURM displays the status of all nodes in the cluster?**
    - A) sinfo
    - B) scontrol
    - C) squeue
    - D) sbatch
    - **Answer:** A) sinfo  
    **Explanation:** `sinfo` is used to display the status of nodes, partitions, and their resources.


# Session 2 & 3: Submitting and Managing Jobs, Writing the Batch Script

1. **Which command in SLURM is used to submit a batch job?**
   - A) sbatch
   - B) srun
   - C) squeue
   - D) sinfo
   - **Answer:** A) sbatch  
   **Explanation:** The `sbatch` command is used to submit batch jobs to the SLURM job scheduler.

2. **Which option in a batch script defines the job's maximum run time?**
   - A) --time
   - B) --mem
   - C) --cpu
   - D) --partition
   - **Answer:** A) --time  
   **Explanation:** The `--time` option specifies the maximum run time for a job.

3. **In a SLURM batch script, which line specifies the partition for the job?**
   - A) #SBATCH --partition=compute
   - B) #SBATCH --nodes=2
   - C) #SBATCH --time=01:00:00
   - D) #SBATCH --cpu=4
   - **Answer:** A) #SBATCH --partition=compute  
   **Explanation:** The `--partition` option specifies which partition the job should run on.

4. **Which command displays the current status of jobs in SLURM?**
   - A) squeue
   - B) sbatch
   - C) scontrol
   - D) sinfo
   - **Answer:** A) squeue  
   **Explanation:** The `squeue` command shows the current status of all jobs in the SLURM queue.

5. **Which of the following SLURM directives is used to set the number of nodes for a job?**
   - A) #SBATCH --nodes
   - B) #SBATCH --cpus
   - C) #SBATCH --mem
   - D) #SBATCH --time
   - **Answer:** A) #SBATCH --nodes  
   **Explanation:** The `--nodes` directive specifies how many nodes are required for the job.

6. **Which command in SLURM allows you to check the resource usage of completed jobs?**
   - A) sacct
   - B) sstat
   - C) squeue
   - D) sbatch
   - **Answer:** A) sacct  
   **Explanation:** The `sacct` command provides job accounting data, including resource usage for completed jobs.

7. **Which directive in a SLURM batch script sets the number of CPUs required by the job?**
   - A) #SBATCH --cpus
   - B) #SBATCH --cpu
   - C) #SBATCH --nodes
   - D) #SBATCH --mem
   - **Answer:** A) #SBATCH --cpus  
   **Explanation:** The `--cpus` directive specifies how many CPUs are needed for the job.

8. **What is the purpose of the `#SBATCH --mem` directive in a batch script?**
   - A) To allocate CPU cores
   - B) To specify the amount of memory required for the job
   - C) To set the job priority
   - D) To set the partition for the job
   - **Answer:** B) To specify the amount of memory required for the job  
   **Explanation:** The `--mem` directive sets the amount of memory needed by the job.

9. **Which option in a batch script allows you to specify a job's working directory?**
   - A) --workdir
   - B) --directory
   - C) --output
   - D) --chdir
   - **Answer:** D) --chdir  
   **Explanation:** The `--chdir` option in SLURM changes the working directory before executing the job.

10. **What does the `#SBATCH --output` directive specify in a SLURM batch script?**
    - A) The location for job output files
    - B) The input file for the job
    - C) The partition to run the job
    - D) The node allocation for the job
    - **Answer:** A) The location for job output files  
    **Explanation:** The `--output` option specifies where the output of the job should be written.

11. **Which SLURM command is used to cancel a pending or running job?**
    - A) scancel
    - B) sbatch
    - C) sinfo
    - D) scontrol
    - **Answer:** A) scancel  
   **Explanation:** The `scancel` command is used to cancel a job in SLURM.

12. **Which of the following is true about the `--dependency` directive in SLURM?**
    - A) It defines job execution order based on conditions
    - B) It defines the node allocation for the job
    - C) It defines the amount of memory required for a job
    - D) It sets the maximum job runtime
    - **Answer:** A) It defines job execution order based on conditions  
    **Explanation:** The `--dependency` directive allows users to specify job execution order based on conditions like job completion.

13. **In SLURM, which command provides detailed information about the status of a job?**
    - A) sstat
    - B) sacct
    - C) sinfo
    - D) squeue
    - **Answer:** A) sstat  
   **Explanation:** The `sstat` command provides detailed information about a job's status, including resource usage.

14. **What file extension is typically used for a SLURM batch script?**
    - A) .sh
    - B) .slurm
    - C) .job
    - D) .sbatch
    - **Answer:** A) .sh  
   **Explanation:** SLURM batch scripts are commonly written in shell script format, hence the `.sh` extension.

15. **Which of the following SLURM directives specifies the maximum allowed job runtime?**
    - A) #SBATCH --time
    - B) #SBATCH --cpu
    - C) #SBATCH --nodes
    - D) #SBATCH --partition
    - **Answer:** A) #SBATCH --time  
   **Explanation:** The `--time` directive specifies the maximum allowed runtime for a job.

16. **Which of the following commands allows you to interact with a job in SLURM?**
    - A) srun
    - B) sbatch
    - C) squeue
    - D) scontrol
    - **Answer:** A) srun  
   **Explanation:** The `srun` command is used to launch interactive jobs in SLURM.

17. **Which directive specifies the name of the job in SLURM?**
    - A) #SBATCH --name
    - B) #SBATCH --jobname
    - C) #SBATCH --label
    - D) #SBATCH --id
    - **Answer:** A) #SBATCH --name  
   **Explanation:** The `--name` directive allows users to specify a name for the job.

18. **What is the default file where job error messages are logged in SLURM?**
    - A) slurm-%j.out
    - B) joberror.log
    - C) joboutput.log
    - D) slurm-%j.err
    - **Answer:** A) slurm-%j.out  
   **Explanation:** By default, job output and errors are logged into the file `slurm-%j.out`, where `%j` represents the job ID.

19. **What does the `#SBATCH --exclusive` directive do?**
    - A) Runs the job in exclusive mode on one node
    - B) Reserves all resources for the job
    - C) Prevents other jobs from being submitted to the same partition
    - D) Allows the job to use exclusive network bandwidth
    - **Answer:** A) Runs the job in exclusive mode on one node  
   **Explanation:** The `--exclusive` directive reserves the entire node for the job, preventing other jobs from using it.

20. **How can you specify a range of nodes for a SLURM job?**
    - A) #SBATCH --nodes=1-4
    - B) #SBATCH --cpus=4-8
    - C) #SBATCH --time=01:00:00-02:00:00
    - D) #SBATCH --partition=compute-1
    - **Answer:** A) #SBATCH --nodes=1-4  
   **Explanation:** The `--nodes` directive with a range, such as `1-4`, specifies the range of nodes to be allocated for the job.

21. **Which SLURM directive is used to specify the time limit for a job?**
    - A) --time
    - B) --mem
    - C) --nodes
    - D) --queue
    - **Answer:** A) --time  
   **Explanation:** The `--time` directive specifies the maximum allowed execution time for the job.

22. **Which command shows the detailed information about a job's history and resource usage?**
    - A) sacct
    - B) sstat
    - C) sinfo
    - D) scontrol
    - **Answer:** A) sacct  
   **Explanation:** `sacct` provides detailed accounting information about completed jobs, including resource usage and exit status.

23. **In SLURM, what is the command used to get the status of a specific job?**
    - A) scontrol show job <jobid>
    - B) sbatch status <jobid>
    - C) squeue <jobid>
    - D) sinfo <jobid>
    - **Answer:** A) scontrol show job <jobid>  
   **Explanation:** The `scontrol show job` command displays detailed information about a specific job.

24. **Which SLURM directive sets the job's priority in the scheduling queue?**
    - A) --priority
    - B) --preempt
    - C) --constraint
    - D) SLURM does not have a specific priority directive
    - **Answer:** D) SLURM does not have a specific priority directive  
   **Explanation:** SLURM does not directly assign priority via a directive; job priority is determined by scheduling policies.

25. **Which option in SLURM job script can you use to set the working directory for the job output?**
    - A) --output
    - B) --chdir
    - C) --path
    - D) --dir
    - **Answer:** B) --chdir  
   **Explanation:** The `--chdir` option sets the working directory where the job's output is stored.

26. **What type of jobs can be submitted using the `sbatch` command?**
    - A) Interactive jobs
    - B) Batch jobs
    - C) Long-running tasks
    - D) Both batch and interactive jobs
    - **Answer:** B) Batch jobs  
   **Explanation:** The `sbatch` command is used for submitting batch jobs, not interactive jobs.

27. **Which SLURM command is used to show the current state of the entire cluster?**
    - A) sinfo
    - B) scontrol
    - C) sbatch
    - D) squeue
    - **Answer:** A) sinfo  
   **Explanation:** The `sinfo` command provides detailed information about the state of the cluster, partitions, and nodes.

28. **What is the default action when no memory requirement is specified in a SLURM job script?**
    - A) The job is automatically allocated with maximum memory
    - B) The job is denied submission
    - C) The job runs with the default memory setting for the node
    - D) The job uses zero memory
    - **Answer:** C) The job runs with the default memory setting for the node  
   **Explanation:** If no memory requirement is specified, the job runs with the default memory allocation for the node.

29. **Which SLURM command can be used to check the system-wide resource availability?**
    - A) sinfo
    - B) squeue
    - C) scontrol
    - D) sbatch
    - **Answer:** A) sinfo  
   **Explanation:** The `sinfo` command displays the availability of resources such as nodes and partitions in the cluster.

30. **Which SLURM directive is used to specify the output file for job logs?**
    - A) --logfile
    - B) --output
    - C) --stderr
    - D) --log
    - **Answer:** B) --output  
   **Explanation:** The `--output` directive specifies the file where job output will be saved.


# Session 4 & 5: SLURM Installation and Configuration, Submitting and Managing Jobs, Writing the Batch Script

1. **Which of the following is required for installing SLURM on a node?**
   - A) Kernel patching
   - B) SLURM package and dependencies
   - C) NVIDIA driver installation
   - D) Rebooting the system
   - **Answer:** B) SLURM package and dependencies  
   **Explanation:** SLURM requires the installation of the SLURM package and its dependencies, like munge, to work properly.

2. **Which directory is typically used to store SLURM configuration files?**
   - A) /etc/slurm
   - B) /usr/local/slurm
   - C) /var/lib/slurm
   - D) /home/slurm
   - **Answer:** A) /etc/slurm  
   **Explanation:** SLURM configuration files are typically stored in `/etc/slurm`.

3. **What command is used to install SLURM on a Linux machine?**
   - A) apt-get install slurm
   - B) yum install slurm
   - C) slurminstall
   - D) install-slurm
   - **Answer:** B) yum install slurm  
   **Explanation:** The `yum install slurm` command is used for SLURM installation on systems that use the `yum` package manager (e.g., CentOS/RHEL).

4. **Which configuration file contains the SLURM controller settings?**
   - A) slurm.conf
   - B) slurmdbd.conf
   - C) slurmctld.conf
   - D) slurm-sched.conf
   - **Answer:** A) slurm.conf  
   **Explanation:** The `slurm.conf` file contains the main configuration for SLURM, including controller and scheduler settings.

5. **In SLURM, which file is used for job accounting and database configurations?**
   - A) slurmdbd.conf
   - B) slurm.conf
   - C) job.conf
   - D) slurmdb.conf
   - **Answer:** A) slurmdbd.conf  
   **Explanation:** The `slurmdbd.conf` file is used to configure SLURM’s job accounting and database settings.

6. **Which SLURM service must be running on the controller node to manage jobs?**
   - A) slurmctld
   - B) slurmd
   - C) slurmdbd
   - D) slurmmon
   - **Answer:** A) slurmctld  
   **Explanation:** The `slurmctld` service manages job scheduling and resource allocation on the controller node.

7. **What is the purpose of the munge service in SLURM?**
   - A) To manage job scheduling policies
   - B) To authenticate communication between SLURM nodes
   - C) To store job outputs
   - D) To configure user access control
   - **Answer:** B) To authenticate communication between SLURM nodes  
   **Explanation:** Munge is used for authentication to secure communication between SLURM nodes.

8. **Which SLURM service should be running on the compute nodes to handle job execution?**
   - A) slurmctld
   - B) slurmd
   - C) slurmdbd
   - D) slurmmon
   - **Answer:** B) slurmd  
   **Explanation:** The `slurmd` service runs on compute nodes and is responsible for job execution.

9. **Where would you configure the number of CPU cores per node in SLURM?**
   - A) slurm.conf
   - B) slurmdbd.conf
   - C) slurmctld.conf
   - D) job.conf
   - **Answer:** A) slurm.conf  
   **Explanation:** The `slurm.conf` file contains the configuration for CPU cores per node under the `NodeName` section.

10. **Which SLURM command is used to check the SLURM configuration for errors?**
    - A) slurmd -t
    - B) scontrol reconfigure
    - C) slurmctld -t
    - D) srun check
    - **Answer:** C) slurmctld -t  
   **Explanation:** The `slurmctld -t` command checks the SLURM configuration for syntax errors.

11. **Which of the following is NOT a valid SLURM scheduling policy?**
    - A) First Come First Served (FCFS)
    - B) Shortest Job First (SJF)
    - C) Round Robin
    - D) FIFO
    - **Answer:** C) Round Robin  
   **Explanation:** SLURM does not support Round Robin scheduling by default, but it supports FCFS and SJF.

12. **Which SLURM command is used to reload the SLURM configuration after a change?**
    - A) scontrol reconfigure
    - B) slurmctld reload
    - C) slurmd restart
    - D) scontrol reload
    - **Answer:** A) scontrol reconfigure  
   **Explanation:** The `scontrol reconfigure` command reloads the SLURM configuration after changes are made.

13. **Which SLURM configuration file defines resource limits for users and jobs?**
    - A) slurm.conf
    - B) slurmdbd.conf
    - C) slurm-accounting.conf
    - D) slurm-limits.conf
    - **Answer:** A) slurm.conf  
   **Explanation:** The `slurm.conf` file defines the limits on resources, partitions, and job configurations.

14. **Which command is used to check the status of the SLURM controller daemon?**
    - A) systemctl status slurmctld
    - B) slurmctl status
    - C) slurmstatus
    - D) scontrol status slurmctld
    - **Answer:** A) systemctl status slurmctld  
   **Explanation:** The `systemctl status slurmctld` command checks the status of the SLURM controller daemon.

15. **Which SLURM directive defines the number of nodes required for a job?**
    - A) --nodes
    - B) --cpus-per-task
    - C) --ntasks
    - D) --mem
    - **Answer:** A) --nodes  
   **Explanation:** The `--nodes` directive specifies the number of nodes required for a job.

16. **In SLURM, which command is used to view and modify job parameters?**
    - A) scontrol
    - B) squeue
    - C) sinfo
    - D) sbatch
    - **Answer:** A) scontrol  
   **Explanation:** The `scontrol` command is used to view and modify job parameters, such as job state and priority.

17. **Which SLURM directive specifies the maximum wall time for a job?**
    - A) --time
    - B) --walltime
    - C) --max-time
    - D) --duration
    - **Answer:** A) --time  
   **Explanation:** The `--time` directive sets the maximum wall time allowed for a job.

18. **What file needs to be edited to change the SLURM job scheduler configuration?**
    - A) slurm.conf
    - B) slurm-scheduler.conf
    - C) slurmctld.conf
    - D) job.cfg
    - **Answer:** A) slurm.conf  
   **Explanation:** The `slurm.conf` file is edited to change job scheduling configurations, including partition, nodes, and resource limits.

19. **Which command in SLURM shows detailed information about a job's state?**
    - A) sstat
    - B) scontrol show job
    - C) squeue
    - D) sinfo
    - **Answer:** B) scontrol show job  
   **Explanation:** The `scontrol show job` command provides detailed information about a specific job's state.

20. **What does the `--gres` option in SLURM specify?**
    - A) General resource allocation
    - B) General resources for CPU cores
    - C) General resources for GPU allocation
    - D) General resource scheduling
    - **Answer:** C) General resources for GPU allocation  
   **Explanation:** The `--gres` option specifies the allocation of general resources such as GPUs.

21. **Which configuration file in SLURM is responsible for job accounting and logging?**
    - A) slurmdbd.conf
    - B) slurm.conf
    - C) joblog.conf
    - D) slurm-accounting.conf
    - **Answer:** A) slurmdbd.conf  
   **Explanation:** The `slurmdbd.conf` file handles job accounting and logging configurations.

22. **Which command is used to start the SLURM controller?**
    - A) systemctl start slurmctld
    - B) slurmctld start
    - C) slurmstart
    - D) scontrol start
    - **Answer:** A) systemctl start slurmctld  
   **Explanation:** The `systemctl start slurmctld` command is used to start the SLURM controller service.

23. **Which directive in SLURM batch scripts sets the job’s output file?**
    - A) --output
    - B) --error
    - C) --logfile
    - D) --result
    - **Answer:** A) --output  
   **Explanation:** The `--output` directive in SLURM specifies the file to store job output.

24. **Which SLURM configuration file defines the resource allocation for different partitions?**
    - A) slurm.conf
    - B) partition.conf
    - C) slurm-partition.conf
    - D) job.conf
    - **Answer:** A) slurm.conf  
   **Explanation:** The `slurm.conf` file defines partition-based resource allocation, such as CPU, memory, and node configurations.

25. **Which command is used to submit a job to SLURM?**
    - A) sbatch
    - B) squeue
    - C) scontrol
    - D) srun
    - **Answer:** A) sbatch  
   **Explanation:** The `sbatch` command is used to submit batch jobs to the SLURM scheduler.

26. **What directive in SLURM is used to specify a specific partition for a job?**
    - A) --partition
    - B) --node
    - C) --resource
    - D) --queue
    - **Answer:** A) --partition  
   **Explanation:** The `--partition` directive specifies the partition on which to run the job.

27. **Which SLURM command is used to display information about running jobs in the queue?**
    - A) squeue
    - B) sinfo
    - C) sbatch
    - D) scontrol
    - **Answer:** A) squeue  
   **Explanation:** The `squeue` command is used to display information about jobs in the queue.

28. **What is the primary function of the SLURM job scheduler?**
    - A) To authenticate users
    - B) To manage disk space allocation
    - C) To allocate resources and schedule jobs
    - D) To monitor job completion
    - **Answer:** C) To allocate resources and schedule jobs  
   **Explanation:** The job scheduler is responsible for allocating resources and scheduling jobs based on availability and policies.

29. **Which SLURM directive defines the memory required for a job?**
    - A) --memory
    - B) --mem
    - C) --mem-per-cpu
    - D) --resource
    - **Answer:** B) --mem  
   **Explanation:** The `--mem` directive defines the total memory required for the job.

30. **How can you ensure that a SLURM job is re-submitted after a failure?**
    - A) Use the --requeue directive
    - B) Use the --retry directive
    - C) Use the --resubmit directive
    - D) Use the --job-restart directive
    - **Answer:** A) Use the --requeue directive  
   **Explanation:** The `--requeue` directive ensures that a job is automatically re-submitted if it fails.

# Session 6 & 7: Managing Nodes, Setting Server Scheduling Policies

1. **In SLURM, which command is used to view the state of the compute nodes?**
   - A) sinfo
   - B) scontrol show node
   - C) squeue
   - D) slurmd -t
   - **Answer:** B) scontrol show node  
   **Explanation:** The `scontrol show node` command provides detailed information about the state and status of compute nodes.

2. **Which SLURM directive is used to set the maximum number of jobs that can run simultaneously on a node?**
   - A) --max-jobs
   - B) --nodes
   - C) --ntasks-per-node
   - D) --cpus-per-node
   - **Answer:** C) --ntasks-per-node  
   **Explanation:** The `--ntasks-per-node` directive specifies the number of tasks that can run on each node.

3. **What does the SLURM command `scontrol` allow you to manage?**
   - A) Jobs
   - B) Nodes
   - C) Partitions
   - D) All of the above
   - **Answer:** D) All of the above  
   **Explanation:** The `scontrol` command is used to manage jobs, nodes, partitions, and more in SLURM.

4. **Which SLURM command is used to view the status of all the nodes in the cluster?**
   - A) scontrol show node
   - B) sinfo
   - C) squeue
   - D) scontrol show status
   - **Answer:** B) sinfo  
   **Explanation:** The `sinfo` command shows the status of all nodes and partitions in the SLURM cluster.

5. **Which file contains the configuration for node-specific parameters in SLURM?**
   - A) slurm.conf
   - B) node.conf
   - C) node-specs.conf
   - D) slurmd.conf
   - **Answer:** A) slurm.conf  
   **Explanation:** The `slurm.conf` file defines node-specific parameters, such as node names, number of CPUs, memory, and partitions.

6. **How can you disable a node in SLURM so it doesn't accept jobs?**
   - A) scontrol disable
   - B) scontrol update NodeName=<node> State=DOWN
   - C) sinfo down
   - D) slurmd disable
   - **Answer:** B) scontrol update NodeName=<node> State=DOWN  
   **Explanation:** The `scontrol update NodeName=<node> State=DOWN` command disables a node so it won't accept jobs.

7. **Which SLURM command is used to restart the SLURM node daemon (`slurmd`) on a node?**
   - A) slurmd -r
   - B) systemctl restart slurmd
   - C) scontrol restart
   - D) scontrol restart slurmd
   - **Answer:** B) systemctl restart slurmd  
   **Explanation:** The `systemctl restart slurmd` command restarts the SLURM node daemon on a compute node.

8. **Which of the following is the correct format for specifying node resource limits in `slurm.conf`?**
   - A) NodeName=<node_name> CPUs=4 Memory=16GB
   - B) NodeName=<node_name> MaxJobs=10
   - C) NodeName=<node_name> Resources=CPU,Memory
   - D) NodeName=<node_name> MaxNodes=5
   - **Answer:** A) NodeName=<node_name> CPUs=4 Memory=16GB  
   **Explanation:** In `slurm.conf`, node-specific configurations like the number of CPUs and memory are specified in the format `NodeName=<node_name> CPUs=4 Memory=16GB`.

9. **Which SLURM command is used to forcefully remove a job from the queue?**
   - A) scontrol cancel job
   - B) squeue remove job
   - C) scontrol remove job
   - D) scancel job_id
   - **Answer:** D) scancel job_id  
   **Explanation:** The `scancel` command is used to cancel or remove a job from the queue based on its job ID.

10. **Which SLURM command allows the user to submit a job while specifying node and memory requirements?**
    - A) sbatch --nodes=2 --mem=4GB
    - B) srun --cpu=4 --memory=4GB
    - C) sbatch --cpus-per-task=4 --memory=4GB
    - D) scontrol submit --nodes=2 --memory=4GB
    - **Answer:** A) sbatch --nodes=2 --mem=4GB  
   **Explanation:** The `sbatch` command is used to submit a job, and the `--nodes` and `--mem` options specify the node count and memory requirements.

11. **Which scheduling policy in SLURM prioritizes jobs based on the job's submission time?**
    - A) Priority Scheduling
    - B) FIFO (First In First Out)
    - C) Shortest Job First (SJF)
    - D) Fair Share Scheduling
    - **Answer:** B) FIFO (First In First Out)  
   **Explanation:** FIFO (First In First Out) is a scheduling policy that prioritizes jobs based on their submission time.

12. **Which SLURM parameter is used to configure the default node state for nodes that are not explicitly defined?**
    - A) NodeState=DEFAULT
    - B) NodeName=default
    - C) DefaultState=UP
    - D) NodeState=IDLE
    - **Answer:** C) DefaultState=UP  
   **Explanation:** The `DefaultState=UP` parameter in `slurm.conf` sets the default state for nodes when not explicitly defined.

13. **Which of the following SLURM configurations allows for a job to run on multiple nodes?**
    - A) --nodes=1
    - B) --ntasks-per-node=1
    - C) --cpus-per-task=1
    - D) --nodes>1
    - **Answer:** D) --nodes>1  
   **Explanation:** The `--nodes>1` directive in a SLURM job submission command allows the job to run across multiple nodes.

14. **Which SLURM command is used to display the status of jobs in a queue?**
    - A) squeue
    - B) sinfo
    - C) scontrol show jobs
    - D) sbatch status
    - **Answer:** A) squeue  
   **Explanation:** The `squeue` command displays the status of jobs in the queue, showing job IDs, job states, and other information.

15. **Which SLURM directive defines the time limit for a job?**
    - A) --time
    - B) --wall-time
    - C) --duration
    - D) --max-time
    - **Answer:** A) --time  
   **Explanation:** The `--time` directive sets the maximum wall time for a job.

16. **Which SLURM directive defines the number of CPUs required by a job?**
    - A) --cpus-per-task
    - B) --cpus
    - C) --tasks
    - D) --num-cores
    - **Answer:** A) --cpus-per-task  
   **Explanation:** The `--cpus-per-task` directive specifies the number of CPUs needed for each task in the job.

17. **Which command is used to check the current resource allocation on SLURM-managed nodes?**
    - A) scontrol show resource
    - B) sinfo
    - C) squeue
    - D) sinfo --resource
    - **Answer:** B) sinfo  
   **Explanation:** The `sinfo` command shows information about the available resources and status of nodes in the cluster.

18. **Which SLURM command displays detailed information about the status of a specific job?**
    - A) scontrol show job
    - B) squeue job
    - C) scontrol show jobid
    - D) sjob status
    - **Answer:** A) scontrol show job  
   **Explanation:** The `scontrol show job` command provides detailed status information about a specific job.

19. **Which of the following SLURM scheduling policies ensures fair resource allocation based on user history and usage?**
    - A) FIFO
    - B) Shortest Job First
    - C) Fair Share Scheduling
    - D) Priority Scheduling
    - **Answer:** C) Fair Share Scheduling  
   **Explanation:** Fair Share Scheduling ensures that resources are allocated to users based on their previous job usage, giving fair access to resources.

20. **What is the purpose of the `--constraint` directive in SLURM?**
    - A) To specify node characteristics or hardware features required for a job
    - B) To limit the number of CPUs per task
    - C) To define the job's memory requirements
    - D) To specify the maximum job time
    - **Answer:** A) To specify node characteristics or hardware features required for a job  
   **Explanation:** The `--constraint` directive is used to specify particular hardware or software features required for a job to run.

21. **Which command in SLURM can be used to change the state of a node to 'DRAIN'?**
    - A) scontrol update NodeName=<node> State=DRAIN
    - B) scontrol down NodeName=<node>
    - C) sinfo drain
    - D) scontrol disable NodeName=<node>
    - **Answer:** A) scontrol update NodeName=<node> State=DRAIN  
   **Explanation:** The `scontrol update NodeName=<node> State=DRAIN` command sets the state of a node to 'DRAIN', preventing new jobs from starting on it.

22. **Which SLURM configuration file specifies how many resources are available for each partition?**
    - A) slurm.conf
    - B) partition.conf
    - C) resources.conf
    - D) partition-specs.conf
    - **Answer:** A) slurm.conf  
   **Explanation:** The `slurm.conf` file specifies the available resources for each partition, such as CPU, memory, and node configurations.

23. **What does the `scontrol show partition` command display?**
    - A) Information about a specific partition's resources and state
    - B) Detailed job status
    - C) Node status in the partition
    - D) List of all partitions
    - **Answer:** A) Information about a specific partition's resources and state  
   **Explanation:** The `scontrol show partition` command displays information about the resources and state of a specific partition.

24. **Which SLURM configuration parameter specifies the maximum number of running jobs per user in a partition?**
    - A) MaxJobs
    - B) MaxTasks
    - C) MaxJobsPerUser
    - D) MaxJobCount
    - **Answer:** C) MaxJobsPerUser  
   **Explanation:** The `MaxJobsPerUser` parameter specifies the maximum number of jobs a user can run in a partition at any given time.

25. **Which SLURM directive is used to define job array behavior, such as job dependencies or indexing?**
    - A) --job-array
    - B) --array-index
    - C) --dependency
    - D) --array
    - **Answer:** D) --array  
   **Explanation:** The `--array` directive is used to define job arrays in SLURM, including indexing and job dependencies.

26. **Which SLURM parameter allows setting the maximum number of nodes a job can request?**
    - A) MaxNodes
    - B) --nodes
    - C) MaxJobNodes
    - D) NodeLimit
    - **Answer:** A) MaxNodes  
   **Explanation:** The `MaxNodes` parameter limits the maximum number of nodes a job can request in SLURM.

27. **Which command is used to get a detailed view of the system's resource usage by node in SLURM?**
    - A) sinfo --nodes
    - B) scontrol show resource
    - C) scontrol show node
    - D) sinfo --resource-usage
    - **Answer:** C) scontrol show node  
   **Explanation:** The `scontrol show node` command gives detailed information about resource usage by each node in SLURM.

28. **What does the SLURM `--exclusive` directive do when submitting a job?**
    - A) It ensures that the job uses all the resources of a single node exclusively.
    - B) It runs the job on nodes with exclusive hardware features.
    - C) It ensures the job runs without preemption.
    - D) It guarantees that the job will run on high-priority nodes.
    - **Answer:** A) It ensures that the job uses all the resources of a single node exclusively.  
   **Explanation:** The `--exclusive` directive ensures that no other jobs share the resources of the node where the job is running.

29. **What does the SLURM `--dependency` option allow a user to do?**
    - A) Set job priorities
    - B) Create job dependencies, so one job runs after another
    - C) Set resource limits
    - D) Ensure exclusive access to a node
    - **Answer:** B) Create job dependencies, so one job runs after another  
   **Explanation:** The `--dependency` option allows setting dependencies between jobs, ensuring that one job runs only after another has completed.

30. **What is the primary purpose of SLURM's job accounting features?**
    - A) To allow users to manage jobs in a queue
    - B) To manage job priorities
    - C) To track resource usage for each job and user
    - D) To manage node allocation policies
    - **Answer:** C) To track resource usage for each job and user  
   **Explanation:** SLURM's job accounting features track the amount of resources used by each job, providing usage statistics for jobs and users.



# Session 8 & 9: Resource Scheduling, Monitoring Jobs and Node Performance

1. **In SLURM, which command is used to check the real-time status of job queues?**
   - A) squeue
   - B) sinfo
   - C) sbatch
   - D) scontrol show job
   - **Answer:** A) squeue  
   **Explanation:** The `squeue` command displays the status of jobs in the queue, including job ID, status, and the nodes allocated.

2. **Which of the following commands can be used to view detailed information about a SLURM job after it's been submitted?**
   - A) scontrol show job
   - B) squeue -l
   - C) sinfo
   - D) sbatch status
   - **Answer:** A) scontrol show job  
   **Explanation:** The `scontrol show job` command provides detailed information about a specific SLURM job.

3. **In SLURM, which option is used to view the status of running jobs, including resource usage?**
   - A) scontrol show jobs
   - B) sinfo
   - C) squeue -t running
   - D) scontrol show jobid
   - **Answer:** C) squeue -t running  
   **Explanation:** The `squeue -t running` command lists all currently running jobs in SLURM, showing their status and resource usage.

4. **Which SLURM directive allows jobs to be scheduled based on the available CPUs?**
   - A) --cpus-per-task
   - B) --nodes
   - C) --cpu-per-core
   - D) --ntasks
   - **Answer:** A) --cpus-per-task  
   **Explanation:** The `--cpus-per-task` directive defines how many CPUs a job requires for each task.

5. **Which of the following SLURM commands shows detailed information about job nodes, partitions, and resource utilization?**
   - A) sinfo
   - B) squeue
   - C) scontrol show nodes
   - D) scontrol show job
   - **Answer:** C) scontrol show nodes  
   **Explanation:** The `scontrol show nodes` command provides detailed information about node status, partitions, and resource utilization.

6. **How can you view the resource usage history of a specific SLURM job?**
   - A) scontrol show jobid
   - B) sinfo
   - C) sacct
   - D) squeue
   - **Answer:** C) sacc  
   **Explanation:** The `sacct` command allows users to view job accounting information, including resource usage history.

7. **Which command is used to show the current job information and node status in SLURM?**
   - A) sinfo
   - B) squeue
   - C) scontrol show job
   - D) scontrol show nodes
   - **Answer:** B) squeue  
   **Explanation:** The `squeue` command shows current job information, node status, and resource utilization.

8. **Which of the following SLURM scheduling policies ensures that each job gets an equal share of resources?**
   - A) FIFO
   - B) Priority Scheduling
   - C) Fair Share Scheduling
   - D) Backfill Scheduling
   - **Answer:** C) Fair Share Scheduling  
   **Explanation:** Fair Share Scheduling ensures that each user gets an equal share of resources based on their past usage.

9. **Which SLURM configuration directive is used to define the maximum number of jobs a user can submit to a specific partition?**
   - A) MaxJobs
   - B) MaxJobsPerUser
   - C) MaxTaskCount
   - D) MaxJobPerPartition
   - **Answer:** B) MaxJobsPerUser  
   **Explanation:** The `MaxJobsPerUser` directive sets the maximum number of jobs a user can submit to a partition.

10. **What does the `--exclusive` option in a SLURM job submission do?**
    - A) Runs the job with the highest priority
    - B) Ensures that the job uses all resources of the assigned node exclusively
    - C) Runs the job only on a specific partition
    - D) Disables preemption of the job
    - **Answer:** B) Ensures that the job uses all resources of the assigned node exclusively  
   **Explanation:** The `--exclusive` option ensures that no other jobs share the resources of the node where the job runs.

11. **Which SLURM command allows you to monitor and manage the SLURM job scheduler?**
    - A) squeue
    - B) sinfo
    - C) scontrol
    - D) sbatch
    - **Answer:** C) scontrol  
   **Explanation:** The `scontrol` command is used to manage and monitor the SLURM job scheduler, including jobs, nodes, and partitions.

12. **Which SLURM directive is used to specify a job’s runtime limit?**
    - A) --time
    - B) --wall-time
    - C) --runtime
    - D) --job-time-limit
    - **Answer:** A) --time  
   **Explanation:** The `--time` directive specifies the maximum runtime (walltime) allowed for a job in SLURM.

13. **Which SLURM scheduling policy is designed to prioritize smaller jobs first?**
    - A) Priority Scheduling
    - B) FIFO
    - C) Shortest Job First (SJF)
    - D) Backfill Scheduling
    - **Answer:** C) Shortest Job First (SJF)  
   **Explanation:** Shortest Job First (SJF) scheduling policy prioritizes smaller jobs in the queue to improve resource utilization.

14. **How can a user check the resource usage of a job in real-time?**
    - A) sinfo
    - B) squeue
    - C) scontrol show jobid
    - D) scontrol show nodes
    - **Answer:** B) squeue  
   **Explanation:** The `squeue` command provides real-time information about job status and resource usage.

15. **What does the `sacct` command do in SLURM?**
    - A) It provides detailed job status and history.
    - B) It shows the available nodes in the cluster.
    - C) It submits a new job to the queue.
    - D) It displays job completion time.
    - **Answer:** A) It provides detailed job status and history.  
   **Explanation:** The `sacct` command allows users to access accounting information related to jobs, including their status and resource consumption.

16. **Which SLURM directive specifies the maximum number of CPUs a job can use?**
    - A) --cpus-per-task
    - B) --cpus
    - C) --cpu-count
    - D) --max-cpus
    - **Answer:** A) --cpus-per-task  
   **Explanation:** The `--cpus-per-task` directive limits the number of CPUs used per task in SLURM.

17. **Which SLURM configuration parameter can be used to adjust job scheduling based on priority?**
    - A) PriorityWeightAge
    - B) PriorityWeightFairshare
    - C) PriorityWeightSize
    - D) All of the above
    - **Answer:** D) All of the above  
   **Explanation:** All these parameters (`PriorityWeightAge`, `PriorityWeightFairshare`, and `PriorityWeightSize`) can be used to adjust job scheduling priority in SLURM.

18. **Which SLURM command allows you to modify a running job’s priority or state?**
    - A) scontrol update
    - B) squeue modify
    - C) sbatch update
    - D) scontrol modify
    - **Answer:** A) scontrol update  
   **Explanation:** The `scontrol update` command allows modification of a running job's priority or state.

19. **Which of the following is a resource management tool integrated with SLURM for monitoring and scheduling jobs?**
    - A) Nagios
    - B) Grafana
    - C) Ganglia
    - D) SLURM Monitor
    - **Answer:** C) Ganglia  
   **Explanation:** Ganglia is a widely used monitoring system that integrates with SLURM to monitor job and node performance.

20. **How can you view the status of nodes in SLURM, including their availability and resource usage?**
    - A) sinfo
    - B) scontrol show node
    - C) squeue
    - D) sbatch
    - **Answer:** A) sinfo  
   **Explanation:** The `sinfo` command displays node status, availability, and resource usage in SLURM.

21. **Which SLURM option defines the number of nodes required for a job?**
    - A) --nodes
    - B) --ntasks
    - C) --cpus-per-task
    - D) --cpus
    - **Answer:** A) --nodes  
   **Explanation:** The `--nodes` directive specifies the number of nodes required for a job in SLURM.

22. **What is the purpose of the `--exclusive` option in SLURM?**
    - A) To allocate exclusive resources for a job
    - B) To ensure no other jobs share a node
    - C) To prioritize job scheduling
    - D) To restrict the job to a specific partition
    - **Answer:** B) To ensure no other jobs share a node  
   **Explanation:** The `--exclusive` option ensures that a job uses all the resources of a node without sharing with other jobs.

23. **Which SLURM parameter helps determine job scheduling priorities based on user history and job size?**
    - A) PriorityWeightFairshare
    - B) PriorityWeightSize
    - C) PriorityWeightAge
    - D) JobHistory
    - **Answer:** A) PriorityWeightFairshare  
   **Explanation:** The `PriorityWeightFairshare` parameter influences job scheduling priorities based on user history.

24. **What is the primary use of SLURM’s `backfill` feature?**
    - A) To schedule jobs based on their priority
    - B) To schedule smaller jobs that do not delay larger ones
    - C) To allocate resources exclusively to large jobs
    - D) To manage node failures
    - **Answer:** B) To schedule smaller jobs that do not delay larger ones  
   **Explanation:** The `backfill` feature allows SLURM to schedule smaller jobs in available gaps without delaying larger jobs.

25. **Which SLURM command is used to cancel a specific job in the queue?**
    - A) squeue cancel
    - B) scontrol cancel
    - C) scancel
    - D) sbatch cancel
    - **Answer:** C) scancel  
   **Explanation:** The `scancel` command is used to cancel a specific job in SLURM.

26. **What does the `sacct` command do?**
    - A) Monitors job progress
    - B) Provides job accounting information
    - C) Modifies job parameters
    - D) Allocates new nodes
    - **Answer:** B) Provides job accounting information  
   **Explanation:** The `sacct` command is used to view job accounting information, including resource usage and job completion status.

27. **Which of the following is a valid SLURM job state?**
    - A) RUNNING
    - B) QUEUED
    - C) COMPLETED
    - D) All of the above
    - **Answer:** D) All of the above  
   **Explanation:** SLURM uses various job states, including `RUNNING`, `QUEUED`, and `COMPLETED`.

28. **Which SLURM command provides information about available job partitions?**
    - A) sinfo
    - B) sbatch
    - C) scontrol show partition
    - D) squeue -p
    - **Answer:** A) sinfo  
   **Explanation:** The `sinfo` command displays information about available job partitions and their resource usage.

29. **What is the purpose of SLURM's `--ntasks` directive?**
    - A) It specifies the number of nodes required for a job
    - B) It specifies the number of CPUs per task
    - C) It specifies the number of tasks a job will run
    - D) It specifies the maximum memory per task
    - **Answer:** C) It specifies the number of tasks a job will run  
   **Explanation:** The `--ntasks` directive defines how many tasks a job will run across nodes.

30. **Which SLURM command can be used to monitor job status and identify resources used by the job?**
    - A) squeue
    - B) scontrol
    - C) sinfo
    - D) sbatch
    - **Answer:** A) squeue  
   **Explanation:** The `squeue` command allows monitoring of job status and the resources consumed by jobs in SLURM.

# Session 10: SLURM Accounting

1. **Which SLURM command is used to gather job accounting data?**
   - A) scontrol
   - B) sacct
   - C) squeue
   - D) sinfo
   - **Answer:** B) sacct  
   **Explanation:** The `sacct` command is used to gather job accounting data such as resource usage, job start and end times, and exit codes.

2. **What information can you obtain using the `sacct` command in SLURM?**
   - A) Job resource usage
   - B) Job state transitions
   - C) Job completion times
   - D) All of the above
   - **Answer:** D) All of the above  
   **Explanation:** The `sacct` command provides comprehensive job accounting information, including resource usage, state transitions, and completion times.

3. **Which SLURM parameter defines the accounting storage directory?**
   - A) AccountingStorage
   - B) SlurmAccountingStorage
   - C) AccountingStorageDir
   - D) SlurmAccountStorage
   - **Answer:** C) AccountingStorageDir  
   **Explanation:** The `AccountingStorageDir` parameter specifies the directory where job accounting information is stored in SLURM.

4. **Which SLURM configuration file contains accounting settings?**
   - A) slurm.conf
   - B) slurmdbd.conf
   - C) job.conf
   - D) accounting.conf
   - **Answer:** B) slurmdbd.conf  
   **Explanation:** The `slurmdbd.conf` file contains the configuration settings for SLURM’s accounting database daemon.

5. **What does SLURM's accounting data store?**
   - A) Job resource usage
   - B) Job priority
   - C) Job failure reasons
   - D) All of the above
   - **Answer:** D) All of the above  
   **Explanation:** SLURM's accounting data stores various details about jobs, including resource usage, priority, and reasons for job failures.

6. **Which SLURM command can be used to report job accounting information for jobs in the past?**
   - A) sacct
   - B) sinfo
   - C) squeue
   - D) scontrol
   - **Answer:** A) sacct  
   **Explanation:** The `sacct` command can be used to report historical job accounting information for completed jobs.

7. **What is the purpose of the `--format` option in the `sacct` command?**
   - A) To display job resource usage
   - B) To specify the output format of job accounting information
   - C) To filter jobs by partition
   - D) To modify job state
   - **Answer:** B) To specify the output format of job accounting information  
   **Explanation:** The `--format` option allows users to specify which fields to display in the output of the `sacct` command.

8. **Which of the following accounting fields can be displayed using the `sacct` command?**
   - A) Job ID
   - B) Job state
   - C) CPU time used
   - D) All of the above
   - **Answer:** D) All of the above  
   **Explanation:** The `sacct` command can display various fields, such as job ID, state, and CPU time used, depending on the format specified.

9. **What does the `--starttime` option in the `sacct` command specify?**
   - A) The job's start time
   - B) The time range for displaying job accounting data
   - C) The maximum duration of jobs to display
   - D) The time when the job was submitted
   - **Answer:** B) The time range for displaying job accounting data  
   **Explanation:** The `--starttime` option specifies the time range from which job accounting information should be retrieved.

10. **Which SLURM command provides accounting information for jobs completed within a specific time frame?**
    - A) scontrol
    - B) sinfo
    - C) squeue
    - D) sacct
    - **Answer:** D) sacct  
   **Explanation:** The `sacct` command can provide job accounting information for jobs completed within a specified time frame.

11. **Which SLURM option is used with `sacct` to show the exit code for each job?**
    - A) --exitcode
    - B) --jobexit
    - C) --exit
    - D) --status
    - **Answer:** A) --exitcode  
   **Explanation:** The `--exitcode` option displays the exit code for each job in the `sacct` output.

12. **How can you track resource usage over time for all completed jobs in SLURM?**
    - A) By using the `scontrol` command
    - B) By using the `sacct` command with `--format`
    - C) By using the `squeue` command with `--format`
    - D) By using the `sinfo` command
    - **Answer:** B) By using the `sacct` command with `--format`  
   **Explanation:** The `sacct` command with `--format` allows tracking resource usage for all completed jobs in SLURM.

13. **Which SLURM component stores accounting data?**
    - A) slurmctld
    - B) slurmdbd
    - C) slurmd
    - D) slurmdb
    - **Answer:** B) slurmdbd  
   **Explanation:** The `slurmdbd` (SLURM Database Daemon) is responsible for storing job accounting data.

14. **Which of the following is NOT a valid field that can be displayed with `sacct`?**
    - A) CPUTime
    - B) State
    - C) ExitCode
    - D) PartitionName
    - **Answer:** D) PartitionName  
   **Explanation:** `PartitionName` is not a valid field for job accounting in `sacct`; instead, `Partition` is typically used.

15. **Which SLURM configuration parameter enables the job accounting feature?**
    - A) EnableAccounting
    - B) AccountingStorageType
    - C) JobAccounting
    - D) AccountingEnabled
    - **Answer:** B) AccountingStorageType  
   **Explanation:** The `AccountingStorageType` parameter in SLURM enables job accounting and specifies the accounting storage backend (e.g., `accounting_storage/slurmdbd`).

16. **Which of the following is NOT stored by SLURM's accounting system?**
    - A) Job start time
    - B) Job user
    - C) Job exit code
    - D) Job's CPU count during runtime
    - **Answer:** D) Job's CPU count during runtime  
   **Explanation:** While SLURM tracks resource usage, such as the total CPU time, the exact CPU count during runtime is not specifically stored by the accounting system.

17. **Which SLURM command is used to delete accounting data for completed jobs?**
    - A) sacct delete
    - B) scontrol remove accounting
    - C) slurmdbd remove data
    - D) There is no direct command to delete accounting data
    - **Answer:** D) There is no direct command to delete accounting data  
   **Explanation:** SLURM does not allow direct deletion of accounting data for completed jobs through a command. The data is typically archived.

18. **Which of the following parameters can be modified in SLURM's job accounting configuration?**
    - A) AccountingStorageType
    - B) AccountingStorageHost
    - C) AccountingStoragePort
    - D) All of the above
    - **Answer:** D) All of the above  
   **Explanation:** All of these parameters can be modified in the SLURM accounting configuration file (`slurmdbd.conf`).

19. **Which SLURM command would you use to view the job accounting data in a tabular format?**
    - A) squeue
    - B) sacct -X
    - C) sacct -o jobid,account,alloccpus,elapsed,exitcode
    - D) sinfo
    - **Answer:** C) sacct -o jobid,account,alloccpus,elapsed,exitcode  
   **Explanation:** The `sacct -o` command allows displaying job accounting data in a tabular format, specifying the desired fields.

20. **Which SLURM parameter controls the periodicity of job accounting data?**
    - A) AccountingFrequency
    - B) AccountingPeriod
    - C) AccountingInterval
    - D) AccountingHistoryDuration
    - **Answer:** C) AccountingInterval  
   **Explanation:** The `AccountingInterval` parameter controls how often job accounting data is written to the storage backend.

21. **Which SLURM command allows users to retrieve the job accounting data for a particular user?**
    - A) sacct --user <username>
    - B) squeue --user <username>
    - C) sinfo --user <username>
    - D) scontrol show user
    - **Answer:** A) sacct --user <username>  
   **Explanation:** The `sacct --user` command allows users to retrieve job accounting data specific to a user.

22. **What is the default accounting backend storage for SLURM?**
    - A) MySQL
    - B) PostgreSQL
    - C) SQLite
    - D) SlurmDBD
    - **Answer:** D) SlurmDBD  
   **Explanation:** The default accounting backend storage for SLURM is the `SlurmDBD` daemon.

23. **Which of the following is an important benefit of using SLURM's accounting features?**
    - A) Tracking resource usage for cost allocation
    - B) Job failure diagnosis
    - C) Identifying resource bottlenecks
    - D) All of the above
    - **Answer:** D) All of the above  
   **Explanation:** SLURM accounting features help in tracking resource usage, diagnosing job failures, and identifying system bottlenecks.

24. **Which SLURM tool allows the administrator to manage SLURM job accounting configurations?**
    - A) scontrol
    - B) sinfo
    - C) slurmdbd.conf editor
    - D) sacctmgr
    - **Answer:** D) sacctmgr  
   **Explanation:** The `sacctmgr` tool is used by administrators to manage SLURM job accounting configurations.

25. **Which of the following is a valid option for the `sacct` command?**
    - A) --jobs
    - B) --partition
    - C) --format
    - D) --time
    - **Answer:** C) --format  
   **Explanation:** The `--format` option allows users to specify the fields displayed in the `sacct` command output.

26. **In which scenario would SLURM's accounting features be most useful?**
    - A) During job priority scheduling
    - B) For resource usage analysis and cost reporting
    - C) For debugging job scripts
    - D) For job submission
    - **Answer:** B) For resource usage analysis and cost reporting  
   **Explanation:** SLURM accounting features are crucial for tracking resource usage and generating reports for cost analysis.

27. **What is the purpose of SLURM's job accounting system?**
    - A) To optimize job scheduling
    - B) To record job execution details for billing and analysis
    - C) To assign job priorities
    - D) To maintain a history of job failures
    - **Answer:** B) To record job execution details for billing and analysis  
   **Explanation:** SLURM's job accounting system is designed to track job execution for billing, analysis, and reporting purposes.

28. **What does the `sacct` output include for each job?**
    - A) CPU usage, memory usage, elapsed time
    - B) Job completion status, exit code, allocated resources
    - C) Job user, job ID, job state
    - D) All of the above
    - **Answer:** D) All of the above  
   **Explanation:** The `sacct` command output includes detailed information about job resources, status, and completion data.

29. **Which of the following is a key factor that SLURM's accounting data helps monitor in large clusters?**
    - A) Job queue lengths
    - B) CPU and memory resource utilization
    - C) Job prioritization
    - D) Scheduling policies
    - **Answer:** B) CPU and memory resource utilization  
   **Explanation:** SLURM's accounting data helps monitor resource utilization, which is essential for managing large-scale clusters effectively.

30. **How does SLURM's accounting data aid system administrators?**
    - A) By enabling better resource management
    - B) By helping in user billing
    - C) By providing insights into job performance
    - D) All of the above
    - **Answer:** D) All of the above  
   **Explanation:** SLURM's accounting data provides system administrators with the necessary information for resource management, user billing, and performance analysis.

