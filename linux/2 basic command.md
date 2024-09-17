# Linux Commands - Beginner Friendly Guide

1. **ls**
   - *Example:* `ls`
   - *Explanation:* Shows a list of files and folders in the current directory.

2. **cp**
   - *Example:* `cp file1.txt file2.txt`
   - *Explanation:* Copies a file. `file1.txt` will be copied to `file2.txt`.

3. **mv**
   - *Example:* `mv oldname.txt newname.txt`
   - *Explanation:* Moves or renames files. `oldname.txt` will be renamed to `newname.txt`.

4. **lpr**
   - *Example:* `lpr file.txt`
   - *Explanation:* Sends a file to the printer to print.

5. **sort**
   - *Example:* `sort file.txt`
   - *Explanation:* Sorts the lines in a file alphabetically.

6. **grep**
   - *Example:* `grep 'text' file.txt`
   - *Explanation:* Searches for the word "text" in `file.txt` and shows matching lines.

7. **cat**
   - *Example:* `cat file.txt`
   - *Explanation:* Displays the content of a file.

8. **tac**
   - *Example:* `tac file.txt`
   - *Explanation:* Shows the content of a file in reverse order (last line first).

9. **more**
   - *Example:* `more file.txt`
   - *Explanation:* Views the content of a file one screen at a time.

10. **head**
    - *Example:* `head file.txt`
    - *Explanation:* Shows the first 10 lines of a file.

11. **tail**
    - *Example:* `tail file.txt`
    - *Explanation:* Shows the last 10 lines of a file.

12. **man**
    - *Example:* `man ls`
    - *Explanation:* Opens the manual for a command, like `ls`, to learn more about it.

13. **whatis**
    - *Example:* `whatis ls`
    - *Explanation:* Provides a brief description of the `ls` command.

14. **whereis**
    - *Example:* `whereis ls`
    - *Explanation:* Finds where the `ls` command is located on your system.

15. **locate**
    - *Example:* `locate file.txt`
    - *Explanation:* Finds files by name quickly.

16. **find**
    - *Example:* `find / -name 'file.txt'`
    - *Explanation:* Searches for files named `file.txt` starting from the root directory.

17. **diff**
    - *Example:* `diff file1.txt file2.txt`
    - *Explanation:* Compares two files and shows the differences.

18. **file**
    - *Example:* `file file.txt`
    - *Explanation:* Tells you what type of file `file.txt` is (e.g., text, image).

19. **rm**
    - *Example:* `rm file.txt`
    - *Explanation:* Deletes a file.

20. **mkdir**
    - *Example:* `mkdir newdir`
    - *Explanation:* Creates a new directory named `newdir`.

21. **rmdir**
    - *Example:* `rmdir olddir`
    - *Explanation:* Removes an empty directory named `olddir`.

22. **cd**
    - *Example:* `cd /path/to/directory`
    - *Explanation:* Changes the current directory to the one you specify.

23. **pwd**
    - *Example:* `pwd`
    - *Explanation:* Shows the current directory you are in.

24. **ln**
    - *Example:* `ln file.txt link.txt`
    - *Explanation:* Creates a hard link to `file.txt` named `link.txt`.

25. **ln -s**
    - *Example:* `ln -s file.txt symlink.txt`
    - *Explanation:* Creates a symbolic (or soft) link to `file.txt` named `symlink.txt`.

26. **gzip**
    - *Example:* `gzip file.txt`
    - *Explanation:* Compresses `file.txt` to `file.txt.gz`.

27. **gunzip**
    - *Example:* `gunzip file.txt.gz`
    - *Explanation:* Decompresses `file.txt.gz` back to `file.txt`.

28. **zip**
    - *Example:* `zip archive.zip file.txt`
    - *Explanation:* Compresses `file.txt` into a zip archive named `archive.zip`.

29. **unzip**
    - *Example:* `unzip archive.zip`
    - *Explanation:* Extracts files from `archive.zip`.

30. **tar**
    - *Example:* `tar -cvf archive.tar file.txt`
    - *Explanation:* Creates a tar archive named `archive.tar` containing `file.txt`.

31. **tar -xvf**
    - *Example:* `tar -xvf archive.tar`
    - *Explanation:* Extracts files from `archive.tar`.

32. **zcat**
    - *Example:* `zcat file.gz`
    - *Explanation:* Shows the content of a compressed file without decompressing it.

33. **cal**
    - *Example:* `cal`
    - *Explanation:* Displays the calendar for the current month.

34. **bc**
    - *Example:* `bc`
    - *Explanation:* Opens a calculator for performing calculations.

35. **bc -l**
    - *Example:* `bc -l`
    - *Explanation:* Opens a calculator with more mathematical functions.

36. **banner**
    - *Example:* `banner Hello`
    - *Explanation:* Displays "Hello" in large ASCII text (might not be available on all systems).

37. **date**
    - *Example:* `date`
    - *Explanation:* Shows the current date and time.

38. **time**
    - *Example:* `time ls`
    - *Explanation:* Shows how long it takes to run a command like `ls`.

39. **wc**
    - *Example:* `wc file.txt`
    - *Explanation:* Counts the number of lines, words, and characters in `file.txt`.

40. **touch**
    - *Example:* `touch newfile.txt`
    - *Explanation:* Creates an empty file named `newfile.txt` or updates its modification time if it already exists.

41. **echo**
    - *Example:* `echo "Hello"`
    - *Explanation:* Prints "Hello" to the screen.

42. **who**
    - *Example:* `who`
    - *Explanation:* Lists users currently logged in to the system.

43. **finger**
    - *Example:* `finger username`
    - *Explanation:* Shows information about a user named `username`.

44. **w**
    - *Example:* `w`
    - *Explanation:* Shows who is logged in and what they are doing.

45. **whoami**
    - *Example:* `whoami`
    - *Explanation:* Displays your current username.

46. **who am i**
    - *Example:* `who am i`
    - *Explanation:* Shows information about your current login session.

47. **alias**
    - *Example:* `alias ll='ls -l'`
    - *Explanation:* Creates a shortcut command. For example, `ll` will run `ls -l`.

48. **unalias**
    - *Example:* `unalias ll`
    - *Explanation:* Removes a shortcut command you created with `alias`.

49. **pushd**
    - *Example:* `pushd /path/to/directory`
    - *Explanation:* Saves your current directory and changes to a new one.

50. **popd**
    - *Example:* `popd`
    - *Explanation:* Returns to the directory saved with `pushd`.

51. **jobs**
    - *Example:* `jobs`
    - *Explanation:* Lists background tasks running in your session.

52. **ps**
    - *Example:* `ps`
    - *Explanation:* Shows information about currently running processes.


#

Here is the list of questions numbered sequentially:


# Bash Commands Practice

## File Operations
1. **Create an empty file** named `example.txt`:
   ```bash
   touch example.txt
   ```

2. **Display the contents** of a file `file.txt`:
   ```bash
   cat file.txt
   ```

3. **Rename a file** `old.txt` to `new.txt`:
   ```bash
   mv old.txt new.txt
   ```

4. **Copy a file** `source.txt` to the directory `/home/user/backup`:
   ```bash
   cp source.txt /home/user/backup/
   ```

5. **Move file `file2.txt`** to the `test_dir` directory:
   ```bash
   mv file2.txt ~/test_dir/
   ```

6. **Delete the file** `file1.txt`:
   ```bash
   rm file1.txt
   ```

## Directory Operations
7. **Create a directory** named `test_dir` in your home directory:
   ```bash
   mkdir ~/test_dir
   ```

8. **Remove a directory** `testdir` and all its contents:
   ```bash
   rm -r testdir
   ```

## Listing Files
9. **List all files (including hidden ones)** in the current directory:
   ```bash
   ls -a
   ```

10. **Find all `.txt` files** in the current directory and subdirectories:
   ```bash
   find . -name "*.txt"
   ```

11. **List all files (including hidden ones)** in `/home/user/`:
   ```bash
   ls -a /home/user/
   ```

## File Content Viewing
12. **Display the first 10 lines** of a file called `data.log`:
   ```bash
   head data.log
   ```

13. **Display the last 10 lines** of a file `log.txt`:
   ```bash
   tail log.txt
   ```

14. **Show the first 5 lines** of a file named `notes.txt`:
   ```bash
   head -n 5 notes.txt
   ```

## Search and Filter
15. **Search for the word** "error" in a file `system.log`:
   ```bash
   grep "error" system.log
   ```

16. **Search for the word** "error" in a file named `log.txt`:
   ```bash
   grep "error" log.txt
   ```

## Permissions and Links
17. **Change the permissions** of `script.sh` to make it executable:
   ```bash
   chmod +x script.sh
   ```

18. **Change the permissions** of `file1.txt` to make it executable for the owner only:
   ```bash
   chmod u+x file1.txt
   ```

19. **Create a symbolic link** named `my_link` that points to `file1.txt`:
   ```bash
   ln -s file1.txt my_link
   ```

## Counting and Disk Space
20. **Count the number of lines, words, and characters** in a file `notes.txt`:
   ```bash
   wc notes.txt
   ```

21. **Count the number of lines** in a file named `data.csv`:
   ```bash
   wc -l data.csv
   ```

22. **Check the amount of free disk space** on your system:
   ```bash
   df -h
   ```

23. **Display the current disk usage** of the filesystem:
   ```bash
   df -h
   ```

## Process and Directory
24. **Display the running processes** on your system:
   ```bash
   ps aux
   ```

25. **Display the current working directory**:
   ```bash
   pwd
   ```

## Output Redirection
26. **Append the output of** `ls -l` to a file called `logfile.txt`:
   ```bash
   ls -l >> logfile.txt
   ```


