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
```


### 11 pattern 2*i

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