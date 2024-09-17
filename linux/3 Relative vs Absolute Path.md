

### Relative vs Absolute Path in Linux/Bash

**Absolute Path**:  
An absolute path is the complete path from the root directory (denoted by `/`). It always starts from `/` and points to a location in the file system regardless of the current working directory.  
Example: `/home/user/docs/file.txt`

**Relative Path**:  
A relative path is based on the current working directory and does not start from `/`. It refers to the location relative to where you currently are in the file system. Special symbols like `.` (current directory) and `..` (parent directory) are often used.  
Example: `../docs/file.txt` (navigates one directory up and then into `docs` to find `file.txt`).

---

### Practice Questions:

1. **Navigate to the** `/etc` **directory using an absolute path**:
   ```bash
   cd /etc
   ```

2. **Navigate to the** `/var/log` **directory from** `/home/user/documents` **using a relative path**:
   ```bash
   cd ../../var/log
   ```

3. **Absolute path to** `file1.txt` **located in** `~/mydir/`:
   ```bash
   /home/user/mydir/file1.txt
   ```

4. **Navigate to** `/home/user/pictures` **from** `/home/user/projects` **using an absolute path**:
   ```bash
   cd /home/user/pictures
   ```

5. **Create a file named** `newfile.txt` **in** `/home/user/docs` **using an absolute path**:
   ```bash
   touch /home/user/docs/newfile.txt
   ```

6. **Relative path to move from** `/home/user/documents` **to** `/home/user`:
   ```bash
   cd ..
   ```

7. **Navigate to the parent directory** from the current directory using a relative path:
   ```bash
   cd ..
   ```

8. **List all files in** `/usr/local/bin` **from any directory using an absolute path**:
   ```bash
   ls /usr/local/bin
   ```

9. **Navigate to** `/var/log/apache2` **from** `/var/log` **using a relative path**:
   ```bash
   cd apache2
   ```

10. **Copy a file named** `report.txt` **from** `/home/user/docs` **to** `/home/user/backups` **using absolute paths**:
    ```bash
    cp /home/user/docs/report.txt /home/user/backups/
    ```

11. **Navigate to** `/home/user/docs` **from** `/home/user/docs/reports` **using a relative path**:
    ```bash
    cd ..
    ```

12. **Difference between** `cd /home/user` **and** `cd ~/user`:
    - `cd /home/user` navigates to the **absolute path** `/home/user`.
    - `cd ~/user` is **incorrect** unless there's a directory `user` in your home directory (`~`), which usually refers to `/home/your_username`.

13. **Navigate to** `/usr/local/share` **from** `/usr/local/bin` **using a relative path**:
    ```bash
    cd ../share
    ```

14. **Display the contents of a file named** `config.txt` **located in** `/etc` **using an absolute path**:
    ```bash
    cat /etc/config.txt
    ```

15. **Navigate to** `/home/user/music/rock/classic` **from** `/home/user/music` **using a relative path**:
    ```bash
    cd rock/classic
    ```

---

