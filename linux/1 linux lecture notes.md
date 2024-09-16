# Introduction to Linux Operating System

## Why Operating Systems?
- **Applications and Disk:**
  - Applications are stored on disk as files.
  - The operating system loads these applications into main memory for execution.
- **Process:**
  - An instance of a program being executed.

---

## General Operating System Organization
- **Components:**
  - **GUI**: Graphical User Interface
  - **Shell**: Command-line interface
  - **User Processes**: Running applications
  - **OS**: Operating System
  - **System Calls**: Interface between user applications and the OS
  - **Kernel**: Core part of the OS managing hardware and resources

---

## Kernel Responsibilities
- **Functions:**
  - Process scheduling
  - Memory management
  - File system management
  - Device access management
  - Networking
  - System call API provision

---

## User Mode vs Kernel Mode
- **Modes:**
  - **User Mode:** Limited access, only user space memory accessible.
  - **Kernel Mode:** (supervisor mode) Full access, user and kernel space memory accessible.
- **Special Instructions:**
  - Halt system
  - Access memory management hardware
  - Initiate I/O operations


  **diagram**

---

## Interrupts
- **Definition:**
  - A signal sent to the CPU indicating an event.
  - Can be hardware or software initiated.
- **Process:**
  - CPU stops current tasks, transfers control to Interrupt Service Routine (ISR).
  - CPU resumes after ISR completion.
  - **Interrupt Vector Table (IVT):** Maps interrupts to their memory addresses.

---

## Introduction to Linux
- **History:**
  - Linux: World's most widely used operating system.
  - Origins in UNIX (Ken Thompson, 1969).
  - GNU created by Richard Stallman (1984) as a free software alternative.
  - Linux kernel created by Linus Torvalds (1991).

---

## True UNIX vs UNIX-like
- **True UNIX:**
  - Certified by The Open Group.
  - Maintains a single UNIX standard
  - Example: macOS.
- **UNIX-like:**
  - Not certified by The Open Group.

---

## Linux Kernel
- **Role:**
  - Main component of the OS.
  - Manages memory, process scheduling, and hardware.

---

## Installing Linux
- **Options:**
  - **Windows Subsystem for Linux (WSL):** Simplest and lightweight.
  - **Virtual Machine:** Using VMWare or Oracle VirtualBox.
  - **Dual Boot:** Windows and Linux on the same machine.

---

## Virtual Machine Concept
- **Diagram:**
  - Shows multiple virtual machines (Linux and Windows) managed by Virtual Machine Manager on a host operating system.

---

## Linux Distributions (“Distros”)
- **Examples:**
  - Ubuntu, Fedora, CentOS, etc.

---

## Linux Command Line
- **Shells:**
  - **Bourne Shell (sh)**
  - **C Shell (csh)**
  - **TC Shell (tsh)**
  - **Korn Shell (ksh)**
- **Function:**
  - User interface to the OS, provides command execution.

---

## Opening the Terminal
- **Methods:**
  - Start button → System tools → Terminal
  - Search for Terminal
  - Tools → Open Terminal
  - Shortcut: Ctrl + Alt + T

---

## The Shell Prompt
- **Format:**
  - `username@machinename:~$`
  - Indicates user and current working directory.

---

## Valid and Invalid Commands
- **Examples:**
  - Correct and incorrect command formats.
  - Handling incomplete commands and errors.

---

## The `date` Command
- **Usage:**
  - Display the system date.
  - Format example: `date +"Today is %A, %d %B %y"`
  - `TZ='America/Los_Angeles' date`: Display date according to a specified timezone.

---

## Linux Command Format
- **Structure:**
  - `command -option argument`
  - Examples: `date -I`, `date --iso`, `date -r /path/to/file`

---

## Command Options: Examples
- **Examples:**
  - `sort -ru colors.txt`
  - `sort -r -u colors.txt`
  - `sort --reverse --unique colors.txt`

---

## The Manual Page
- **Purpose:**
  - Documentation and help for commands.
  - **Command:** `man [command]`
  - Example: `man sort`
  - Type `q` to exit.

---

## The `which` Command
- **Purpose:**
  - Returns the executable file path for a command.
  - Example: `which clear`

---

## File and Directory Management
- **Directory Structure:**
  - `/`: Root directory (the very beginning of the file system)
  - `~`: Current user’s home directory (e.g. /home/dac)
  - `• .`: Current directory
  - `• ..`: Parent of the current directory
- **Commands:**
  - `touch`: Create an empty file
  - `pwd`: Print Working Directory
  - `cd`: Change directory
  - `ls`: List directory contents
  - `mkdir`: Create a directory
  - `cp`: Copy files/directories
  - `mv`: Rename or move files/directories
  - `rm`: Delete files (use `rm -r` for directories)

---




## Linux Editors
- **Editors:**
  - `vi` : The original Linux editor.
  - `vim` : Improved version of `vi`.
  - `nano` : User-friendly editor. Install using:
    - `sudo apt-get update`
    - `sudo apt-get install nano`

---

## Users and Groups

### User Management
- **Create a New User:**
  - `sudo adduser [username]`
- **Delete a User:**
  - `sudo deluser [username]` (or `userdel` on some systems).

### /etc/passwd File
- **Purpose:**
  - Maps user names to user IDs.
- **Format:**
  - Example entry:
    ```
    root:x:0:0:root:/root:/bin/bash
    cdac:x:65534:65534:cdac:/home/cdac:/bin/bash
    ```
- **Fields:**
- Field 1: User name
- Field 2: User’s encrypted password (Actual password is in the shadowfile, if it contains x)
- Field 3: User ID (UID) – User’s representation in the kernel
- Field 4: Group ID (GID) – Determines file permissions
- Field 5: User’s real name
- Field 6: User’s home directory
- Field 7: User’s shell
• Note: The superuser (root) always has UID and GID of 0

### File Ownership
- **Checking Ownership:**
- Use `ls -l` to display file owner and group.
- When we create a user, Linux automatically also creates a group by the
- same name and makes the user a part of that group
- But then, what is a group?
- **Group Management:**
- **Group:** Collection of users managing access to resources.
  - **Commands:**
    - `sudo groupadd [groupname]` : Create a new group.
    - `sudo groupmod -n [newname] [oldname]` : Rename a group.
    - `sudo groupdel [groupname]` : Remove a group.
    - `sudo usermod -aG [groupname] [username]` : Add user to group.
    - `sudo gpasswd -d [username] [groupname]` : Remove user from group.

---

## File Attributes
- **File Attributes (from `ls -l`):**
  - 10 characters indicating file type and permissions:
    - **Type:**
      - `d` : Directory
      - `-` : File
      - `l` : Symbolic link
    - **Permissions:**
      - Owner: `rwx`
      - Group: `rwx`
      - Others: `rwx`

---

## Creating and Managing Symbolic Links
- **Create a Symbolic Link:**
  - `ln -s [target] [linkname]`
  - Example: `ln -s hello.txt symbolic_link_example`
- **Verify:**
  - `ls -l`
- **Remove Symbolic Link:**
  - `rm [linkname]`

---

## File Permissions

### Character-based Permissions
- **Add/Remove Permissions:**
  - `chmod u+x [file]` : Add execute permission for the user.
  - `chmod g-w [file]` : Remove write permission from the group.
  - `chmod u+x,g+r [file]` : Add execute for user, read for group.
  - `chmod a=r [file]` : Set read-only permission for everyone.

### Octal File Permissions
- **Permission Values:**
  - `000` : No permissions
  - `001` : Execute only
  - `010` : Write only
  - `011` : Write and execute
  - `100` : Read only
  - `101` : Read and execute
  - `110` : Read and write
  - `111` : Read, write, and execute
- **Commands:**
  - `chmod 700 [file]` : Full permissions for owner only.
  - `chmod 777 [file]` : Full permissions for everyone.
  - `chmod 755 [file]` : Read/execute for all, write for owner.
  - `chmod 525 [file]` : Read/execute for owner, write for group, read/execute for others.
  - `chmod 621 [file]` : Read/write for owner, write for group, execute for others.

---

---

## Program Execution

- **Disk:** Program code is stored here.
- **Main Memory:** Program is loaded into RAM for execution.
- **CPU:** Executes the program instructions.
- **Input/Output:** Handles user interactions and outputs.

---

## Why Operating Systems?

- **Applications:** Applications are stored as files on disk.
- **Loading:** OS loads applications into main memory for execution.
- **Process:** An instance of a program in execution.

---

## General Operating System Organization

- **GUI:** Graphical User Interface.
- **Servers:** Manage network resources and services.
- **Shell:** Command-line interface for user commands.
- **User Processes:** Applications and services run by users.
- **System Calls:** Interface for user processes to interact with the OS.

---

## Kernel

- **Definition:** Core component of the OS managing hardware and resources.
- **Tasks:**
  - Process Scheduling
  - Memory Management
  - File System Management
  - Device Access Management
  - Networking
  - System Call API Provision

---

## User Mode and Kernel Mode

- **User Mode:**
  - Access only user space memory.
  - Attempts to access kernel space cause hardware exceptions.
- **Kernel Mode:**
  - Access both user and kernel space memory.
  - Executes privileged instructions like halting the system or managing I/O.

---

## Interrupts

- **Definition:** Signals to CPU indicating an event has occurred.
- **Types:**
  - **Hardware Interrupts:** Generated by hardware devices.
  - **Software Interrupts:** Generated by software using system calls.
- **Process:**
  - CPU halts current task and executes the Interrupt Service Routine (ISR).
  - After handling the interrupt, the CPU resumes the previous task.
- **Interrupt Vector Table (IVT):** Maps interrupts to their memory addresses.

---

## Introduction to Linux

- **History:**
  - Originated from UNIX (Ken Thompson, 1969).
  - GNU Project (Richard Stallman, 1984) created free software alternatives.
  - Linux Kernel (Linus Torvalds, 1991) provided the missing kernel for GNU.

- **True UNIX vs UNIX-like:**
  - **True UNIX:** Certified by The Open Group (e.g., macOS).
  - **UNIX-like:** Non-certified variants (e.g., Linux).

---

## Linux Kernel

- **Role:** Manages memory, process scheduling, hardware, etc.

---

## Installing Linux

- **Options:**
  - **Windows Subsystem for Linux (WSL):** Simplest and lightweight. [Installation Guide](https://learn.microsoft.com/en-us/windows/wsl/install)
  - **Virtual Machine:** Use VMWare or Oracle VirtualBox. [Installation Guide](https://techbland.com/how-to-install-lubuntu-on-virtualbox-on-windows/)
  - **Dual-Boot:** Install alongside Windows.

---

## Virtual Machine Concept

- **Components:**
  - **Host/Base OS:** Windows.
  - **VMs:** Linux, Windows, etc.
  - **Virtual Machine Manager:** Manages multiple VMs (e.g., VirtualBox, VMWare).

---

## Linux Distributions (“Distros”)

- **Examples:** Ubuntu, Fedora, Debian.

---

## Linux Command Line

- **Shells:**
  - **Bourne Shell (sh):** Original shell.
  - **C Shell (csh):** Part of BSD UNIX.
  - **Korn Shell (ksh):** Enhanced Bourne Shell.

---

## Opening the Terminal

- **Methods:**
  - Start button -> System Tools -> Terminal.
  - Search for Terminal in Start menu.
  - Use Ctrl + Alt + T.

---

## The Shell Prompt

- **Format:** `username@machinename:current_directory$`
- **Superuser Prompt:** Ends with `#` instead of `$`.

---

## Valid and Invalid Commands

- **Valid Commands:** Produce expected output.
- **Invalid Commands:** Generate errors.
- **Example:** Use `"` or `Ctrl+C` to exit incomplete commands.

---

## The `date` Command

- **Purpose:** Display system date.
- **Format Example:** `date +"Today is %A, %d %B %y"`
  - `%A`: Full weekday name.
  - `%d`: Day of the month.
  - `%B`: Full month name.
  - `%y`: Year without century.

---

## Linux Command Format

- **Structure:** `command -option argument`
  - **Command:** The action to perform.
  - **Options:** Modify default behavior (e.g., `-r` for reverse).
  - **Arguments:** Inputs to the command.

---

## Command Options: More Examples

- **Examples:**
  - `sort -ru colors.txt`
  - `sort -r -u colors.txt`
  - `sort --reverse --unique colors.txt`

---

## The Manual Page

- **Purpose:** Provides documentation/help about commands.
- **Usage:** `man <command>` (e.g., `man sort`).
- **Exit:** Press `q`.

---

## The `which` Command

- **Purpose:** Locate the executable file of a command.
- **Example:** `which clear`

---

## File and Directory Management

- **Directory Structure:**
  - `/`: Root directory.
  - `~`: User’s home directory.
  - `/home/<user>`: User-specific directories.

---

## Directory Shortcuts

- **`/`:** Root directory.
- **`~`:** User’s home directory.
- **`.`:** Current directory.
- **`..`:** Parent directory.

---

## File and Directory Commands

- **Commands:**
  - `touch <file>`: Create an empty file.
  - `pwd`: Print working directory.
  - `cd <path>`: Change directory.
  - `ls`: List files in directory.
  - `mkdir <dir>`: Create a directory.
  - `cp <source> <destination>`: Copy files/directories.
  - `mv <source> <destination>`: Rename or move files/directories.
  - `rm <file>`: Delete a file. Use `rm -r <dir>` to delete directories recursively.

---

## Linux Editors

- **vi:** Original Linux editor.
- **vim:** Improved version of vi.
- **nano:** Easy-to-use editor. Install with `sudo apt-get update` and `sudo apt-get install nano`.

---

## Users

- **Create User:** `sudo adduser <username>`
- **Delete User:** `sudo deluser <username>` (or `userdel`)

---

## `/etc/passwd` File

- **Purpose:** Maps user names to user IDs (UIDs).
- **Format:**
  - `username:x:UID:GID:Full Name:Home Directory:Shell`
- **Example Entry:**
  - `cdac:x:65534:65534:cdac:/home/cdac:/bin/bash`

---

## File Ownership

- **Ownership:** Every file is owned by a user.
- **Command:** Use `ls -l` to display owner and group information.

---

## Group

- **Definition:** Collection of users managing access to resources.
- **Management Commands:**
  - `groupadd <groupname>`: Create a group.
  - `groupmod -n <newname> <oldname>`: Rename a group.
  - `groupdel <groupname>`: Delete a group.
  - `usermod -aG <groupname> <username>`: Add user to a group.
  - `gpasswd -d <username> <groupname>`: Remove user from a group.

---

## File Attributes

- **Command:** `ls -l`
- **Format:**
  - `d` = Directory, `-` = File, `l` = Symbolic link.
  - **Permissions:** `r` (Read), `w` (Write), `x` (Execute).

---

## Creating a Symbolic Link

- **Command:** `ln -s <target> <linkname>`
- **Example:** `ln -s hello.txt symbolic_link_example`
- **Remove Link:** `rm <linkname>`

---

## File Permissions

- **Permissions Types:**
  - **User (`u`)**
  - **Group (`g`)**
  - **Others (`o`)**

- **Command Examples:**
  - `chmod u+x <file>`: Add execute permission for user.
  - `chmod g-w <file>`: Remove write permission for group.
  - `chmod a=r <file>`: Set read-only permissions for all.

---

## Octal File Permissions

- **Permissions Table:**

| Binary | Decimal | Permissions |
|--------|---------|-------------|
| 000    | 0       | ---         |
| 001    | 1       | --x         |
| 010    | 2       | -w-         |
| 011    | 3       | -wx         |
| 100    | 4       | r--         |
| 101    | 5       | r-x         |
| 110    | 6       | rw-         |
| 111    | 7       | rwx         |

- **Commands:**
  - `chmod 700 <file>`: Full permissions for owner, none for others.
  - `chmod 777 <file>`: Full permissions for everyone.
  - `chmod 755 <file>`: Full permissions for

 - chmod 525 file1: rx for owner, w to group, rx for others
- chmod 621 file1: rw for owner, w to group, x for others


# Process Management

---

## Program and Process

- **Process:** An instance of an executing program.
  - **Consumes resources:** CPU time, memory, etc.
  - **Tracked by the OS:** The operating system manages and schedules processes.
- **Segments of a Process:**
  - **Code/Text:** Contains the instructions of the program.
  - **Data:** Stores static variables.
  - **Heap:** Used for dynamic memory allocation by the programmer.
  - **Stack:** Manages memory that grows and shrinks with function calls, also used for local variables.



### Explanation

- **Data Segment:**
  - The `result` variable is stored here as a global variable.
- **Heap:**
  - Memory allocated dynamically for `num1` and `num2`.
- **Stack:**
  - Local variables `num1`, `num2`, and `sum` are managed on the stack.

---

## Process States

- **new:** Process is being created.
- **running:** Instructions are being executed.
- **waiting:** Process is waiting for an event.
- **ready:** Process is waiting to be assigned to a CPU.
- **terminated:** Process has finished execution.

---

## Process Control Block (PCB)

- **Definition:** Data structure maintained by the OS for each process.
- **Contains:** Useful information about the process, including state, program counter, CPU registers, etc.

---

## Process Scheduling

- **Definition:** The process of selecting a process from the ready queue and assigning it to the CPU.
- **Result:** Enables multiprogramming and efficient CPU utilization.
- **Technique:** Time multiplexing.

### Process Scheduling Steps

1. A process is running.
2. The OS moves the running process to the ready queue.
3. An interrupt occurs, causing the OS to switch to the next ready process.

---

## Process Queues

- **Job Queue:** Entry point for all processes.
- **Ready Queue:** Contains processes that are ready to run but waiting for CPU time.
- **I/O Waiting Queue:** Contains processes waiting for I/O operations to complete.

---

## Scheduler Types

- **Long Term Scheduler:** Decides which processes are admitted to the ready queue.
- **Short Term Scheduler:** Decides which process in the ready queue is executed next (CPU scheduler).
- **Medium Term Scheduler:** Manages the swapping of processes between main memory and disk.

---

## CPU Scheduling (Short Term Scheduling)

- **Resources:** CPU time, disk space.
- **Preemptive Resources:** Can be taken away by the OS (e.g., CPU time).
- **Non-preemptive Resources:** Cannot be taken away until the process releases it (e.g., file access).

### Criteria for Good Scheduling Algorithm

- **Fairness:** Ensures every process gets its fair share of CPU time.
- **Efficiency:** Keeps CPU busy.
- **Response Time:** Minimizes response time for interactive users.
- **Throughput:** Maximizes the number of jobs completed per hour.
- **Minimize Overhead:** Reduces context switching overhead.

---

## Scheduling Algorithms

- **First-Come First-Served (FCFS)**
- **Round Robin (RR)**
- **Priority**
- **Shortest Job First (SJF)**

### FCFS (First-Come First-Served)

- **Definition:** Executes processes in the order they arrive.
- **Non-preemptive:** The process is executed until completion before the next process starts.
- **Implementation:** Easiest to implement.

### Example FCFS Scheduling

| Process | Arrival Time | Processing Time |
|---------|--------------|-----------------|
| A       | 0.000        | 3               |
| B       | 1.001        | 6               |
| C       | 4.001        | 4               |
| D       | 6.001        | 2               |

### Round Robin (RR)

- **Definition:** Preemptive scheduling algorithm that uses time slices.
- **Process:** Each process gets executed for a time slice before moving to the next process.
- **Designed For:** Time-sharing systems.

### Example Round Robin Scheduling

| Process | Burst Time |
|---------|------------|
| P1      | 10         |
| P2      | 2          |
| P3      | 5          |
| P4      | 6          |

- **Time Slice:** 3 units

---



# Shell Scripts and Linux Processes

---

## Variables in Shell Scripts

### User-Defined Variables

```bash
INSTITUTE="ACTS"
echo "Hello $INSTITUTE"
```

### Shell/System Variables

```bash
echo "Home directory: $HOME"
echo "Username: $USER"
echo "Current directory: $PWD"
echo "Process ID: $$"
```

### Escape Characters

To display special characters, use the escape character `\`:

```bash
echo "Deposited \$100 to your account"
```

---

## What is a Shell Script?

- **Definition:** A file containing a series of commands to be executed by the shell.
- **Examples of Commands:**

```bash
echo "5/2" | bc
echo "scale=2; 5/2" | bc
echo "scale=10; 5/2" | bc
name="Linux Student"
echo $name > out.txt
```

---

## Linux Processes

- **Process Types:**
  - **Parent:** The initial process that spawns child processes.
  - **Child:** A process created by another process.
  - **Daemon:** Long-running processes that run in the background (e.g., sshd, httpd).
  - **Zombie (Defunct):** A terminated process that has not yet had its resources released.
  - **Orphan:** A child process whose parent has terminated before it did.

### Commands

- **View Processes:**

```bash
ps -ef | less
```

  - `e`: Show all processes
  - `f`: Full-format listing

- **Note:** The first process is init with PID 1.

---

## Important Process System Calls

- **fork():** Creates a nearly identical copy of the process.
- **exec():** Loads and starts a program, replacing the current process.

### Example

When running the `ls` command:

1. The shell calls `fork()` to create a copy of itself.
2. The new shell copy calls `exec(ls)` to run `ls`.

---

## Foreground and Background Processes

- **Foreground Processes:** Run in the terminal and prevent other commands from executing until they are terminated.
- **Background Processes:** Run in the background, allowing other commands to be executed in the foreground.

### Example

```bash
sleep 10
sleep 60 &    # Starts sleep 60 in the background
echo "hello there"
jobs           # Lists background jobs
fg             # Brings the background process to the foreground
```

---

## Linux Process Management Commands

- **ps:** Shows process status.

```bash
ps
```

  - Displays processes with columns for PID, TTY, TIME, CMD.

```bash
ps -ef
```

  - Shows all processes with additional details.

- **Finding Processes:**

```bash
ps -u atul     # Lists all processes started by user 'atul'
pstree         # Displays a tree-like representation of processes
pstree -p 1234 # Shows the tree for a particular process
top            # Provides dynamic real-time view of system processes
```

---

## Signals and Killing Processes

- **Kill a Process:**

```bash
sudo kill <pid>   # Sends a termination signal to a process
sudo kill 1947
```

- **List Signals:**

```bash
kill -l
```

- **Example:**

  - Start a calculator program.
  - Find its PID:

```bash
pgrep -l kcalc
```

  - Kill the process using its PID:

```bash
kill -2 1208    # Sends SIGINT signal (2) to PID 1208
```

  - Alternative for multiple PIDs:

```bash
pidof firefox   # Gets all PIDs for Firefox
kill -INT $(pidof firefox)  # Sends SIGINT to all PIDs
```
```



# Shell Scripts and Variables

---

## Variables in Shell Scripts

### User-Defined Variables

```bash
INSTITUTE="ACTS"
echo "Hello $INSTITUTE"
```

### Shell/System Variables

```bash
echo "Home directory: $HOME"
echo "Username: $USER"
echo "Current directory: $PWD"
echo "Process ID: $$"
```

### Escape Characters

To display special characters, use the escape character `\`:

```bash
echo "Deposited \$100 to your account"
```

---

## What is a Shell Script?

- **Definition:** A file containing a series of commands to be executed by the shell.
- **Examples of Commands:**

```bash
echo "5/2" | bc
echo "scale=2; 5/2" | bc
echo "scale=10; 5/2" | bc
name="Linux Student"
echo $name > out.txt
```

---

## Writing a Shell Script – Pseudocode

1. Open a new file with an extension `.sh` and write your pseudocode.
2. Example: Display the logged-in user’s user ID and whether it is the root user or not.

```bash
sudo nano get_user_name.sh
# Get the user id
# Check if user id is root or not
```

---

## Writing a Shell Script – Shebang Operator

- **Shebang Operator:** `#!/bin/bash`

  - `#` (sharp) and `!` (bang) together at the top of the script file.

```bash
#!/bin/bash
# Get the user id
# Check if user id is root or not
```

---

## Writing a Shell Script – Get the User ID

```bash
#!/bin/bash
# Get the user id
CURRENT_USER_NAME=$USER
echo "Logged in user is: $CURRENT_USER_NAME"
# Check if user id is root or not
```

### Executing a Shell Script

1. Try running: `get_user_name.sh`
   - Error! Specify the path using dot: `./get_user_name.sh`
   - Error! Give execute permission: `chmod u+x get_user_name.sh`
   - Try running again: `./get_user_name.sh`

### Complete the Shell Script, Save and Rerun

```bash
#!/bin/bash
# Get the user id
CURRENT_USER_NAME=$USER
echo "Logged in user is: $CURRENT_USER_NAME"
# Check if user id is root or not
if [ "$UID" -eq 0 ]; then
  echo "$CURRENT_USER_NAME is the root user."
else
  echo "$CURRENT_USER_NAME is NOT the root user."
fi
```

---

## Using Variables (read_example_prompt.sh)

```bash
#!/bin/bash
read -p "Enter your name: " name
read -p "Enter your age: " age
read -p "Enter your city: " city
echo "My name is: $name"
echo "My age is: $age"
echo "My city is: $city"
```

---

## Conditions – if Statement

```bash
#!/bin/sh
a=10
b=20
if [ $a -eq $b ]; then
  echo "a is equal to b"
fi
if [ $a -ne $b ]; then
  echo "a is not equal to b"
fi
```

### Same Example Using if-else

```bash
#!/bin/sh
a=10
b=20
if [ $a -eq $b ]; then
  echo "a is equal to b"
else
  echo "a is not equal to b"
fi
```

### Check If a Number is Even or Odd

```bash
#!/bin/bash
read -p "Enter a number : " n
rem=$(( $n % 2 ))
# Other syntaxes
# let "rem = n % 2"
# rem=$(expr $n % 2)
# rem=$(echo "$n % 2" | bc)
if [ $rem -eq 0 ]; then
  echo "$n is an even number"
else
  echo "$n is an odd number"
fi
```

### if-elif-else

```bash
#!/bin/bash
echo "Enter a Number"
read num
if [ $num -lt 0 ]; then
  echo "Negative"
elif [ $num -gt 0 ]; then
  echo "Positive"
else
  echo "Neither Positive Nor Negative"
fi
```

### Max of Three Numbers

```bash
#!/bin/bash
echo "Enter Num1"
read num1
echo "Enter Num2"
read num2
echo "Enter Num3"
read num3
# To accept multiple inputs:
# read num1 num2 num3
if [ $num1 -gt $num2 ] && [ $num1 -gt $num3 ]; then
  echo $num1
elif [ $num2 -gt $num1 ] && [ $num2 -gt $num3 ]; then
  echo $num2
else
  echo $num3
fi
```

### String Comparison

```bash
#!/bin/bash
# Shell script to check whether two input strings are equal

# Take user input
echo "Enter string a : "
read a
echo "Enter string b : "
read b

# Check equality of input
if [ "$a" == "$b" ]; then
  # If equal print equal
  echo "Strings are equal."
else
  # If not equal
  echo "Strings are not equal."
fi
```



# Advanced Shell Scripts

---

## Calculate Average Using Bash Calculator

```bash
#!/bin/bash
read -p "Enter marks in subject 1: " marks1
read -p "Enter marks in subject 2: " marks2
read -p "Enter marks in subject 3: " marks3
total=$(( $marks1 + $marks2 + $marks3 ))
echo "Total marks: $total"
avg=$( echo "scale=4; $total / 3" | bc )
echo "Average marks: $avg"
```

---

## RegEx: Check if a Filename Starts With a Specific String

```bash
#!/bin/bash

# Define file name and prefix (modify as needed)
FILE_NAME="report_2023.txt"
PREFIX="report_"

# Regex pattern for checking the prefix
prefix_regex="^$PREFIX"

# Check if filename starts with the prefix using [[ ]]
# Here, ~ means start of string
if [[ $FILE_NAME =~ $prefix_regex ]]; then
  echo "File name starts with the expected prefix '$PREFIX'."
else
  echo "File name does not start with the expected prefix."
fi
```

---

## Sending Parameters to a Script

```bash
#!/bin/bash

# Get file name and prefix as command-line arguments
FILE_NAME="$1"
PREFIX="$2"

# Check if arguments are provided
if [[ -z "$FILE_NAME" || -z "$PREFIX" ]]; then
  echo "Usage: $0 <filename> <prefix>"
  exit 1
fi

# Regex pattern for checking the prefix
prefix_regex="^$PREFIX"

# Check if filename starts with the prefix using [[ ]]
if [[ $FILE_NAME =~ $prefix_regex ]]; then
  echo "File name starts with the expected prefix '$PREFIX'."
else
  echo "File name does not start with the expected prefix."
fi
```

### How to Run

```bash
./script_name.sh report_2023.txt report_

bash name.sh
```
```


Certainly! Here are the separate snippets for `grep`, `find`, and `cron` jobs in Markdown format:

---

### `grep` Command

**Basic Examples:**

```bash
# Search for the word "CDAC" in the file hello.txt
grep CDAC hello.txt

# List files whose name contains "ct"
ls | grep ct

# List files whose name starts with "Pi"
ls | grep ^Pi

# List files whose name ends with "es"
ls | grep es$
```

**Examples with a Sample File: `GreatGatsby.txt`**

```bash
# Search for the word "Gatsby"
grep "Gatsby" GreatGatsby.txt

# Display the first few lines of the file
head "GreatGatsby.txt"

# Search for "if" in a case-insensitive manner
grep "if" GreatGatsby.txt -i

# Search for the word "ate"
grep "ate" GreatGatsby.txt

# Search for the whole word "ate" only
grep "ate" GreatGatsby.txt -w

# Count occurrences of "Gatsby" ignoring case
grep "Gatsby" GreatGatsby.txt -ic

# Display line numbers with the match
grep "Gatsby" GreatGatsby.txt -n
```

**More Examples:**

```bash
# Find lines containing both "gatsby" and "it"
grep "gatsby it" greatgatsby.txt

# Find lines containing either "gatsby" or "it"
grep "gatsby\|it" greatgatsby.txt

# Find lines starting with "The"
grep ^The greatgatsby.txt

# Find lines ending with "."
grep ".$" greatgatsby.txt

# Find lines containing "gatsby" (case-insensitive)
grep -i "gatsby" greatgatsby.txt

# Find lines containing at least one digit
grep -E "[0-9]" greatgatsby.txt

# Find lines containing words with at least 6 characters
grep -E "\w{6,}" greatgatsby.txt

# Count the number of lines containing "gatsby"
grep -c "gatsby" greatgatsby.txt

# Find lines containing "gatsby" and print the line number
grep -n "gatsby" greatgatsby.txt

# Find lines not containing "gatsby"
grep -v "gatsby" greatgatsby.txt

# Find lines containing "gatsby" and "Fitzgerald", but not "Nick"
grep -E "gatsby.*Fitzgerald" greatgatsby.txt | grep -v "Nick"

# Find lines containing "gatsby" and print the matching part
grep -o "gatsby" greatgatsby.txt

# Replace "gatsby" with "Great Gatsby" in all lines
sed 's/gatsby/Great Gatsby/g' greatgatsby.txt
```

**Recursive Search Using `grep`:**

```bash
# Search for the word "cdac" in all directories and subdirectories
grep cdac -r
```

---

### Regular Expressions (regex) with `grep`

**Basic Syntax:**

- **Match a single character (except newline):** `.`  
  Example: `p.T` (Matches `pet`, `pat`, `pot`, `pit`, etc.)

- **Matching a range of characters:** `[a-z]`, `[0-9]`  
  Example: `hpcsa-[0-9][0-9]` (Matches `hpcsa-23`, `hpcsa-24`, `hpcsa-25`, etc.)

- **Matching the beginning or end of a line:** `^` for beginning, `$` for end  
  Example: `^C-DAC` (Starts with `C-DAC`), `C-DAC$` (Ends with `C-DAC`)

- **Repeating characters:** `*`, `+`  
  Example: `ab*c` (Matches `ac`, `abc`, `abbc`, etc.), `ab+c` (Matches `abc`, `abbc`, but not `ac`)

- **Matching an exact number of times:** `{n}`  
  Example: `ab{2}c` (Matches `abbc` but not `abc` or `ac`)

- **Alternate matching:** `|`  
  Example: `(HPCSA|HPCAP)` (Matches either `HPCSA` or `HPCAP`)

- **Negation:** `[^\d]` (Matches any character that is not a digit)

**Anchors:**

```bash
# Start of a line
grep "^gatsby" "GreatGatsby.txt" -i

# End of a line
grep "out$" testfile.txt
```

**Character Classes:**

```bash
# Matches any single character a, b, or c
grep "[abc]" GreatGatsby.txt

# Matches any single character from a to z
grep "[a-z]" GreatGatsby.txt

# Matches any single digit
grep "[0-9]" GreatGatsby.txt
```

**More `grep` Examples:**

```bash
# Lines containing "Gatsby"
grep "Gatsby" greatgatsby.txt

# Lines starting with "The"
grep "^The" greatgatsby.txt

# Lines ending with "."
grep "\.$" greatgatsby.txt

# Lines containing "Gatsby" but not "West Egg"
grep "Gatsby" greatgatsby.txt | grep -v "West Egg"

# Count lines with "East"
grep -c "East" greatgatsby.txt

# Lines containing "y"
grep "y" greatgatsby.txt

# Lines containing "-" 
grep "-" greatgatsby.txt

# Lines with words of at least 8 characters
grep -E "\w{8,}" greatgatsby.txt

# Lines with uppercase followed by lowercase letters
grep -E "[A-Z][a-z]+" greatgatsby.txt

# Lines that do not contain the word "Gatsby"
grep -v "Gatsby" greatgatsby.txt

# Case-insensitive search for "Gatsby"
grep -i "Gatsby" greatgatsby.txt

# Print all words and remove duplicates
grep -oE "\w+" greatgatsby.txt | sort | uniq

# Lines with exactly 3 words
grep -E "\b\w+\b{3}" greatgatsby.txt

# Match whole words "green light"
grep -w "green light" greatgatsby.txt

# Lines starting with a digit
grep "^[0-9]" greatgatsby.txt

# Match date format
grep -E "[0-9]{4}-[0-1][0-9]-[0-3][0-9]" greatgatsby.txt

# First line with "Gatsby"
grep -n "Gatsby" greatgatsby.txt | head -n 1

# Lines with "party" within the first 50 lines
head -n 50 greatgatsby.txt | grep "party" | tail -n 10
```

---

### `find` Command

**Basic Usage:**

```bash
# Find a file named "one.txt"
find -name one.txt

# Find all files with a .txt extension
find -type f -name "*.txt"

# Find a file named "one.txt" recursively
find . -type f -name one.txt

# Find all files larger than 10KB
find -type f -size +10k

# Find files larger than 10KB and list their sizes
find -type f -size +10k -ls

# Find directories with permission 755
find -type d -perm 755 -ls
```

**Problem: Find and Display Files**

```bash
#!/bin/bash
read -p "Enter the file extension (e.g., txt, pdf): " file_extension

# Find files in the current directory
current_dir_files=$(find . -type f -name "*.$file_extension")

# Find files in the user's home directory
home_dir_files=$(find ~ -type f -name "*.$file_extension")

echo "Files in the current directory:"
echo "$current_dir_files"
echo "Files in your home directory:"
echo "$home_dir_files"
```

**Extended Problem: Create a Zip File**

```bash
#!/bin/bash
read -p "Enter the file extension (e.g., txt, pdf): " file_extension
archive_name="new.zip"

# Find files in the current directory
current_dir_files=$(find . -type f -name "*.$file_extension")

# Find files in the user's home directory
home_dir_files=$(find ~ -type f -name "*.$file_extension")

# Combine the file lists
all_files="$current_dir_files $home_dir_files"

# Check if any files were found
if [[ -z "$all_files" ]]; then
  echo "No files found with the extension '$file_extension'."
  exit 1
fi

# Create the archive using zip
zip -r "$archive_name" $all_files
echo "Created archive: $archive_name"

# Alternative: Create a tar archive
# tar -cf "$archive_name" $all_files
```

---

### Running as a Cron Job

**Cron** is a command-line utility to schedule jobs to run automatically.

**Schedule a Script to Run Every Hour:**

```bash
# Edit the crontab file
crontab -e

# Add this line to the crontab file
0 * * * * /path/to/your/script.sh
```

This line tells cron to run the script at the 0th minute of every hour, every day, every month, and every year.

---


Here's the information formatted in Markdown:

---

## Network Services (FTP, Telnet, etc.)

### FTP Concept

**FTP (File Transfer Protocol)**

- **Overview:**
  - One of the earliest Internet protocols for file transfers.
  - Facilitates downloading (server-to-client) or uploading (client-to-server) of files remotely.

- **Components:**
  - **FTP Server:** Hosts files that can be downloaded or can receive files from users.
  - **FTP Client:** Downloads files from an FTP server or uploads files to the FTP server.

### Setting Up FTP Server on Ubuntu (on VirtualBox)

**Step 1: Install vsftpd**

```bash
sudo apt install vsftpd
```

**Step 2: Start the FTP Server**

```bash
sudo systemctl start vsftpd
```

**Step 3: Create an FTP User**

```bash
sudo useradd -m testuser
sudo passwd testuser
```

**Step 4: Allow FTP Through the Firewall**

```bash
sudo ufw allow 20/tcp
sudo ufw allow 21/tcp
```

**Step 5: Connect to the FTP Server Locally**

```bash
sudo ftp <Ubuntu>
```

*(Replace `<Ubuntu>` with your virtual machine's hostname or IP address)*

---




Here's the information formatted in Markdown:

---

## Group

**Group**: A collection of users that helps manage access to files, directories, and other system resources.

### Example Groups:

- **DAC Group**: Alice, Bob
- **AI Group**: Carol, Dave
- **GuestLectures Group**: Alice, Carol
- **CampusCommittee Group**: Carol, Dave
- **ExtraCurricular Group**: Alice, Bob, Dave

**Note**: Groups are less significant now due to reduced shared machine usage. Every user has a primary group and possibly secondary groups, with the primary group listed in the `/etc/passwd` file.

### Group Management Commands:

- **Find Existing Groups:**

    ```bash
    groups
    ```

- **Create a New Group:**

    ```bash
    sudo groupadd marketing
    ```

- **Rename a Group:**

    ```bash
    sudo groupmod -n sales marketing
    ```

- **Remove a Group:**

    ```bash
    sudo groupdel sales
    ```

- **Add a User to a Group:**

    ```bash
    sudo usermod -aG marketing john
    ```

- **Remove a User from a Group:**

    ```bash
    sudo gpasswd -d john marketing
    ```

- **Find Groups and Their Members:**

    ```bash
    cat /etc/group | sort
    ```

- **Find Group Names of a User:**

    ```bash
    groups <username>
    ```

---

## File Inode

**Inode (Index Node)**: A data structure storing metadata about a file or directory, including:

- File type (Regular, Directory, Link)
- Permissions
- Owner and Group
- Size
- Timestamps
- Pointers to data blocks
- Link count

**Link**: Association between a file name and its inode.

- **Hard Link**: A directory entry pointing directly to the file's inode. Changes are reflected everywhere.
- **Soft Link (Symbolic Link)**: A file containing a reference to another file's path, not its inode. Becomes a "dangling" link if the original file is deleted.

### Examples:

- **Hard Link:**

    ```bash
    ln cdac.txt cdac_hard_link
    ```

- **Soft Link:**

    ```bash
    ln -s cdac.txt cdac_soft_link
    ```

---

## Network Services (FTP, Telnet, etc.)

### FTP Concept

**FTP (File Transfer Protocol)**: One of the earliest Internet protocols for file transfers.

- **Components:**
  - **FTP Server**: Hosts files for download or receives files from users.
  - **FTP Client**: Downloads files from or uploads files to the FTP server.

### Setting Up FTP Server on Ubuntu (VirtualBox)

**Step 1: Install vsftpd**

```bash
sudo apt install vsftpd
```

**Step 2: Start the FTP Server**

```bash
sudo systemctl start vsftpd
```

**Step 3: Create an FTP User**

```bash
sudo useradd -m testuser
sudo passwd testuser
```

**Step 4: Allow FTP Through the Firewall**

```bash
sudo ufw allow 20/tcp
sudo ufw allow 21/tcp
```

**Step 5: Connect to the FTP Server Locally**

```bash
sudo ftp <Ubuntu>
```

*(Replace `<Ubuntu>` with your virtual machine's name or IP address)*

### Accessing the FTP Server from Windows

1. Open Command Prompt and type `ftp`.
2. Use `ftp> open` and provide the IP address of the Ubuntu machine (e.g., `192.168.0.24`).
3. Login with `testuser` and the corresponding password.

**Commands:**

- **Check Directory:**

    ```bash
    ftp> pwd
    ftp> dir
    ```

- **Download a File:**

    ```bash
    ftp> get test.txt
    ```

---

### Telnet and SSH

**Telnet**: An Internet protocol allowing a client to connect to a remote server. It is somewhat obsolete.

**SSH (Secure Shell)**: A modern alternative to Telnet that provides secure remote access to a server.

### Setting Up Telnet Server on Ubuntu

**Step 1: Install Telnet Server**

```bash
sudo apt install telnetd -y
```

**Step 2: Check Telnet Status**

```bash
sudo systemctl status inetd
```

**Step 3: Configure Firewall for Telnet**

```bash
sudo ufw enable
sudo ufw allow 23
```

**Step 4: Test Telnet**

```bash
telnet 192.168.0.24
```

### Accessing Telnet from Windows

1. On Command Prompt, type `telnet`.
2. If Telnet is not installed, enable it via "Turn Windows Features On/Off".
3. Connect to the server with `o 192.168.0.24`.

### Setting Up SSH on Ubuntu Server

**Step 1: Install SSH Server**

```bash
sudo apt install openssh-server
```

**Step 2: Check SSH Status**

```bash
sudo systemctl status ssh
```

**Step 3: Configure Firewall for SSH**

```bash
sudo ufw allow ssh
```

**Step 4: Restart SSH Service**

```bash
sudo service ssh restart
```

### Access SSH Using PuTTY

1. Download and install PuTTY from [https://www.putty.org/](https://www.putty.org/).
2. Open PuTTY, enter the IP address (e.g., `192.168.0.24`), and connect.
3. Login with `testuser` and the corresponding password.

---






