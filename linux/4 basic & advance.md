# Basic Commands

1. **How do you check the current working directory?**
   - Command: `pwd`
   - Example: 
     ```bash
     $ pwd
     /home/user
     ```

2. **What command displays the first 10 lines of a file?**
   - Command: `head <filename>`
   - Example: 
     ```bash
     $ head example.txt
     ```

3. **How can you count the number of lines in a file?**
   - Command: `wc -l <filename>`
   - Example: 
     ```bash
     $ wc -l example.txt
     42 example.txt
     ```

     - wc can count line , word and char

4. **What command lists all files in the current directory?**
   - Command: `ls`
   - Example: 
     ```bash
     $ ls
     file1.txt  file2.txt  dir1
     ```

5. **How do you display the last 5 lines of a file?**
   - Command: `tail -n 5 <filename>`
   - Example: 
     ```bash
     $ tail -n 5 example.txt
     ```

# Intermediate Commands

6. **How can you find all occurrences of "error" in a log file, ignoring case?**
   - Command: `grep -i "error" <logfile>`
   - Example: 
     ```bash
     $ grep -i "error" server.log
     ```

7. **What command displays unique entries from a file?**
   - Command: `sort <filename> | uniq`
   - Example: 
     ```bash
     $ sort entries.txt | uniq
     ```

8. **How do you show the disk usage of files and directories?**
   - Command: `du -h`
   - Example: 
     ```bash
     $ du -h
     4.0K   ./dir1
     1.5M   ./file.txt
     ```

9. **How can you redirect standard output and standard error to different files?**
   - Command: `command > output.txt 2> error.txt`
   - Example: 
     ```bash
     $ ls /nonexistent > out.txt 2> err.txt
     ```

     ```
     >  is used for overwrite

     >> append add to the bottom
     ```

10. **What command changes the owner of a file to a different user?**
    - Command: `chown <newowner> <filename>`
    - Example: 
      ```bash
      $ sudo chown john file.txt
      ```

# Advanced Commands

11. **How can you display lines from a file that contain a specific word but not a certain pattern?**
    - Command: `grep "word" <filename> | grep -v "pattern"`
    - Example: 
      ```bash
      $ grep "foo" file.txt | grep -v "bar"
      ```

12. **What command finds all .txt files recursively and lists them?**
    - Command: `find . -name "*.txt"`
    - Example: 
      ```bash
      $ find . -name "*.txt"
      ./docs/file.txt
      ```

13. **How do you replace a string in a file using `sed`?**
    - Command: `sed -i 's/oldstring/newstring/g' <filename>`
    - Example: 
      ```bash
      $ sed -i 's/foo/bar/g' example.txt
      ```

14. **What command creates a tarball of a directory?**
    - Command: `tar -cvf archive.tar <directory>`
    - Example: 
      ```bash
      $ tar -cvf archive.tar myfolder
      ```

15. **How can you list users currently logged into the system?**
    - Command: `who`
    - Example: 
      ```bash
      $ who
      user1    pts/0        2024-09-18 10:12
      ```

# Basic Commands (Continued)

16. **How do you view the contents of a text file one screen at a time?**
    - Command: `less <filename>`
    - Example: 
      ```bash
      $ less example.txt
      ```

17. **What command allows you to create a new directory?**
    - Command: `mkdir <dirname>`
    - Example: 
      ```bash
      $ mkdir newdir
      ```

18. **How can you copy a file from one location to another?**
    - Command: `cp <source> <destination>`
    - Example: 
      ```bash
      $ cp file1.txt /backup/
      ```

19. **What command removes a file from the filesystem?**
    - Command: `rm <filename>`
    - Example: 
      ```bash
      $ rm file.txt
      ```

20. **How do you check the current user's home directory?**
    - Command: `echo $HOME`
    - Example: 
      ```bash
      $ echo $HOME
      /home/user
      ```
      - $home is variavble predefine in the system

# Intermediate Commands (Continued)

21. **How can you find all files modified in the last 7 days?**
    - Command: `find . -mtime -7`
    - Example: 
      ```bash
      $ find . -mtime -7
      ```
-special file

     ```
      $ find . -type f -name "a.txt" -mtime -7
      ```

22. **What command lists all currently running processes?**
    - Command: `ps aux`
    - Example: 
      ```bash
      $ ps aux
      ```

23. **How do you check the free and used disk space on the system?**
    - Command: `df -h`
    - Example: 
      ```bash
      $ df -h
      ```

24. **What command can you use to search for a specific pattern in a directory of files?**
    - Command: `grep -r "pattern" <directory>`
    - Example: 
      ```bash
      $ grep -r "error" /var/log
      ```

25. **How can you compare two files line by line?**
    - Command: `diff <file1> <file2>`
    - Example: 
      ```bash
      $ diff file1.txt file2.txt
      ```

# Advanced Commands (Continued)

26. **How do you monitor real-time log file updates?**
    - Command: `tail -f <logfile>`
    - Example: 
      ```bash
      $ tail -f /var/log/syslog
      ```

27. **What command can you use to find the largest files in a directory?**
    - Command: `du -ah <directory> | sort -rh | head -n 10`
    - Example: 
      ```bash
      $ du -ah /home | sort -rh | head -n 10
      ```
      du -ah  --> find size and name of file

      sort -rh  -->  large size first

28. **How do you change file permissions to allow read, write, and execute for the owner only?**
    - Command: `chmod 700 <filename>`
    - Example: 
      ```bash
      $ chmod 700 file.txt
      ```

29. **What command combines multiple files into a single file?**
    - Command: `cat <file1> <file2> > combinedfile`
    - Example: 
      ```bash
      $ cat file1.txt file2.txt > combined.txt
      ```

30. **How can you check network connectivity to a specific IP address?**
    - Command: `ping <IP-address>`
    - Example: 
      ```bash
      $ ping 8.8.8.8
      ```

# Bonus Questions

31. **How do you list all environment variables in the current session?**
    - Command: `printenv` or `env`
    - Example: 
      ```bash
      $ printenv
      ```

32. **What command can you use to display the last 20 entries in the system log?**
    - Command: `tail -n 20 /var/log/syslog`
    - Example: 
      ```bash
      $ tail -n 20 /var/log/syslog
      ```

33. **How do you create a symbolic link to a file?**
    - Command: `ln -s <targetfile> <linkname>`
    - Example: 
      ```bash
      $ ln -s /path/to/file symlink
      ```

34. **What command lists all installed packages on a Debian-based system?**
    - Command: `dpkg --list`
    - Example: 
      ```bash
      $ dpkg --list
      ```

35. **How can you schedule a command to run at a specific time using cron?**
    - Command: `crontab -e` and use appropriate cron syntax
    - Example: 
      ```bash
      # Example: Run a script at 2 AM daily
      0 2 * * * /path/to/script.sh
      ```
