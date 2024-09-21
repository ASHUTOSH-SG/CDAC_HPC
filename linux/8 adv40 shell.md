## 1. How would you set up a cron job to back up a directory every night at midnight?


Here’s the updated backup script with comments to explain each part:

### Cron Job Setup
First, add this line in your crontab (`crontab -e`):

```bash
0 0 * * * /path/to/backup-script.sh
```
This will run the script every day at midnight (00:00).

The stars (*) in 0 0 * * * represent  minitue hour "every day, every month, and every day of the week," so the script runs at midnight daily

### Backup Script (`backup-script.sh`)

```bash
#!/bin/bash

# Define the source directory to be backed up
SOURCE_DIR="$HOME/cdac"

# Define the directory where backups will be stored
BACKUP_DIR="$HOME/cdac/backup"

# Get the current date (format: YYYY-MM-DD)
DATE=$(date +%Y-%m-%d)

# Define the backup file name with the date in it
BACKUP_FILE="$BACKUP_DIR/backup-$DATE.tar.gz"

# Create the backup directory if it doesn't exist
mkdir -p $BACKUP_DIR

# Create a compressed tarball (.tar.gz) of the source directory
# -C changes to the source directory, and "." ensures everything in that folder is included
tar -czf $BACKUP_FILE -C $SOURCE_DIR .

# Optional: Print a message to indicate the backup was successful
echo "Backup completed: $BACKUP_FILE"
```

### Explanation of the Code:
1. **`SOURCE_DIR="$HOME/cdac"`**: This is the folder you want to back up.
2. **`BACKUP_DIR="$HOME/cdac/backup"`**: This is the folder where the backup will be saved.
3. **`DATE=$(date +%Y-%m-%d)`**: This generates the current date in the format `YYYY-MM-DD`, which will be used in the backup file name.
4. **`BACKUP_FILE="$BACKUP_DIR/backup-$DATE.tar.gz"`**: This specifies the full path and name of the backup file, including the date.
5. **`mkdir -p $BACKUP_DIR`**: Creates the backup directory if it doesn’t already exist.
6. **`tar -czf $BACKUP_FILE -C $SOURCE_DIR .`**: Compresses (`-czf`) everything from the source directory into a `.tar.gz` file.
7. **`echo "Backup completed"`**: This is optional, just to inform you that the backup has been completed.

### Make the Script Executable
Finally, don’t forget to make the script executable by running:

```bash
chmod u+x /path/to/backup-script.sh
```
Let's go through your points with corrections and explanations:



## 2. How can you list all scheduled cron jobs for the current user?
To list all scheduled cron jobs for the current user, the correct command is:

```bash
crontab -l
```

- **Explanation**: `crontab -l` lists all cron jobs for the user, while `-1` is not a valid option.

---

### 3. How can you use cron to run a job every hour on the hour and every 15 minutes past the hour?

To run a script every hour at the following times: at the start of the hour, 15 minutes past, 30 minutes past, and 45 minutes past, the cron syntax should be:

```bash
0 * * * * /path/to/your/script.sh   # At the start of every hour
15 * * * * /path/to/your/script.sh  # 15 minutes past the hour
30 * * * * /path/to/your/script.sh  # 30 minutes past the hour
45 * * * * /path/to/your/script.sh  # 45 minutes past the hour
```

- **Explanation**: The `0`, `15`, `30`, and `45` represent the minutes at which the job runs each hour. Each `*` represents "every" hour, day, month, and weekday. You had missing spaces in your example (`15**` should be `15 * * * *`).

---

### 4. Counting Lines with a Specific Word

Here’s a corrected version of the script that prompts the user for a filename and word to search for:

```bash
#!/bin/bash

# Prompt the user for the file name
read -p "Enter the file name: " filename

# Prompt the user for the word to search for
read -p "Enter the word to search for: " word

# Count the lines containing the specified word
grep -i "$word" "$filename" | wc -l
```

- **Explanation**:
  - `read -p` is used to prompt the user for input.
  - `grep -i` searches for the word in the file, ignoring case (`-i`).
  - `wc -l` counts the number of lines containing the word.

This script will count how many lines in the given file contain the word the user inputs.

## 5. Count the number of lines in the file logfile.txt that contain the exact word "ERROR". Ensure that "ERROR123" or "WARNINGERROR" are excluded from the count

```bash
grep -w "ERROR" logfile.txt | wc -l
```

### Explanation:
- **`grep -w "ERROR"`**: The `-w` option ensures that only the exact word "ERROR" is matched (so "ERROR123" or "WARNINGERROR" will not be counted).
- **`logfile.txt`**: The file you are searching within.
- **`wc -l`**: Counts the number of lines output by `grep`.

This command will count only the lines where "ERROR" appears as a standalone word in `logfile.txt`.

## 6. Ask the user for a file extension and find all files matching that extension in the current directory and its subdirectories. Display the file paths for both directories.


### Script:
```bash
#!/bin/bash

# Prompt the user for a file extension
read -p "Enter the file extension (e.g., txt, pdf): " file_extension

# Find all files with the given extension in the current directory and subdirectories
current_dir_files=$(find . -type f -name "*.$file_extension")

# Display the file paths
echo "Files in the current directory and subdirectories with .$file_extension extension:"
echo "$current_dir_files"
```

### Explanation:
1. **`read -p "Enter the file extension"`**: Prompts the user to input the desired file extension.
2. **`find . -type f -name "*.$file_extension"`**:
   - `find .` starts searching in the current directory (`.`) and its subdirectories.
   - `-type f` ensures it only finds regular files.
   - `-name "*.$file_extension"` finds files that end with the given extension.
3. **`echo "$current_dir_files"`**: Prints the paths of the files found.


## 7. After finding files with a specified extension in the current directory, create a tarball archive named backup.tar.gz containing all those files

Here’s the corrected script that finds files with a specified extension and creates a tarball archive named `backup.tar.gz` containing those files:

### Script:
```bash
#!/bin/bash

# Prompt the user for a file extension
read -p "Enter the file extension (e.g., txt, pdf): " file_extension

# Find all files with the given extension in the current directory and subdirectories
files=$(find . -type f -name "*.$file_extension")

# Check if any files were found
if [ -z "$files" ]; then
    echo "No files found with the extension .$file_extension"
else
    # Create a tarball archive named backup.tar.gz with the found files
    tar -czvf backup.tar.gz $files
    echo "Backup created: backup.tar.gz"
fi
```

### Explanation:
The -z option is a way to test for an empty string in a shell script. If files contains no matching files,

1. **`read -p "Enter the file extension"`**: Prompts the user for a file extension.
2. **`files=$(find . -type f -name "*.$file_extension")`**: Finds all files with the specified extension in the current directory and subdirectories.
3. **`if [ -z "$files" ]; then ... fi`**: Checks if any files were found:
   - If no files are found, it informs the user.
   - If files are found, it proceeds to create the tarball.
4. **`tar -czvf backup.tar.gz $files`**:
   - `-c`: Create a new archive.
   - `-z`: Compress the archive using gzip.
   - `-v`: Verbosely list files processed.
   - `-f backup.tar.gz`: Specifies the name of the archive file.


## 8. Replace "temporary" with "permanent" in all .txt files
```
#!/bin/bash

# Find and replace "temporary" with "permanent" in all .txt files in ~/test
find ~/test/ -type f -name "*.txt" -exec sed -i 's/temporary/permanent/g' {} +
```
### Explanation:
#### - `find ~/test/`: Searches in the ~/test directory.
#### - `-type f`: Targets only files.
#### - `-name "*.txt"`: Filters for .txt files.
#### - `-exec sed -i 's/temporary/permanent/g' {} +`: Executes the `sed` command to replace occurrences in-place.

The command `-exec sed -i 's/temporary/permanent/g' {} +` is part of the `find` command and does the following:

### Breakdown:
- **`-exec`**: This option allows you to execute a command on the files found by `find`.
- **`sed -i 's/temporary/permanent/g'`**:
  - **`sed`**: A stream editor for filtering and transforming text.
  - **`-i`**: Stands for "in-place," meaning that the changes will be applied directly to the files instead of outputting to the terminal.
  - **`'s/temporary/permanent/g'`**: This is a `sed` substitution command:
    - **`s/`**: Indicates substitution.
    - **`temporary`**: The string to be replaced.
    - **`permanent`**: The string to replace it with.
    - **`g`**: Stands for "global," meaning all occurrences in each line will be replaced, not just the first one.
- **`{}`**: A placeholder that `find` replaces with the current file name it has found.
- **`+`**: Indicates that `find` should pass multiple file names at once to the `sed` command, improving efficiency over using `\;`, which would run `sed` for each file individually.




## 9. Create a script that asks the user for a directory and then lists all files in that directory with their sizes in a human-readable format. Exclude directories from the list

```
#!/bin/bash

# Ask the user for a directory
read -p "Enter a directory: " directory

# List files in the specified directory with human-readable sizes, excluding directories
if [ -d "$directory" ]; then
    find "$directory" -maxdepth 1 -type f -exec du -h {} +
else
    echo "The specified path is not a directory."
fi

# Explanation:
# - -maxdepth 1: Limits the search to the specified directory, excluding subdirectories.
# - -type f: Finds only files.
# - du -h: Displays file sizes in a human-readable format.

```

## 10 Ask the user for a directory and a time period (in days). List all files in that directory that have been modified within the last specified number of days.

```
#!/bin/bash

# Ask the user for a directory and store it in the variable 'directory'
read -p "Enter a directory: " directory

# Ask the user for a time period in days and store it in the variable 'days'
read -p "Enter the time period in days: " days

# Check if the specified path is a valid directory
if [ -d "$directory" ]; then
    # Inform the user about the files being listed
    echo "Files modified in the last $days days in '$directory':"
    
    # Use the 'find' command to locate files modified within the specified number of days
    find "$directory" -type f -mtime -"$days"
else
    # Inform the user that the specified path is not a directory
    echo "The specified path '$directory' is not a directory."
fi

```


## 11. Rename .tmp files to .bak

```
#!/bin/bash

# Find all .tmp files in the current directory and rename them to .bak
find . -type f -name "*.tmp" -exec bash -c 'mv "$0" "${0%.tmp}.bak"' {} \;

# Explanation:
# - `find .`: Searches in the current directory (denoted by `.`).
# - `-type f`: Limits the search to regular files only (not directories).
# - `-name "*.tmp"`: Filters the search to files with a .tmp extension.
# - `-exec`: Allows the execution of a command on each file found.
# - `bash -c`: Runs a new Bash shell to execute the following command.
# - `'mv "$0" "${0%.tmp}.bak"'`: The command to be executed:
#   - `mv "$0"`: Moves (renames) the file represented by `$0`, which is replaced by the filename found.
#   - `"${0%.tmp}.bak"`: This constructs the new filename:
#     - `${0%.tmp}`: Uses parameter expansion to remove the `.tmp` suffix from the filename.
#     - `.bak`: Appends the new extension, resulting in a filename ending with `.bak`.
# - `{}`: A placeholder that `find` replaces with the current file's path.
# - `\;`: Indicates the end of the `-exec` command.


```


## 12. Write a script that asks the user for a file name and displays the file's creation timestamp. If the file does user.

```


### Script:
```bash
#!/bin/bash

# Ask the user for a file name
read -p "Enter the file name: " filename

# Check if the file exists
if [ -f "$filename" ]; then
    # Get the file's creation timestamp
    timestamp=$(stat -c %W "$filename")
    
    # Check if the timestamp is not zero (0 means not available)
    if [ "$timestamp" -ne 0 ]; then
        # Convert the timestamp to a human-readable format
        creation_time=$(date -d @"$timestamp")
        echo "The creation timestamp of '$filename' is: $creation_time"
    else
        echo "Creation timestamp is not available for '$filename'."
    fi
else
    echo "File '$filename' does not exist."
fi
```

### Explanation:
1. **User Input**: 
   - `read -p "Enter the file name: " filename`: Prompts the user to enter a file name and stores it in the variable `filename`.

2. **File Existence Check**: 
   - `if [ -f "$filename" ]; then`: Checks if the file exists and is a regular file.

3. **Get Creation Timestamp**: 
   - `timestamp=$(stat -c %W "$filename")`: Uses `stat` to get the file's creation timestamp. `%W` returns the creation time in seconds since the epoch.

4. **Timestamp Check**: 
   - `if [ "$timestamp" -ne 0 ]; then`: Checks if the timestamp is not zero (a zero timestamp indicates that the creation time is not available).

5. **Convert and Display**: 
   - `creation_time=$(date -d @"$timestamp")`: Converts the timestamp to a human-readable format using the `date` command.
   - `echo "The creation timestamp of '$filename' is: $creation_time"`: Displays the creation timestamp.

6. **Error Handling**: 
   - If the file does not exist or if the creation timestamp is unavailable, appropriate messages are printed.



## 14. Ask the user to input a size threshold (e.g., 50MB) and find all files in the current directory and its subdirectories larger than this threshold. List their names and sizes.

```
#!/bin/bash

# Prompt the user to enter the lower size limit (in kilobytes)
read -p "Enter the lower value (in KB): " low

# Prompt the user to enter the upper size limit (in kilobytes)
read -p "Enter the upper value (in KB): " upp

# Use the 'find' command to search for files within the specified size range
# -type f: Look for regular files only
# -size +"$low"k: Files larger than the lower limit specified by the user
# -size -"$upp"k: Files smaller than the upper limit specified by the user
# -ls: List the details of the found files
find . -type f -size +"$low"k -size -"$upp"k -ls

```

## 15.    Extract and display all unique email addresses from a file contacts.txt. Assume that email addresses are in the format username@domain.com.

```
#!/bin/bash

# Extract and display all unique email addresses from contacts.txt
# Use grep to find email addresses, sort them, and remove duplicates

# Extract email addresses
grep -Eo '[[:alnum:]_]+@[[:alnum:]]+\.[[:alnum:]]+' contacts.txt | sort | uniq

# Explanation:
# - grep: Command used to search for patterns in files.
# - -E: Enables extended regular expressions, allowing for more complex patterns.
# - -o: Only print the part of the line that matches the pattern (email addresses).
# - '[[:alnum:]_]+': Matches one or more alphanumeric characters or underscores (the username).
# - '@': Matches the "@" symbol.
# - '[[:alnum:]]+\.[[:alnum:]]+': Matches the domain part, which consists of one or more alphanumeric characters, followed by a dot, and one or more alphanumeric characters (the domain name).
# - sort: Sorts the extracted email addresses.
# - uniq: Removes duplicate entries from the sorted list, leaving only unique email addresses.

```


## 17 Replace all instances of the word "old" with "new" in all .nd files within a given directory and its subitirenter Make sure to only replace whole words
```
#!/bin/bash

# Prompt the user to enter a directory
read -p "Enter the directory: " directory

# Use the 'find' command to locate .nd files and replace "old" with "new"
find "$directory" -type f -name "*.nd" -exec sed -i 's/\bold\b/new/g' {} +

# Explanation:
# - find "$directory": Searches in the specified directory.
# - -type f: Looks for regular files only.
# - -name "*.nd": Filters for files with the .nd extension.
# - -exec: Executes the following command on each found file.
# - sed -i 's/\bold\b/new/g': 
#   - -i: Modifies the files in place.
#   - 's/\bold\b/new/g': Substitutes "old" with "new", where:
#     - \b: Ensures that only whole words are matched (word boundary).
#     - g: Replaces all instances in the file (global).
# - {} +: Replaces {} with the filenames found by `find`.

```
## 18. Compare the sizes of two files provided by the user and display which file is larger or if they are of equal size

```
Here’s a corrected and complete version of your script that compares the sizes of two files provided by the user:

### Script:
```bash
#!/bin/bash

# Prompt the user for the first file name
read -p "Enter the first file name: " file1

# Prompt the user for the second file name
read -p "Enter the second file name: " file2

# Check if both files exist
if [ -f "$file1" ] && [ -f "$file2" ]; then
    # Get the sizes of the files
    size1=$(stat -c%s "$file1")  # Get size in bytes of file1
    size2=$(stat -c%s "$file2")  # Get size in bytes of file2

    # Compare the sizes
    if [[ $size1 -gt $size2 ]]; then
        echo "$file1 is larger."
    elif [[ $size1 -lt $size2 ]]; then
        echo "$file2 is larger."
    else
        echo "The files are of equal size."
    fi
else
    echo "One or both files do not exist."
fi
```

### Explanation:
1. **User Input**:
   - `read -p "Enter the first file name: " file1`: Prompts the user to enter the name of the first file and stores it in the variable `file1`.
   - `read -p "Enter the second file name: " file2`: Prompts the user for the name of the second file and stores it in `file2`.

2. **File Existence Check**:
   - `if [ -f "$file1" ] && [ -f "$file2" ]; then`: Checks if both files exist and are regular files.

3. **Get File Sizes**:
   - `size1=$(stat -c%s "$file1")`: Uses `stat` to get the size of `file1` in bytes.
   - `size2=$(stat -c%s "$file2")`: Uses `stat` to get the size of `file2` in bytes.

4. **Compare Sizes**:
   - `if [[ $size1 -gt $size2 ]]; then`: Checks if `file1` is larger than `file2`.
   - `elif [[ $size1 -lt $size2 ]]; then`: Checks if `file2` is larger than `file1`.
   - `else`: If neither condition is true, the files are of equal size.

5. **Error Message**:
   - If either file does not exist, the script prints an appropriate message.



## 19 Write a script to identify and display duplicate lines in a file data.txt. List each duplicate line along with the number of times it appears.



```
#!/bin/bash

# Sort the file and count occurrences of each line
input_file="data.txt"

# Check if the file exists
if [ -f "$input_file" ]; then
    echo "Duplicate lines in '$input_file':"
    
    # Sort the file, count occurrences, and filter for duplicates
    sort "$input_file" | uniq -c | while read -r count line; do
        # Only print lines that appear more than once
        if [[ $count -gt 1 ]]; then
            echo "$line appears $count times"
        fi
    done
else
    echo "The file '$input_file' does not exist."
fi
```

### Explanation:
1. **Input File**:
   - `input_file="data.txt"`: Specifies the file to be analyzed.

2. **File Existence Check**:
   - `if [ -f "$input_file" ]; then`: Checks if `data.txt` exists.

3. **Finding Duplicates**:
   - `sort "$input_file"`: Sorts the contents of the file to prepare it for counting.
   - `| uniq -c`: Counts occurrences of each line in the sorted output. The `-c` option prefixes each line with its count.

4. **Reading Output**:
   - `while read -r count line; do`: Reads the count and the line from the output of `uniq -c`. 
   - `$count` is the number of occurrences, and `$line` is the actual line content.

5. **Conditional Check**:
   - `if [[ $count -gt 1 ]]; then`: Checks if the line appears more than once.
   - If true, it echoes the line and the count: `echo "$line appears $count times"`.

6. **Error Message**:
   - If `data.txt` does not exist, it informs the user.







## 20.Ask the user for a file name and a new owner. Change the ownership of the file to the specified new owner.



### Script:
```
#!/bin/bash

# Prompt the user for a file name
read -p "Enter the file name: " filename

# Prompt the user for a new owner
read -p "Enter the new owner: " new_owner

# Check if the file exists
if [[ -f "$filename" ]]; then
    # Change the ownership of the file
    sudo chown "$new_owner" "$filename"
    
    # Confirm the ownership change
    echo "Ownership of '$filename' changed to '$new_owner'."
else
    # Inform the user if the file does not exist
    echo "'$filename' does not exist."
fi
```

### Explanation:
1. **User Prompts**:
   - The script prompts the user for the file name and the new owner's username, storing these in `filename` and `new_owner`, respectively.

2. **File Existence Check**:
   - The condition `if [[ -f "$filename" ]]; then` checks if the specified file exists and is a regular file.

3. **Change Ownership**:
   - `sudo chown "$new_owner" "$filename"`: This command changes the file's ownership to the specified new owner. The use of `sudo` allows for changing ownership when necessary permissions are required.

4. **Success Confirmation**:
   - If the ownership change is successful, a confirmation message is displayed.

5. **Error Handling**:
   - If the file does not exist, the user is informed accordingly.


```


Here are the scripts from questions 21 to 37, now with detailed comments explaining each command and part of the command:

### 21. Find Directories Larger Than a Specified Size
```bash
#!/bin/bash

# Prompt for size in GB
read -p "Enter the minimum size in GB: " min_size

# Find directories larger than specified size
find . -type d -exec du -sh {} + | awk -v min_size="$min_size" '
    # Process each line
    $1 ~ /G/ && $1+0 > min_size {print $0}
'
# - find .: Search in the current directory.
# - -type d: Only find directories.
# - -exec du -sh {} +: For each found directory, execute 'du -sh' to get its size in human-readable format.
# - awk: A text processing tool used to filter results.
# - $1 ~ /G/: Check if the size ends with 'G' (GB).
# - $1+0 > min_size: Compare the numerical value of the size with the specified minimum.
```

---

### 22. Monitor a Directory for Changes
```bash
#!/bin/bash

# Specify the directory to monitor
read -p "Enter the directory to monitor: " dir

# Monitor the directory and log changes
inotifywait -m -r -e create,delete,modify "$dir" --format '%w%f %e' >> changes.log
# - inotifywait: Command to watch for file system changes.
# - -m: Monitor continuously.
# - -r: Watch directories recursively.
# - -e create,delete,modify: Specify events to watch (file creation, deletion, and modification).
# - --format '%w%f %e': Format the output to include the full path and event type.
# - >> changes.log: Append output to the log file.
```

---

### 23. Compare Two Files
```bash
#!/bin/bash

# Ask for two file names
read -p "Enter the first file name: " file1
read -p "Enter the second file name: " file2

# Compare the files
if diff -q "$file1" "$file2" > /dev/null; then
    echo "The files are identical."
else
    echo "The files are different."
    diff "$file1" "$file2" # Show differences if they are not identical
fi
# - diff: Command to compare files.
# - -q: Quiet mode, only report if files differ.
# - > /dev/null: Redirect output to null, suppressing it.
```

---

### 24. List Files and Permissions
```bash
#!/bin/bash

# Specify the directory
read -p "Enter the directory: " dir

# List files and their permissions
ls -l "$dir" | awk '{print $1, $9}'
# - ls -l: List files with detailed information, including permissions.
# - awk '{print $1, $9}': Print the first column (permissions) and the ninth column (file name).
```

---

### 25. Search for Lines Matching a Regex
```bash
#!/bin/bash

# Ask for a regex and a file name
read -p "Enter a regular expression: " regex
read -p "Enter the file name: " file

# Search and display matching lines
grep -E "$regex" "$file"
# - grep: Command to search text using patterns.
# - -E: Enable extended regular expressions.
```

---

### 26. Summary Report of .log Files
```bash
#!/bin/bash

# Initialize total line count and size
total_lines=0
total_size=0

# Loop through .log files
for file in *.log; do
    if [ -f "$file" ]; then
        lines=$(wc -l < "$file") # Count lines in the file
        size=$(stat -c%s "$file") # Get the file size in bytes
        echo "$file: $lines lines, $size bytes" # Display file info
        total_lines=$((total_lines + lines)) # Accumulate total lines
        total_size=$((total_size + size)) # Accumulate total size
    fi
done

# Print total summary
echo "Total: $total_lines lines, $total_size bytes"
# - wc -l: Count the number of lines in a file.
# - stat -c%s: Get the size of a file in bytes.
```

---

### 27. List Files with a Specific Extension and Prompt for Deletion
```bash
#!/bin/bash

# Ask for a directory and file extension
read -p "Enter the directory: " dir
read -p "Enter the file extension (e.g., .txt): " ext

# List files with the specified extension
files=("$dir"/*"$ext") # Collect files with the specified extension
for file in "${files[@]}"; do
    if [ -f "$file" ]; then
        read -p "Do you want to delete $file? (y/n) " choice # Ask for confirmation
        if [[ $choice == 'y' ]]; then
            rm "$file" # Remove the file
            echo "$file deleted."
        fi
    fi
done
# - "$dir"/*"$ext": Expand to all files with the specified extension.
# - rm: Command to delete files.
```

---

### 28. Count Occurrences of a Specific Word
```bash
#!/bin/bash

# Ask for the directory and the word
read -p "Enter the directory: " dir
read -p "Enter the word to count: " word

# Count occurrences per file
for file in "$dir"/*; do
    if [ -f "$file" ]; then
        count=$(grep -o -i "$word" "$file" | wc -l) # Count occurrences of the word
        echo "$file: $count occurrences" # Display the count
    fi
done
# - grep -o -i: Search for the word, print each match on a new line, and ignore case.
# - wc -l: Count the number of lines (which are now individual matches).
```

---

### 29. Find Broken Symbolic Links
```bash
#!/bin/bash

# Ask for the directory
read -p "Enter the directory to search for broken links: " dir

# Find and list broken symbolic links
find "$dir" -type l ! -exec test -e {} \; -print
# - find "$dir": Search in the specified directory.
# - -type l: Only find symbolic links.
# - ! -exec test -e {} \;: Test if the link does not point to a valid file.
# - -print: Display the broken links.
```

---

### 30. Encrypt a File
```bash
#!/bin/bash

# Ask for the file name and encryption method
read -p "Enter the file name to encrypt: " file
read -p "Enter the encryption method (e.g., openssl aes-256-cbc): " method

# Encrypt the file
$method -in "$file" -out "$file.enc"
echo "File '$file' has been encrypted as '$file.enc'."
# - $method: The encryption command specified by the user.
# - -in: Specify the input file to encrypt.
# - -out: Specify the output encrypted file.
```

---

### 31. Update File Permissions
```bash
#!/bin/bash

# Ask for a file name and permission mode
read -p "Enter the file name: " file
read -p "Enter the permission mode (e.g., 755): " mode

# Update permissions
chmod "$mode" "$file"
echo "Permissions for '$file' have been updated to '$mode'."
# - chmod: Command to change file permissions.
# - "$mode": The new permission mode specified by the user.
```

---

### 32. Find Files Containing a Search Term
```bash
#!/bin/bash

# Ask for search term and file extension
read -p "Enter the search term: " term
read -p "Enter the file extension: " ext

# Find and archive matching files
zip search_results.zip *"$ext" -x *"$term"* 
# - zip: Command to create a zip archive.
# - *"$ext": Match files with the specified extension.
# - -x *"$term": Exclude files that contain the search term.
```

---

### 33. List Files Sorted by Modification Time
```bash
#!/bin/bash

# Ask for a directory
read -p "Enter the directory: " dir

# List files sorted by modification time
ls -lt "$dir" | grep '^-' | awk '{print $9}'
# - ls -lt: List files sorted by modification time (newest first).
# - grep '^-': Filter out only files (exclude directories).
# - awk '{print $9}': Print the file names.
```

---

### 34. Count "failed" Lines in a Log File
```bash
#!/bin/bash

# Specify the log file
log_file="server.log"

# Count lines containing "failed" but not "successful"
count=$(grep "failed" "$log_file" | grep -v "successful" | wc -l)
echo "Count of lines with 'failed': $count"
# - grep "failed": Search for lines containing the word "failed".
# - grep -v "successful": Exclude lines containing the word "successful".
# - wc -l: Count the number of matching lines.
```

---

### 35.

 List Files Modified in the Last 7 Days
```bash
#!/bin/bash

# List files modified in the last 7 days in the user's home directory
find ~ -type f -mtime -7 -exec ls -l {} \;
# - find ~: Search in the user's home directory.
# - -type f: Only find files.
# - -mtime -7: Find files modified in the last 7 days.
# - -exec ls -l {} \;: For each found file, execute 'ls -l' to list its details.
```

---

### 36. Create a Compressed Backup of a Directory
```bash
#!/bin/bash

# Ask for the directory name
read -p "Enter the directory name to back up: " dir

# Create a compressed backup
tar -czf "backup_$(date +%Y%m%d).tar.gz" "$dir"
echo "Backup of '$dir' created as 'backup_$(date +%Y%m%d).tar.gz'."
# - tar: Command to create an archive.
# - -czf: Options to create (c), compress with gzip (z), and specify the output file (f).
# - $(date +%Y%m%d): Use the current date in YYYYMMDD format for the filename.
```

---

### 37. Find Duplicate Files by Content
```bash
#!/bin/bash

# Ask for the directory
read -p "Enter the directory to search for duplicate files: " dir

# Find duplicate files based on content
find "$dir" -type f -exec md5sum {} + | sort | uniq -w32 -dD
# - find "$dir": Search in the specified directory.
# - -type f: Only find regular files.
# - -exec md5sum {} +: Calculate and print the MD5 hash for each file.
# - sort: Sort the output to group duplicate hashes together.
# - uniq -w32 -dD: Find duplicates based on the first 32 characters (the hash) and print them.
```

---

