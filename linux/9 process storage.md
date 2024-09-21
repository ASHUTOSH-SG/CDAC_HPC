

### Disk and System Information Commands

1. **Find free disk space on the root filesystem:**
   ```bash
   df -h /
   ```
   - **df**: Disk Free; a command to display disk space usage.
   - **-h**: Human-readable format; makes sizes easier to read (e.g., KB, MB, GB).
   - **/**: The root directory; shows space for the entire filesystem.

2. **List the top 5 memory-consuming processes:**
   ```bash
   ps aux --sort=-%mem | head -n 6
   ```
   - **ps**: Process Status; displays information about running processes.
   - **aux**: Shows all users’ processes with detailed info.
   - **--sort=-%mem**: Sort by memory usage in descending order.
   - **|**: Pipe; sends output from one command to another.
   - **head -n 6**: Displays the first 6 lines of output (including the header).

3. **Display the current logged-in user:**
   ```bash
   whoami
   ```
   - **whoami**: Displays the username of the current user.

4. **Get the system uptime in a human-readable format:**
   ```bash
   uptime -p
   ```
   - **uptime**: Shows how long the system has been running.
   - **-p**: Pretty format; provides a more readable output of the uptime.

5. **Count the number of files in the /tmp directory:**
   ```bash
   ls -1 /tmp | wc -l
   ```
   - **ls**: List; displays files and directories.
   - **-1**: One file per line; makes it easier to count.
   - **/tmp**: Temporary directory; commonly used for temporary files.
   - **|**: Pipe; directs output to the next command.
   - **wc -l**: Word Count; counts the number of lines (files).

6. **Find the disk usage of the /var directory:**
   ```bash
   du -sh /var
   ```
   - **du**: Disk Usage; reports file and directory space usage.
   - **-s**: Summarize; shows only total for the specified directory.
   - **-h**: Human-readable format; displays sizes in a readable way.
   - **/var**: Variable directory; holds files that change frequently.

7. **Get the 1-minute load average of the system:**
   ```bash
   uptime | awk '{print $8}'
   ```
   - **uptime**: Provides system uptime and load averages.
   - **|**: Pipe; passes output to the next command.
   - **awk**: A text processing tool; here, it extracts the 8th field from the output (1-minute load average).
   - **'{print $8}'**: Command to print the 8th field.

8. **Count the number of users currently logged into the system:**
   ```bash
   who | wc -l
   ```
   - **who**: Displays who is logged in.
   - **|**: Pipe; sends the output to the next command.
   - **wc -l**: Counts the number of lines (i.e., users).

9. **Display the hostname of the current system:**
   ```bash
   hostname
   ```
   - **hostname**: Displays the name of the current system.

10. **List all services currently running on the system:**
    ```bash
    systemctl list-units --type=service --state=running
    ```
    - **systemctl**: Control tool for managing systemd services.
    - **list-units**: Lists active units (services, sockets, etc.).
    - **--type=service**: Filters the list to show only services.
    - **--state=running**: Shows only currently running services.

### Process-Related Questions

1. **Display all running processes along with their PID and memory usage:**
   ```bash
   ps aux --sort=-%mem
   ```
   - **ps**: Process Status; shows running processes.
   - **aux**: Displays all users’ processes.
   - **--sort=-%mem**: Sort by memory usage in descending order.

2. **Find the PID of a specific process by its name:**
   ```bash
   pgrep <process_name>
   ```
   - **pgrep**: Search for processes based on name.
   - **<process_name>**: Placeholder for the actual name of the process.

3. **Terminate a process using its PID:**
   ```bash
   kill <PID>
   ```
   - **kill**: Command to terminate a process.
   - **<PID>**: Placeholder for the Process ID of the process to be terminated.

4. **Display detailed information about a specific process:**
   ```bash
   ps -p <PID> -o pid,comm,%cpu,%mem,etime,args
   ```
   - **ps**: Shows information about processes.
   - **-p <PID>**: Specifies the process ID to query.
   - **-o**: Customizes the output format.
   - **pid, comm, %cpu, %mem, etime, args**: Fields to display (PID, command name, CPU and memory usage, elapsed time, command-line arguments).

5. **Check which user owns a particular process:**
   ```bash
   ps -o user= -p <PID>
   ```
   - **ps**: Displays process information.
   - **-o user=**: Outputs only the user field, with no header.
   - **-p <PID>**: Specifies the Process ID.

6. **Filter running processes to show only those using more than a specified amount of CPU:**
   ```bash
   ps aux --sort=-%cpu | awk '$3>threshold'
   ```
   - **ps**: Shows running processes.
   - **--sort=-%cpu**: Sorts by CPU usage in descending order.
   - **awk**: Filters output based on specified conditions.
   - **'$3>threshold'**: Prints processes where the CPU usage (3rd column) exceeds a specified threshold.

7. **See the command line arguments used to start a specific process:**
   ```bash
   ps -p <PID> -o args=
   ```
   - **ps**: Shows process information.
   - **-p <PID>**: Specifies the Process ID.
   - **-o args=**: Outputs the command-line arguments without a header.

8. **Display the top 10 processes by CPU usage:**
   ```bash
   ps aux --sort=-%cpu | head -n 11
   ```
   - **ps**: Displays running processes.
   - **--sort=-%cpu**: Sorts by CPU usage in descending order.
   - **head -n 11**: Displays the first 11 lines (10 processes plus the header).

9. **Check the parent process ID (PPID) of a running process:**
   ```bash
   ps -o ppid= -p <PID>
   ```
   - **ps**: Displays process information.
   - **-o ppid=**: Outputs only the parent process ID without a header.
   - **-p <PID>**: Specifies the Process ID.

10. **Monitor the real-time resource usage of processes on the system:**
    ```bash
    top
    ```
    - **top**: Displays real-time information about system processes, including CPU and memory usage.


    



### Script 1: CPU Usage Monitoring
### Question 1:
Write a shell script that:
- Continuously prompts the user to enter the current CPU usage percentage and a CPU usage threshold.
- If the entered CPU usage exceeds the threshold, print a warning message and break the loop.
- If the CPU usage is below the threshold, print a message indicating that the CPU usage is within the acceptable range and ask if the user wants to continue checking.
- If the user chooses to continue, ask for new input. If they choose to stop, end the script
```bash
#!/bin/bash

# Start an infinite loop to continuously prompt the user
while true; do
    # Prompt user for current CPU usage percentage
    read -p "Enter current CPU usage percentage: " cpu_usage
    # Prompt user for a CPU usage threshold
    read -p "Enter CPU usage threshold: " threshold

    # Check if the entered CPU usage exceeds the threshold
    if (( $(echo "$cpu_usage > $threshold" | bc -l) )); then
        # Print warning message if CPU usage is too high
        echo "Warning: CPU usage exceeds the threshold!"
        break  # Exit the loop
    else
        # Inform user that CPU usage is acceptable
        echo "CPU usage is within the acceptable range."
        # Ask if the user wants to continue checking
        read -p "Do you want to continue checking? (yes/no): " choice
        # If the user does not want to continue, exit the loop
        if [[ "$choice" != "yes" ]]; then
            break
        fi
    fi
done
```

### Script 2: Memory Usage Monitoring
Write a shell script that:
- Continuously prompts the user to enter the current memory usage percentage and a memory usage threshold.
- If the entered memory usage exceeds the threshold, print a warning message and break the loop.
- If the memory usage is below the threshold, print a message indicating that there is sufficient memory available and ask if the user wants to continue checking.
- If the user chooses to continue, ask for new input. If they choose to stop, end the script

```bash
#!/bin/bash

# Start an infinite loop to continuously prompt the user
while true; do
    # Prompt user for current memory usage percentage
    read -p "Enter current memory usage percentage: " mem_usage
    # Prompt user for a memory usage threshold
    read -p "Enter memory usage threshold: " threshold

    # Check if the entered memory usage exceeds the threshold
    if (( $(echo "$mem_usage > $threshold" | bc -l) )); then
        # Print warning message if memory usage is too high
        echo "Warning: Memory usage exceeds the threshold!"
        break  # Exit the loop
    else
        # Inform user that there is sufficient memory available
        echo "Sufficient memory available."
        # Ask if the user wants to continue checking
        read -p "Do you want to continue checking? (yes/no): " choice
        # If the user does not want to continue, exit the loop
        if [[ "$choice" != "yes" ]]; then
            break
        fi
    fi
done
```

### Explanation of Key Parts

- **`#!/bin/bash`**: Specifies that the script should be run using the Bash shell.
- **`while true; do`**: Starts an infinite loop that will continue until explicitly broken.
- **`read -p`**: Prompts the user for input and stores it in a variable.
- **`if (( $(echo "$value > $threshold" | bc -l) ))`**: Evaluates whether the value exceeds the threshold using `bc` for floating-point comparison.
- **`echo`**: Prints messages to the terminal.
- **`break`**: Exits the loop when a certain condition is met.
- **`if [[ "$choice" != "yes" ]]`**: Checks the user's response to decide whether to continue or exit.

