---

### Lab 1: Executing Basic Commands

1. **Question:** How do you display the current working directory?
   ```bash
   pwd
   ```
   **Explanation:** This command outputs the path of the current directory.

2. **Question:** How do you display the path to your HOME directory?
   ```bash
   echo $HOME
   ```
   **Explanation:** This prints the path of the home directory for the current user.

3. **Question:** How can you display your login name?
   ```bash
   whoami
   ```
   **Explanation:** This command shows the username of the currently logged-in user.

4. **Question:** How do you display hidden files in the current directory?
   ```bash
   ls -a
   ```
   **Explanation:** The `-a` flag lists all files, including hidden ones (those starting with a dot).

5. **Question:** How do you list all files in your home directory?
   ```bash
   ls ~
   ```
   **Explanation:** This lists all the files in the home directory.

6. **Question:** How do you display files in long listing format?
   ```bash
   ls -l
   ```
   **Explanation:** The `-l` option provides detailed information about files.

7. **Question:** How can you list files beginning with "chap" followed by any number or lowercase letter?
   ```bash
   ls chap[a-z0-9]*
   ```
   **Explanation:** This uses pattern matching to find files that start with "chap".

8. **Question:** How do you create a directory called `C_prog` in your home directory?
   ```bash
   mkdir ~/C_prog
   ```
   **Explanation:** This command creates a new directory in the specified location.

9. **Question:** How do you create directories named `newdir` and `newdirectory` in your home directory?
   ```bash
   mkdir ~/newdir ~/newdirectory
   ```
   **Explanation:** This creates both directories simultaneously.

10. **Question:** How do you list all files and their contents in subdirectories of your home directory?
    ```bash
    ls -R ~
    ```
    **Explanation:** The `-R` option lists files recursively.

11. **Question:** How do you remove the `newdirectory` from your working directory?
    ```bash
    rmdir ~/newdirectory
    ```
    **Explanation:** This removes an empty directory.

12. **Question:** How do you create a directory called `temp` under your home directory?
    ```bash
    mkdir ~/temp
    ```
    **Explanation:** This creates a new directory named `temp`.

13. **Question:** How do you remove `newdir` and verify its removal?
    ```bash
    rmdir ~/newdir
    ls ~
    ```
    **Explanation:** This removes the directory and lists files to confirm.

14. **Question:** How do you create another directory called `directorynew` under `temp`?
    ```bash
    mkdir ~/temp/directorynew
    ```
    **Explanation:** This creates a nested directory.

15. **Question:** How do you change to your home directory?
    ```bash
    cd ~
    ```
    **Explanation:** This navigates to the home directory.

16. **Question:** How do you change to `directorynew` using relative and absolute paths?
    ```bash
    cd temp/directorynew
    cd ~/temp/directorynew
    ```
    **Explanation:** Both commands change to the same directory using different path types.

17. **Question:** How do you remove the `C_prog` directory from your home directory?
    ```bash
    rmdir ~/C_prog
    ```
    **Explanation:** This command deletes the specified directory.

18. **Question:** How do you change to the `/etc` directory and display its files?
    ```bash
    cd /etc
    ls
    ```
    **Explanation:** This changes to `/etc` and lists its contents.

19. **Question:** How do you list all files starting with a dot in the `/usr/bin` directory?
    ```bash
    ls /usr/bin/.*
    ```
    **Explanation:** This lists all hidden files in the specified directory.

20. **Question:** How do you create a file named `first.unix` with specific contents?
    ```bash
    echo -e "Hi! Good Morning everybody.\nWelcome to the First exercise on UNIX. Hope you enjoy doing the assignments." > first.unix
    ```
    **Explanation:** This command creates a file and writes the specified text into it.

21. **Question:** How do you copy `first.unix` to `first.unics`?
    ```bash
    cp first.unix first.unics
    ```
    **Explanation:** This duplicates the file under a new name.

22. **Question:** How do you list the contents of `first.unix` and `first.unics` with a single command?
    ```bash
    cat first.unix first.unics
    ```
    **Explanation:** This concatenates the output of both files.

23. **Question:** How do you create a new directory under `temp`?
    ```bash
    mkdir ~/temp/newdir
    ```
    **Explanation:** This creates another directory within `temp`.

24. **Question:** How do you copy all files to the new directory under `temp`?
    ```bash
    cp ~/* ~/temp/newdir/
    ```
    **Explanation:** This copies all files from the home directory to the specified path.

25. **Question:** How do you move `first.unix` to `temp` as `second.unix`?
    ```bash
    mv first.unix ~/temp/second.unix
    ```
    **Explanation:** This moves and renames the file.

26. **Question:** How do you remove the file `first.unics` from the home directory?
    ```bash
    rm first.unics
    ```
    **Explanation:** This deletes the specified file.

27. **Question:** What happens when you issue `rm *` in the `temp` directory?
    ```bash
    cd ~/temp
    rm *
    ```
    **Observation:** All files in `temp` will be removed without confirmation.

28. **Question:** How do you move files ending with `a`, `c`, and `o` to the HOME directory?
    ```bash
    mv *.[aco] ~/
    ```
    **Explanation:** This moves matching files to the home directory.

29. **Question:** How do you copy files ending with `UNIX` to the `temp` directory?
    ```bash
    cp *UNIX ~/temp/
    ```
    **Explanation:** This copies all matching files to the specified directory.

30. **Question:** How do you remove all files and the `temp` directory itself?
    ```bash
    rm -r ~/temp
    ```
    **Explanation:** This recursively deletes the directory and its contents.

31. **Question:** What happens when you use `cp` or `mv` with invalid arguments?
    **Observation:** The system displays an error indicating incorrect usage.

32. **Question:** How do you create a file named `friends` with specific data?
    ```bash
    cat > friends
    ```
    Then enter:
    ```
    Madhu	6966456	09/07/68
    Jamil	2345215	08/09/67
    Ajay	5546785	01/04/66
    Mano	7820022	09/07/68
    David	8281292	09/09/60
    Simmi	7864563	12/12/70
    Navin	2224311	30/05/68
    ```
    **Explanation:** This creates the file and allows data entry.

33. **Question:** How do you display the contents of the `friends` file?
    ```bash
    cat friends
    ```
    **Explanation:** This prints the contents of the specified file.

34. **Question:** How do you copy contents from `friends` to `newfriend` without using `cp`?
    ```bash
    cat friends > newfriend
    ```
    **Explanation:** This command redirects the output to a new file.

35. **Question:** How do you display contents of both `friends` and `newfriend` in a single command?
    ```bash
    cat friends newfriend
    ```
    **Explanation:** This concatenates both file outputs.

36. **Question:** How do you find all users currently working on the system and store it in `users`?
    ```bash
    who > users
    ```
    **Explanation:** This saves the output of the `who` command.

37. **Question:** How do you append the contents of `friends` to `users`?
    ```bash
    cat friends >> users
    ```
    **Explanation:** This appends the file contents.

38. **Question:** How do you display the current date and time?
    ```bash
    date
    ```
    **Observation:** Displays the current date and time in the system’s format.

39. **Question:** How do you display the calendar for your birth month and year?
    ```bash
    cal 09 1968
    ```
    **Explanation:** This shows the specified month and year.

40. **Question:** What happens when you run the following `date` commands?
    ```bash
    date "+%"
    date "+%m"
    date "+%D"
    ```
    **Observation:** The commands return specific parts of the date.

---

### Viewing the File System and Granting/Removing Permissions

1.

 **Question:** How do you give execute permission for the user for a file `chap1`?
   ```bash
   chmod u+x chap1
   ```
   **Explanation:** This grants execute permission to the user.

2. **Question:** How do you give execute permission for user, group, and others for a file `add.c`?
   ```bash
   chmod a+x add.c
   ```
   **Explanation:** This applies execute permission to everyone.

3. **Question:** How do you remove execute permission from user and give read permission to group and others for a file `aa.c`?
   ```bash
   chmod u-x,g+r,o+r aa.c
   ```
   **Explanation:** This modifies permissions accordingly.

4. **Question:** How do you give execute permission for users for multiple files in one command?
   ```bash
   chmod u+x a.c kk.c nato myfile
   ```
   **Explanation:** This applies execute permission to all listed files.

5. **Question:** How do you check system directories?
   ```bash
   ls /
   ```
   **Explanation:** This lists the contents of the root directory.

---

### Lab 2: Using Pipes and Filters

1. **Question:** How do you redirect the content of the help document `ls` into a file called `lsdoc`?
   ```bash
   man ls > lsdoc
   ```
   **Explanation:** This saves the man page of the `ls` command into a file.

2. **Question:** How do you display the content of `lsdoc` page-wise?
   ```bash
   less lsdoc
   ```
   **Explanation:** This allows you to view the file one page at a time.

3. **Question:** How do you display only the first 4 lines of the `lsdoc` file?
   ```bash
   head -n 4 lsdoc
   ```
   **Explanation:** This outputs the first four lines of the file.

4. **Question:** How do you display only the last 7 lines of the file `lsdoc`?
   ```bash
   tail -n 7 lsdoc
   ```
   **Explanation:** This shows the last seven lines of the file.

5. **Question:** How do you remove the file `lsdoc`?
   ```bash
   rm lsdoc
   ```
   **Explanation:** This deletes the specified file.

6. **Question:** How can you find how many birthday parties will be held from `friends`?
   ```bash
   cut -f 3 friends | sort | uniq -c
   ```
   **Explanation:** This counts unique birthdays.

7. **Question:** How do you display lines starting with "Ma" in the file `friends`?
   ```bash
   grep "^Ma" friends
   ```
   **Explanation:** This searches for lines beginning with "Ma".

8. **Question:** How do you display lines starting with "Ma" and ending with "i" or "id"?
   ```bash
   grep "^Ma.*[i|id]$" friends
   ```
   **Explanation:** This matches lines based on both conditions.

9. **Question:** How do you print all files and directory files from the current directory with their paths?
   ```bash
   find "$(pwd)" -type f
   ```
   **Explanation:** This lists all files in the current directory and subdirectories.

10. **Question:** How do you print only the directory files?
    ```bash
    find "$(pwd)" -type d
    ```
    **Explanation:** This lists only directories.

11. **Question:** How do you display files starting with "chap" along with their paths?
    ```bash
    find "$(pwd)" -name "chap*"
    ```
    **Explanation:** This searches for files that match the pattern.

12. **Question:** How do you sort the file `friends` in ascending order of names?
    ```bash
    sort friends
    ```
    **Explanation:** This sorts the file alphabetically by name.

13. **Question:** How do you display the contents of the file `friends` in uppercase letters?
    ```bash
    tr '[:lower:]' '[:upper:]' < friends
    ```
    **Explanation:** This converts the text to uppercase.

14. **Question:** How do you store the contents of your home directory in a file called `dir`?
    ```bash
    ls ~ > dir
    ```
    **Explanation:** This saves the list of files in the home directory.

15. **Question:** How do you display file permissions and names from the `dir` file?
    ```bash
    ls -l ~ | awk '{print $1, $9}' > dir
    ```
    **Explanation:** This extracts specific columns.

16. **Question:** How do you store only file names from the `dir` file?
    ```bash
    ls ~ > files
    ```
    **Explanation:** This captures just the filenames.

17. **Question:** How do you store only permissions of files in a file called `perms`?
    ```bash
    ls -l ~ | awk '{print $1}' > perms
    ```
    **Explanation:** This extracts the permissions.

18. **Question:** How do you store only file sizes in a file called `sizes`?
    ```bash
    ls -l ~ | awk '{print $5}' > sizes
    ```
    **Explanation:** This captures file sizes.

19. **Question:** How do you display file names, sizes, and permissions in that order?
    ```bash
    ls -l ~ | awk '{print $9, $5, $1}'
    ```
    **Explanation:** This outputs the specified columns.

20. **Question:** How do you display the number of users working on the system?
    ```bash
    who | wc -l
    ```
    **Explanation:** This counts the number of lines in the output of `who`.

21. **Question:** How do you find the smallest file in your directory?
    ```bash
    ls -S | tail -n 1
    ```
    **Explanation:** This sorts files by size and shows the smallest.

22. **Question:** How do you display the total number of lines in the `friends` file?
    ```bash
    wc -l < friends
    ```
    **Explanation:** This counts the lines in the file.

---

### Lab 3: Working with Vi Editor

1. **Question:** How do you create a file using Vi and edit it?
   ```bash
   vi filename
   ```
   Inside Vi, press `i` to insert text, then add the provided content. 

   - Change "Netware" to "Novell Netware."
   - Insert "(such as hard disks and printers)" after "share resources."
   - Append the additional text as instructed.

2. **Question:** How do you create the data files used in previous lab sessions using Vi?
   ```bash
   vi emp.lst
   vi dept.lst
   vi desig.lst
   ```
   **Explanation:** This opens each file for creation and editing.

---

### Lab 4: Writing Shell Scripts

1. **Question:** How do you display the primary and secondary prompt and change it temporarily?
   ```bash
   PS1="YourName> "
   ```
   **Explanation:** This changes the primary prompt for the session.

2. **Question:** How do you permanently change your prompt upon login?
   Add `PS1="YourName> "` to `~/.bashrc`.

3. **Question:** How do you check the content of the environmental variable `SHELL`?
   ```bash
   echo $SHELL
   ```
   **Explanation:** This prints the shell being used.

4. **Question:** What happens when you use `export` with a variable?
   - This makes the variable available to subshells.

5. **Question:** How do you write a shell script that checks if a user is logged in?
   ```bash
   #!/bin/bash
   read -p "Enter username: " user
   if who | grep -q "$user"; then
       echo "$user is logged in."
   else
       echo "$user is not logged in."
   fi
   ```
   **Explanation:** This script checks for user login status.

6. **Question:** How do you write a script to display file names and contents?
   ```bash
   for file in *; do
       echo "File: $file"
       cat "$file"
   done
   ```
   **Explanation:** This iterates through files and displays their contents.

7. **Question:** How do you check if a file exists and display permissions?
   ```bash
   #!/bin/bash
   read -p "Enter filename: " file
   if [ -e "$file" ]; then
       ls -l "$file"
   else
       echo "$file does not exist."
   fi
   ```
   **Explanation:** This checks for existence and shows permissions.

8. **Question:** How do you find the largest number from three command line arguments?
   ```bash
   #!/bin/bash
   max=$1
   for num in "$@"; do
       if (( num > max )); then
           max=$num
       fi
   done
   echo "Largest number: $max"
   ```
   **Explanation:** This compares numbers to find the largest.

9. **Question:** How do you create a menu for file operations?
   ```bash
   #!/bin/bash
   while true; do
       echo "1. Create file"
       echo "2. Create directory"
       echo "3. Copy file"
       echo "4. Move file"
       echo "5. Exit"
       read -p "Choose an option: " choice
       case $choice in


           1) # Create file logic ;;
           2) # Create directory logic ;;
           3) # Copy file logic ;;
           4) # Move file logic ;;
           5) exit ;;
           *) echo "Invalid option." ;;
       esac
   done
   ```
   **Explanation:** This script provides a simple menu interface.

10. **Question:** How do you check for a file or directory and confirm deletion?
    ```bash
    #!/bin/bash
    read -p "Enter filename/directory: " name
    if [ -e "$name" ]; then
        read -p "Do you really want to delete $name? (y/n) " answer
        if [ "$answer" == "y" ]; then
            rm -r "$name"
            echo "$name deleted."
        else
            echo "Deletion canceled."
        fi
    else
        echo "$name does not exist."
    fi
    ```
    **Explanation:** This checks existence, asks for confirmation, and deletes if confirmed.

11. **Question:** How do you store names of employees and check login status?
    ```bash
    #!/bin/bash
    employees=("Alice" "Bob" "Charlie" "David")
    for emp in "${employees[@]}"; do
        if who | grep -q "$emp"; then
            echo "$emp is logged in."
        else
            echo "$emp is not logged in."
        fi
    done
    ```
    **Explanation:** This checks the login status of each employee.

---

### Lab 5: Using Process-Related Commands

1. **Question:** How do you find out the PID of processes activated by you?
   ```bash
   ps -u your_username
   ```
   **Explanation:** This lists processes for the specified user.

2. **Question:** How do you get information about all currently active processes?
   ```bash
   ps aux
   ```
   **Explanation:** This shows detailed information about all processes.

3. **Question:** How do you start a process in the background and check its status?
   ```bash
   sleep 60 &
   ```
   Check status with:
   ```bash
   jobs
   ```
   **Explanation:** This runs the `sleep` command in the background.

---

### Stretched Assignments

1. **Question:** How do you display date information in a specific order?
   ```bash
   date "+%H:%M:%S %A %j %B %Y"
   ```
   **Explanation:** This formats the output as required.

2. **Question:** How do you print names of files in descending order of links?
   ```bash
   ls -l | sort -k2 -n -r
   ```
   **Explanation:** This sorts files by link count in descending order.

3. **Question:** How do you print names of files in alphabetical order?
   ```bash
   ls | sort
   ```
   **Explanation:** This sorts and lists filenames alphabetically.

4. **Question:** How do you print names and sizes of files in order of size?
   ```bash
   ls -lS
   ```
   **Explanation:** This lists files sorted by size.

5. **Question:** How do you determine the latest file updated by the user?
   ```bash
   ls -lt | head -n 1
   ```
   **Explanation:** This shows the most recently modified file.

---

