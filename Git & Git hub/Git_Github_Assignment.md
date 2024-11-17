# Git Github
## Q1 
Create a local git repository. Create a file by name index.html. Type 2 lines in it. Perform commit. Modify index.html file and add 2 more lines. Perform commit. Modify the file again and add 2 more line. Restore the earlier verison of the file with 4 lines. Modify file again and 3 lines. Perform commit. Restore 4 line version of the file.

 1)  Initialize Git Repository:
 ```
 git init

 ```

 2) Create index.html and add 2 lines:

```
echo -e "ashutosh \n gangurde" >> index.html
// -e for the  flag tells echo to interpret escape sequences

vim index.html
```
```
<html>
<head></head>
<body>

<p>New Line 1</p>
<p>New Line 2</p>

</body>
</html>

```

 3) Stage and Commit:
 ```
git add index.html
git commit -m "Add index.html with 2 lines"

 ```

 4) Modify index.html and add 2 more lines:
 ```
 vim index.html

<p>New Line 3</p>
<p>New Line 4</p>

 ```

 5) Stage and Commit:
 ```
git add index.html
git commit -m "Add 2 more lines to index.html"

 ```
 6)  Modify index.html again and add 2 more lines:
 ```
 vim index.html

 ```
 ```
<p>New Line 4</p>
<p>New Line 5</p>

 ```
 7) Stage and Commit the new changes:
 ```
git add index.html
git commit -m "Add 2 more lines (total 4) to index.html"

 ```
 8) Restore the earlier version of the file (with 4 lines):
 ```
 git checkout HEAD~1 index.html

 ```
 - The term HEAD~1 in Git refers to the previous commit relative to the current commit (i.e., one commit behind HEAD)

9) Modify the file again and add 3 lines:
```
vim index.html

<p>New Line 5</p>
<p>New Line 6</p>
<p>New Line 7</p>

```
10. Stage and Commit the new changes:
```
git add index.html
git commit -m "Add 3 new lines to index.html"

```

11. Restore the 4-line version of the file:

```
git checkout HEAD~3 index.html

```


---

## Q2
Create a repository by name lab4 on the Github. Create a file by name 
results.txt in it. Type some thing into it. Then clone this repository on the local 
machine. Modify the results.txt file locally. Then push the modifications to the 
remote repository.  

### Step 1: Create a Repository on GitHub
1. Go to [GitHub](https://github.com).
2. Click on **New** to create a new repository.
3. Name the repository `lab4`.
4. Initialize the repository (no README required for now) and click on **Create repository**.

### Step 2: Add a File `results.txt` to the Repository
1. In your newly created GitHub repository, click on **Add file** > **Create new file**.
2. Name the file `results.txt`.
3. Add some content, for example:

   ```
   Initial content in results.txt
   ```

4. Commit the file with a message such as "Add results.txt with initial content".

### Step 3: Clone the Repository to Your Local Machine
Open a terminal and clone the repository using the following command:

```bash
git clone https://github.com/ASHUTOSH-SG/lab4.git
cd lab4
```

### Step 4: Modify the `results.txt` File Locally
1. Open the `results.txt` file in your preferred text editor.
2. Modify the content as needed, for example:

   ```
   Updated content in results.txt
   ```

3. Save the changes.

### Step 5: Stage, Commit, and Push Changes to GitHub

1. Check the status of the repository to see what’s changed:

   ```bash
   git status
   ```

2. Stage the changes:

   ```bash
   git add results.txt
   ```

3. Commit the changes:

   ```bash
   git commit -m "Updated content in results.txt"
   ```

4. Push the changes to the remote GitHub repository:

   ```bash
   git push origin main
   ```

---

### Why Conflicts Happen
- **Simultaneous Edits**: Conflicts happen when two people edit the same part of a file at the same time (e.g., both modify the same line of text in a file).

### How to Resolve Conflicts

1. **Identify the Conflicted File**: Git will inform you of the files that are in conflict.
2. **Manually Edit**: Open the conflicted file(s) in a text editor. Git marks the conflicts in the file with special markers (`<<<<<<<`, `=======`, `>>>>>>>`). Choose which changes to keep and remove the markers.
3. **Stage the Resolved File**: After resolving the conflict, mark the file as resolved:

   ```bash
   git add results.txt
   ```

4. **Commit the Resolution**:

   ```bash
   git commit -m "Resolved conflict in results.txt"
   ```

5. **Push the Changes**: Finally, push the resolved file back to GitHub:

   ```bash
   git push origin main
   ```

---

## Q3
Create a local repository in a directory named hpcsa. Create a file and commit. Create 
a new repository on Github by name demo1. Link the local repository to the remote 
repository. Perform git pull. Create a new file by name index.html on local repository 
and then push it to the remote demo1 repostiroty. 


### Step 1: Create and Initialize a Local Repository

1. Create a directory for your project and initialize it as a Git repository:

   ```bash
   mkdir hpcsa
   cd hpcsa
   git init
   ```

### Step 2: Create a File and Commit

1. Create a new file, for example, `file.txt`:

   ```bash
   echo "Initial file content" > file.txt
   ```

2. Stage and commit the file:

   ```bash
   git add file.txt
   git commit -m "Initial commit with file.txt"
   ```

### Step 3: Create a GitHub Repository

1. Go to [GitHub](https://github.com) and create a new repository called `demo1`.

### Step 4: Link the Local Repository to the Remote

1. Link your local repository to the newly created GitHub repository:

   ```bash
   git remote add origin https://github.com/your-username/demo1.git
   ```

### Step 5: Pull Remote Changes

1. Pull changes from the remote repository to make sure your local copy is up to date:

   ```bash
   git pull origin main
   ```

### Step 6: Create a New File (`index.html`)

1. Create a new file called `index.html`:

   ```bash
   echo "<!DOCTYPE html><html><head><title>Demo</title></head><body><h1>Welcome to Demo1</h1></body></html>" > index.html
   ```

2. Stage and commit the new file:

   ```bash
   git add index.html
   git commit -m "Add index.html"
   ```

### Step 7: Push the File to GitHub

1. Push the newly created `index.html` file to GitHub:

   ```bash
   git push origin main
   ```

---

Now your local repository is linked to the GitHub repository, and you've successfully pushed a new file (`index.html`) to the remote repository `demo1`.

---

# Git Notes InterviewBit

## What is Git and Why is it Used?

- **Git** is a popular open-source **distributed version control system (DVCS)**.
- It helps developers track project changes and collaborate efficiently, especially in team settings.
- Git allows developers to identify changes made by others, revert to previous working versions, and fix bugs.

## Git Cheat Sheet: Basic to Advanced Concepts

### 1. **Git Repository**
   - A **repository** is a storage location where Git stores all project files.
   - It can be local (on your machine) or remote (on a server like GitHub).

### 2. **git clone**
   - `git clone` creates a **copy** (clone) of an existing repository, typically from a remote server to your local machine.

### 3. **git config**
   - `git config` sets repository configurations such as user info.
   - Example:
     ```bash
     git config --global user.name "Your Name"
     git config --global user.email "your_email@example.com"
     ```

### 4. **HEAD in Git**
   - **HEAD** refers to the last commit of the current branch.
   - You can have **multiple heads** in a repository (e.g., one per branch).
   - Common commands involving HEAD:
     - `git checkout HEAD~1` – Go to the previous commit.
     - `git reset HEAD~3` – Uncommit the last 3 commits without losing changes.
     - `git reset --hard HEAD~3` – Remove the last 3 commits and their changes.
     - `git revert --no-commit HEAD~3...HEAD` – Revert the last 3 commits.

### 5. **What is a Conflict?**
   - A **conflict** happens when Git cannot automatically merge changes:
     - Two branches modify the same line in a file.
     - A file is deleted in one branch but modified in another.
   - Conflicts must be resolved manually.

### 6. **git ls-tree**
   - `git ls-tree` shows the tree structure of the repository with file modes, names, and SHA-1 hash values.



## 7. **What does `git status` command do?**
- The `git status` command shows the difference between the working directory and the index (staging area).
- It helps track which files are **staged**, **modified**, or **untracked**.

## 8. **What is the Index?**
- The **Index** (or **Staging Area**) is where changes are prepared before committing them to the repository.
- You can review, format, or add new changes in this area before making a commit.

## 9. **What does `git add` command do?**
- The `git add` command stages changes for commit.
  - `git add .` – Adds all changes (new, modified, deleted files).
  - `git add <file_name>` – Adds a specific file.
  - `git add /<folder_name>/` – Adds changes from a folder.

## 10. **What is a Version Control System (VCS)?**
- A **VCS** tracks code changes made by developers working on a project.
- It helps manage the project’s evolution, allowing developers to safely add new code, fix bugs, and revert to previous versions if necessary.

---

## Intermediate Git Interview Questions

### 1. **How to Squash Multiple Commits into One?**
- Use the command:  
  ```bash
  git rebase -i HEAD~N
  ```
  Replace `N` with the number of commits you want to squash. This combines multiple commits into a single commit.

### 2. **How to Recover a Deleted Branch?**
- If a branch is deleted, recover it using the reflog:
  ```bash
  git reflog
  git checkout -b <branch_name> <commit_hash>
  ```

### 3. **What is `git reflog`?**
- `git reflog` keeps track of the history of changes made to the repository's references (branches/tags).
- It shows every change made (like checkouts or commits) and can be used to recover lost branches.

### 4. **What Does a Commit Object Contain?**
- A **commit object** includes:
  - The state of the project files.
  - A reference to the parent commit.
  - A 40-character SHA-1 hash.

### 5. **Git Config Levels**
- Git uses three configuration levels:
  1. **System** (`/etc/gitconfig`) – Applied system-wide.
  2. **Global** (`~/.gitconfig`) – Applied to the current user.
  3. **Local** (`.git/config`) – Applied only to the current repository.

### 6. **What is a Detached HEAD?**
- A **detached HEAD** occurs when you're working directly with a commit, tag, or an unattached branch (not the latest commit of a branch).
- To avoid it, create a new branch from the current commit using:  
  ```bash
  git checkout -b <new_branch_name>
  ```

### 7. **What Does `git annotate` Do?**
- `git annotate` (or `git blame`) annotates each line of a file with the commit details (who and when changed it).

### 8. **Difference Between `git stash apply` and `git stash pop`**
- **`git stash apply`** applies stashed changes but keeps them in the stash list.
- **`git stash pop`** applies stashed changes and removes them from the stash list.

### 9. **What Do `git diff` and `git status` Do?**
- **`git diff`** shows differences between commits, working directory, and the index.
- **`git status`** shows which files have been modified or staged.

### 10. **Why is Git Easy to Use?**
- **Branching:** Allows working on multiple branches, improving development flow.
- **Distributed System:** Every developer has a full repository, which makes the project more scalable and fault-tolerant.
- **Pull Requests:** Makes collaboration smoother by tracking changes and discussions.
- **Effective Release Cycle:** Git speeds up release cycles and integrates features with ease.

---

## Additional Git Commands

### 11. **Creating a Git Repository**
- To create a new repository, navigate to the project folder and run:
  ```bash
  git init
  ```

### 12. **What is `git stash`?**
- `git stash` temporarily saves your changes to allow switching branches without losing work.
  - Retrieve stashed changes using `git stash apply`.

### 13. **How to Delete a Branch?**
- Delete a **local branch**:
  ```bash
  git branch -d <branch_name>
  ```
- Delete a **remote branch**:
  ```bash
  git push origin --delete <branch_name>
  ```

### 14. **Difference Between `git remote` and `git clone`**
- **`git remote`** adds a URL for a remote repository.
- **`git clone`** copies an existing repository to your local machine.

### 15. **What is `git pull` vs. `git fetch`?**
- **`git pull`**: Fetches and merges changes from the remote repository.
- **`git fetch`**: Fetches changes but doesn’t merge them. You need to run `git merge` manually.

### 16. **Difference Between Pull Request and Branch**
- **Pull Request**: A request to merge changes from one branch to another.
- **Branch**: A separate line of development in a Git repository.

### 17. **Why "Pull Request" and Not "Push Request"?**
- A **pull request** is made to request the target repository to "pull" your changes.
- A **push request** would imply you are pushing your changes to the target repository, which is not the case in Git-based workflows.

### 18. **Difference Between Git and GitHub**
| **Git** | **GitHub** |
| --- | --- |
| A distributed version control system. | A cloud-based platform to host Git repositories. |
| Used locally on your machine. | A web service to manage Git repositories. |
| Git is open-source. | GitHub is owned by Microsoft. |

