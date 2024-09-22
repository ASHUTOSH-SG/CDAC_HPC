## Assignments


## 1. Project Directory Management

This README provides an overview of basic commands and scenarios for directory and file management in Linux.

## Basic Commands

### Create and Navigate Directories

1. **Create a directory named "projects"**:
   ```bash
   mkdir projects
   ```

2. **Create a subdirectory named "python"**:
   ```bash
   cd projects
   mkdir python
   ```

3. **Navigate to the "python" directory**:
   ```bash
   cd python
   ```

### Create and Edit Files

1. **Create a file named "hello.txt"**:
   ```bash
   touch hello.txt
   ```

2. **Edit the file using nano**:
   ```bash
   nano hello.txt
   ```
   Add the text: `Hello, world!`  
   Save and exit (`Ctrl + X`, then `Y`, and `Enter`).

### Permissions and Ownership

1. **Change file permissions**:
   ```bash
   chmod u+x hello.txt
   ```

2. **Check the permissions of the file**:
   ```bash
   ls -l hello.txt
   ```

## User Management

### Create a New User

1. **Create a new user named "newuser"**:
   ```bash
   sudo adduser newuser
   ```

2. **Switch to the new user**:
   ```bash
   su newuser
   ```

### Modify User Information

1. **Edit user information**:
   ```bash
   sudo usermod -c "Gaurav" newuser
   sudo usermod -g sudo newuser
   ```

## Advanced Commands

### Copy and Move Files and Directories

1. **Copy the "hello.txt" file to a new directory named "backup"**:
   ```bash
   mkdir backup
   cp hello.txt backup
   ```

2. **Move the "backup" directory to another location**:
   ```bash
   mv backup /home/projects
   ```

### Find Files and Directories

1. **Find all files with a ".txt" extension**:
   ```bash
   find . -type f -name "*.txt"
   ```

2. **Find files modified within the last 24 hours**:
   ```bash
   find . -type f -mtime -1
   ```

## Scenario 1: File Management

1. **Create a new directory named "my_project"**:
   ```bash
   mkdir my_project
   cd my_project
   ```

2. **Create a text file named "README.md"**:
   ```bash
   touch README.md
   ```

3. **Add content to "README.md"**:
   ```bash
   nano README.md
   ```

4. **Copy "README.md" to a "backup" directory**:
   ```bash
   mkdir backup
   cp README.md backup
   ```

5. **Move the "backup" directory to a different location**:
   ```bash
   mv backup /path/to/new/location
   ```

6. **Delete the original "README.md" file**:
   ```bash
   rm README.md
   ```

7. **Recover the deleted "README.md" file**:
   ```bash
   cp /path/to/new/location/backup/README.md my_project
   ```

## Scenario 2: Working with Permissions

1. **Check current permissions of "README.md"**:
   ```bash
   ls -l README.md
   ```

2. **Make the file executable for the owner only**:
   ```bash
   chmod +x README.md
   ```

3. **Verify that you can execute the file**:
   ```bash
   ./README.md
   ```

4. **Make the file readable and writable for the group and others**:
   ```bash
   chmod 664 README.md
   ```

5. **Check the permissions again**:
   ```bash
   ls -l README.md
   ```

## Scenario 3: Understanding Relative and Absolute Paths

1. **Create a directory structure**:
   ```bash
   mkdir -p structure/mobile/{oneplus,apple} structure/laptop/{hp,dell,mac}
   ```

2. **Navigate to a specific directory using an absolute path**:
   ```bash
   cd /home/structure/laptop/hp
   ```

3. **Navigate using a relative path**:
   ```bash
   cd ../../laptop/hp
   ```

4. **Create a file and reference it**:
   ```bash
   touch ht.txt
   cat /home/structure/laptop/hp/ht.txt
   cat ./ht.txt
   ```

## Scenario 4: Using Wildcards

1. **Find all files with a ".txt" extension**:
   ```bash
   find . -type f -name "*.txt"
   ```

2. **Find all files modified within the last 24 hours**:
   ```bash
   find . -type f -mtime -1
   ```

3. **Delete all files with a ".tmp" extension**:
   ```bash
   find . -type f -name "*.tmp" -delete
   ```



## A bank has the following types of investment options:
1. Current account: No interest is paid.
2. Savings account:
For Balance < 1 lakh rupees, interest = 3.5% PA
For Balance between 1-5 lakh rupees, interest = 6% PA over the
balance of Rs 1 lakh
For Balance > 5 lakh rupees, interest = 7% PA over the balance of Rs
5 lakh

3. Deposit account (Always consider Time = 3 years, Rate = 10%)
(a) Simple interest deposit = (Principal * Rate * Time) / 100
Total Amount (with simple interest) = Principal + Simple Interest
(b) Compound interest Total Amount = Principal * (1 + (Rate /
100))^Time

Accept account type and opening balance from the user.
If it is savings account, show value at the end of the year if the
same balance is maintained throughout the year.
If it is deposit account, accept whether it is simple interest
deposit or compound interest deposit and show the final balance at
the end of the year.



```
#!/bin/bash

# Function to calculate savings account balance with interest
# Interest rules:
# - 3.5% for balance < ₹1,00,000
# - 6% for balance between ₹1,00,000 and ₹5,00,000 (on amount above ₹1,00,000)
# - 7% for balance > ₹5,00,000 (on amount above ₹5,00,000)
calculate_savings_balance() {
    balance=$1
    # Check if balance is less than ₹1,00,000
    if (( $(echo "$balance < 100000" | bc -l) )); then
        # 3.5% interest for balance < ₹1,00,000
        interest=$(echo "scale=2; $balance * 3.5 / 100" | bc)
    # Check if balance is between ₹1,00,000 and ₹5,00,000
    elif (( $(echo "$balance <= 500000" | bc -l) )); then
        # 6% interest for balance over ₹1,00,000 and 3.5% for first ₹1,00,000
        interest=$(echo "scale=2; (6 / 100 * ($balance - 100000)) + (3.5 / 100 * 100000)" | bc)
    else
        # 7% interest for balance over ₹5,00,000, 6% for ₹1,00,000-₹5,00,000, 3.5% for first ₹1,00,000
        interest=$(echo "scale=2; (7 / 100 * ($balance - 500000)) + (6 / 100 * 400000) + (3.5 / 100 * 100000)" | bc)
    fi
    # Calculate final balance by adding interest
    final_balance=$(echo "scale=2; $balance + $interest" | bc)
    echo "Final Balance after 1 year: ₹$final_balance"
}

# Function to calculate deposit account balance
# Takes deposit type as input: "simple" or "compound"
# Assumes fixed rate of 10% and time = 3 years for deposit accounts
calculate_deposit_balance() {
    principal=$1
    rate=10
    time=3
    interest_type=$2
    
    # For simple interest, use the formula: (P * R * T) / 100
    if [ "$interest_type" == "simple" ]; then
        simple_interest=$(echo "scale=2; ($principal * $rate * $time) / 100" | bc)
        total_amount=$(echo "scale=2; $principal + $simple_interest" | bc)
    # For compound interest, use the formula: P * (1 + R/100)^T
    elif [ "$interest_type" == "compound" ]; then
        total_amount=$(echo "scale=2; $principal * (1 + $rate / 100)^$time" | bc -l)
    fi
    echo "Final Balance after $time years: ₹$total_amount"
}

# Prompt the user to enter account type (savings or deposit)
read -p "Enter account type (savings/deposit): " account_type

# Prompt the user to enter the opening balance (initial amount)
read -p "Enter opening balance: " opening_balance

# If account type is savings, calculate savings balance
if [ "$account_type" == "savings" ]; then
    calculate_savings_balance $opening_balance

# If account type is deposit, ask for deposit type (simple or compound) and calculate balance
elif [ "$account_type" == "deposit" ]; then
    read -p "Enter deposit type (simple/compound): " deposit_type
    calculate_deposit_balance $opening_balance $deposit_type

# If account type is invalid, print an error message
else
    echo "Invalid account type!"
fi

```
## extra lab session --------------------------------------------------------


## 1 check whether a number is even or odd is correct. 
1. The `read -p "Enter a number : " n` command takes input from the user and assigns it to the variable `n`.
2. The modulus operation `rem=$(( $n % 2 ))` computes the remainder when `n` is divided by 2.
3. If the remainder is zero (`[ $rem -eq 0 ]`), the number is even; otherwise, it is odd.

Here's your script for easy reference:

```bash
#!/bin/bash

read -p "Enter a number : " n

rem=$(( $n % 2 ))
# Other syntaxes
# let "rem = n % 2"
# rem=$(expr $n % 2)
# rem=$(echo "$n % 2" | bc)

if [ $rem -eq 0 ]
then
    echo "$n is an even number"
else
    echo "$n is an odd number"
fi
```

## 2 maximum of three numbers

```bash
#!/bin/bash
echo "Enter Num1:"
read num1
echo "Enter Num2:"
read num2
echo "Enter Num3:"
read num3
# Alternatively: read -p "Enter Num1 Num2 Num3: " num1 num2 num3

if [ $num1 -gt $num2 ] && [ $num1 -gt $num3 ]; then
    echo "The maximum number is: $num1"
elif [ $num2 -gt $num1 ] && [ $num2 -gt $num3 ]; then
    echo "The maximum number is: $num2"
else
    echo "The maximum number is: $num3"
fi
```

## 3 It checks whether two input strings are equal
```
#!/bin/bash

# Shell script to check whether two input strings are equal

# take user input
echo "Enter string a: "
read a

echo "Enter string b: "
read b

# check equality of input
if [ "$a" == "$b" ]; then
    # if equal, print equal
    echo "Strings are equal."
else
    # if not equal
    echo "Strings are not equal."
fi

```
## 4 average marks
```
#!/bin/bash

# Take input for marks in three subjects
read -p "Enter marks in subject 1: " marks1
read -p "Enter marks in subject 2: " marks2
read -p "Enter marks in subject 3: " marks3

# Calculate total marks
total=$(( marks1 + marks2 + marks3 ))

# Display total marks
echo "Total marks: $total"

# Calculate average marks with 4 decimal places
avg=$( echo "scale=2; $total / 3" | bc )

# Display average marks
echo "Average marks: $avg"

```
### 5 RegEx: Check if a Filename Starts With a Specific String

```
#!/bin/bash

# Define file name and prefix (modify as needed)
FILE_NAME="report_2023.txt"
PREFIX="report_"

# Regex pattern for checking the prefix
prefix_regex="^$PREFIX"

# Check if filename starts with the prefix using [[ ]]
if [[ $FILE_NAME =~ $prefix_regex ]]; then
  echo "File name starts with the expected prefix '$PREFIX'."
else
  echo "File name does not start with the expected prefix."
fi


```

## 6 create a calculator

```
#!/bin/bash

# Simple calculator
echo "Select operation:"
echo "1. Addition"
echo "2. Subtraction"
echo "3. Multiplication"
echo "4. Division"
echo "5. Square"
echo "6. Cube"

# Read the user's choice
read -p "Enter your choice (1-6): " choice

# Perform the operation based on the user's choice
case $choice in
    1) echo "Enter two numbers: "; read a b; echo "Result: $((a + b))";;  # Addition
    2) echo "Enter two numbers: "; read a b; echo "Result: $((a - b))";;  # Subtraction
    3) echo "Enter two numbers: "; read a b; echo "Result: $((a * b))";;  # Multiplication
    4) echo "Enter two numbers: "; read a b; echo "Result: $((a / b))";;  # Division
    5) echo "Enter a number: "; read a; echo "Square: $((a * a))";;       # Square
    6) echo "Enter a number: "; read a; echo "Cube: $((a * a * a))";;     # Cube
    *) echo "Invalid choice";;
esac



```
### 7 Fibonacci
```
read -p "Enter the number " number

a=0
b=1

for ((i=1; i<=number; i++));
do
    echo -n " $a " 
    fib=$((a+b))
    a=$b
    b=$fib
done
```
### 8. Prime numbers
```
#!/bin/bash

# Read user input
read -p "Enter the range for print the prime number:" num
# Loop through numbers from 2 to the entered number
for (( n=2; n<=num; n++ ))
do
    # Check if the number is divisible by any number from 2 to n-1
    for (( i=2; i<n; i++ ))
    do
        if (( n % i == 0 )); then
            break  # Not a prime, exit the inner loop
        fi
    done

    # If the loop completes, i will be equal to n, meaning n is prime
    if (( i == n )); then
        echo "$n"
    fi
done
```

### 9. accept 10 numbers from user, and find addition of all numbers which are divisible by 4.

```
#!/bin/bash

read -p "enter the number with space " -a numbers
sum=0
for num in "${numbers[@]}";do
        if ((num%4==0));then
                sum=$((sum+num))
        fi

done
echo "$sum"

```

### 10 pattern normal
1
12
123
1234
12345
```
```
read -p "Enter the number: " number
for ((i=1; i<=$number; i++)); 
do

    for ((j=1;j<=i;j++));
    do
    echo -n "$j"
    done
    echo
done



## 11 pattern 2*i

```
1
123
12345
1234567
123456789
```
```

#1/bin/bash

read -p "enter line of triangle" l

if [[ $l -eq 0 ]]; then
        echo "enter valid number :  "
else
        for (( i=1; i<=$l; i++ )) do
               # echo $i
               # for (( j=i; j<=$l; j++)) do
               #       echo -n " "
               #done
               for (( k=1; k<=(2*i-1); k++)) do
                       echo -n "$k"
               done
               echo
        done

fi

```



## 12 bank entry 
a. Write a shell script to accept branch id, branch name, and branch address and store these details at the end of the file branchdetails.txt.
Note : before running script, create branchdetails.txt and save following lines in the file, the shell script should append contents in this file, these contents are in the following format:
branch id:branch name:branch address

100:idbi bank,pune: Bajirao road
200:icicibank,Mumbai:varali

```
#!/bin/bash

read -p "enter the branch id: " branchid
read -p "enter the branch name: " branchname
read -p "enter the branch add: " branchadd


echo "$branchid:$branchname:$branchadd" >> branchdetails.txt

cat branchdetails.txt

```

## 13 make dir delete dir change permission
## if else

```
#!/bin/bash

# Display menu and get user input
read -p "1. Create directory 2. Delete file 3. Change permissions 4. Exit: " choice

# Create directory
if [[ $choice -eq 1 ]]; then
    read -p "Enter the name of the directory: " dir

    if [[ -d "$dir" ]]; then
        echo "Directory '$dir' already exists."
    else
        mkdir "$dir"
        echo "Directory '$dir' created."
    fi
fi

# Delete file
if [[ $choice -eq 2 ]]; then
    read -p "Enter the name of the file to delete: " file

    if [[ -f "$file" ]]; then
        rm "$file"
        echo "File '$file' deleted."
    else
        echo "File '$file' not found."
    fi
fi

# Change file permissions
if [[ $choice -eq 3 ]]; then
    read -p "Enter the name of the file to change the permissions: " file

    if [[ -f "$file" ]]; then
        chmod 777 "$file"
        echo "Permissions of '$file' changed to 777."
    else
        echo "File '$file' not found."
    fi
fi

# Exit option
if [[ $choice -eq 4 ]]; then
    echo "Thank you!"
fi

# Handle invalid input
if [[ $choice -lt 1 || $choice -gt 4 ]]; then
    echo "Invalid option. Please enter a number between 1 and 4."
fi

```

## in case
```
#!/bin/bash
# Use case statement to handle different choices
case $choice in
    1)  # Create directory
        read -p "Enter the name of the directory: " dir
        if [[ -d "$dir" ]]; then
            echo "Directory '$dir' already exists."
        else
            mkdir "$dir"
            echo "Directory '$dir' created."
        fi
        ;;
    
    2)  # Delete file
        read -p "Enter the name of the file to delete: " file
        if [[ -f "$file" ]]; then
            rm "$file"
            echo "File '$file' deleted."
        else
            echo "File '$file' not found."
        fi
        ;;
    
    3)  # Change file permissions
        read -p "Enter the name of the file to change the permissions: " file
        if [[ -f "$file" ]]; then
            chmod 777 "$file"
            echo "Permissions of '$file' changed to 777."
        else
            echo "File '$file' not found."
        fi
        ;;
    
    4)  # Exit
        echo "Thank you!"
        ;;
    
    *)  # Handle invalid input
        echo "Invalid option. Please enter a number between 1 and 4."
        ;;
esac

```

## Revised Script Using Functions and a while Loop:

```
#!/bin/bash

# Function to create a directory
create_directory() {
    read -p "Enter the name of the directory: " dir
    if [[ -d "$dir" ]]; then
        echo "Directory '$dir' already exists."
    else
        mkdir "$dir"
        echo "Directory '$dir' created."
    fi
}

# Function to delete a file
delete_file() {
    read -p "Enter the name of the file to delete: " file
    if [[ -f "$file" ]]; then
        rm "$file"
        echo "File '$file' deleted."
    else
        echo "File '$file' not found."
    fi
}

# Function to change file permissions
change_permissions() {
    read -p "Enter the name of the file to change the permissions: " file
    if [[ -f "$file" ]]; then
        chmod 777 "$file"
        echo "Permissions of '$file' changed to 777."
    else
        echo "File '$file' not found."
    fi
}

# Function to display the menu and get user input
display_menu() {
    echo "1. Create directory"
    echo "2. Delete file"
    echo "3. Change permissions"
    echo "4. Exit"
}

# Main loop
while true; do
    display_menu
    read -p "Choose an option: " choice

    case $choice in
        1)  # Call function to create a directory
            create_directory
            ;;
        2)  # Call function to delete a file
            delete_file
            ;;
        3)  # Call function to change permissions
            change_permissions
            ;;
        4)  # Exit the loop and script
            echo "Thank you! Exiting..."
            break
            ;;
        *)  # Handle invalid input
            echo "Invalid option. Please enter a number between 1 and 4."
            ;;
    esac

    # Add a small pause before displaying the menu again
    echo ""
done

```

## 14 checks each number to see if it's divisible by 4, and sums those that are.

```
#!/bin/bash

# Prompt the user to enter numbers separated by space
read -p "Enter numbers separated by space: " -a numbers

sum=0  # Initialize sum to 0

# Loop through the array of numbers
for num in "${numbers[@]}"; do
    if (( num % 4 == 0 )); then  # Check if the number is divisible by 4
        sum=$(( sum + num ))      # Add the number to the sum if it's divisible by 4
    fi
done

# Print the final sum
echo "Sum of numbers divisible by 4: $sum"

```

## 15 Write a bash script to print a triangle pattern based on user input.

The script should ask the user for the number of lines (height) of the triangle.
If the user enters a value of 0, the script should prompt them to "enter a valid number".
Otherwise, the script should print a triangle pattern where each row contains increasing numbers starting from 1 up to (2*i-1) for the ith row.


```
#!/bin/bash

# Prompt the user to enter the number of lines for the triangle
read -p "Enter the number of lines for the triangle: " l

# Check if the input is 0 or less, prompt for a valid number
if [[ $l -le 0 ]]; then
    echo "Please enter a valid number greater than 0."
else
    # Loop to print the triangle pattern
    for (( i=1; i<=$l; i++ )) do
        # Inner loop to print the numbers in each row
        for (( k=1; k<=(2*i-1); k++ )) do
            echo -n "$k"
        done
        # Move to the next line after each row
        echo
    done
fi


```

## 16

```
#!/bin/bash

read -p "select your choice
	1. create n users
	2. List contents of .dat in current folder
	3. exit
:" choice

if [[ $choice -eq 1 ]]; then

        read -p "enter the numbers of user you want" n
	if [ $n -eq 0 ]; then
		echo "enter valid number"

	else
		for (( i=0; i<=n; i++)); do
			user="user$i"
			sudo useradd $user
			echo "user created $i"
		done
	fi
fi


if [[ $choice -eq 2 ]]; then
	read -p "enter the name of dir : " dir
        if [[ -d  $dir  ]]; then
	     ls *.dat
	     cat *.dat

        else
        echo "not exist"
        fi
fi

if [[ $choice -eq 3 ]]; then

echo "thank you"



fi



```

## 17 Write a bash script that lists files based on their extension using a case statement

```
#!/bin/bash

read -p "Enter file extension (e.g., .txt, .sh, .log): " ext

case $ext in
  ".txt" | ".sh" | ".log")
    echo "Listing all $ext files"
    ls *$ext
    ;;
  *)
    echo "Unsupported file extension"
    ;;
esac


```
## 18 check internet question working

```
#!/bin/bash 
echo "Checking internet connection..."
ping  8.8.8.8
if [[ $? -eq 0 ]]; then 
	echo "Connection successful."
else 
	echo "Connection fails, Please check internet connection"
fi
```

## 19  The script monitors the disk usage of the /home directory and alerts the user if the usage exceeds 80%. It runs indefinitely, checking every 5 seconds

```
#!/bin/bash

# Set the directory to monitor
DIRECTORY="/home"

# Start an infinite loop to continuously check disk usage
while true; do
    # Get the disk usage percentage for the specified directory
    USAGE=$(df "$DIRECTORY" | awk 'NR==2 {print $5}' | sed 's/%//')

    # Print the current disk usage
    echo "Disk usage in $DIRECTORY: $USAGE%"

    # Check if the usage exceeds 80%
    if [ "$USAGE" -gt 80 ]; then
        # Print a warning message if usage is over 80%
        echo "Warning: Disk usage has exceeded 80%!"
    fi

    # Pause for 5 seconds before the next check
    sleep 5
done

```

## 20   extra ------------------------------

### 1. Script to Retrieve and Print the IP Address of a Specified Ethernet Interface

```bash
#!/bin/bash

# Specify the Ethernet interface (e.g., eth0)
interface="eth0"

# Retrieve the IP address of the specified interface
ip_address=$(ip addr show "$interface" | grep 'inet ' | awk '{print $2}' | cut -d'/' -f1)

# Print the IP address
if [ -n "$ip_address" ]; then
    echo "The IP address of $interface is: $ip_address"
else
    echo "$interface does not have an IP address assigned."
fi
```

### 2. Script to Check if a Specified Ethernet Interface is Up or Down

```bash
#!/bin/bash

# Specify the Ethernet interface (e.g., eth0)
interface="eth0"

# Check the status of the interface
if ip link show "$interface" | grep -q "state UP"; then
    echo "$interface is up."
else
    echo "$interface is down."
fi
```

### 3. Script to List All Ethernet Interfaces and Their Current IP Addresses

```bash
#!/bin/bash

# List all Ethernet interfaces
for interface in $(ip link show | awk -F': ' '{print $2}' | grep '^[a-z]'); do
    # Retrieve the IP address of each interface
    ip_address=$(ip addr show "$interface" | grep 'inet ' | awk '{print $2}' | cut -d'/' -f1)
    
    # Print the interface and its IP address
    if [ -n "$ip_address" ]; then
        echo "$interface: $ip_address"
    else
        echo "$interface: No IP address assigned."
    fi
done
```

### How to Use the Scripts

1. **Save Each Script**: Save the above scripts into separate files (e.g., `get_ip.sh`, `check_interface_status.sh`, `list_interfaces.sh`).

2. **Make the Scripts Executable**:
   ```bash
   chmod +x get_ip.sh check_interface_status.sh list_interfaces.sh
   ```

3. **Run the Scripts**:
   ```bash
   ./get_ip.sh            # To get the IP address of eth0
   ./check_interface_status.sh  # To check the status of eth0
   ./list_interfaces.sh    # To list all Ethernet interfaces and their IP addresses
   ```

### Notes:
- Ensure you replace `eth0` in the scripts with the actual name of your Ethernet interface if it differs.
- The scripts assume that the `ip` command is available on your system. If it is not, you may need to install the appropriate networking tools.

