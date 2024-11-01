
# Git and GitHub Notes

## Configuration
Set up your Git environment:
```bash
git config --global user.name "ashutosh"
git config --global user.email "ashutosh@gmail.com"
```

### Show Configuration Information
To view your configuration:
```bash
git config --list
```

---

## Cloning a Repository
Clone a repository to your local machine:
```bash
git clone http://github.com/ashutosh/a
```

### Show Files
- List files: `ls`
- List hidden files: `ls -a`

### Check Repository Status
Display the state of your code:
```bash
git status
```

**States:**
1. **Untracked:** New files not yet tracked by Git.
2. **Modified:** Files that have been changed.
3. **Staged:** Files ready to be committed.
4. **Unmodified:** Files that haven't changed.

---

## Adding and Committing Changes
### Add Changes
To stage specific files:
```bash
git add <file_name>
```
To stage all changes:
```bash
git add .
```

### Commit Changes
Record your changes:
```bash
git commit -m "Your commit message"
```

---

## Pushing Changes
Upload local repository content to the remote repository:
```bash
git push origin main
```

---

## Initializing a Repository
Create a new Git repository:
```bash
git init
git remote add origin <link>
```
Verify the remote:
```bash
git remote -v
```

---

## Branch Management
### Branch Commands
- Check current branches: `git branch`
- Rename branch: `git branch -M main`
- Switch to a branch: `git checkout <branch_name>`
- Create a new branch: `git checkout -b <new_branch_name>`
- Delete a branch: `git branch -d <branch_name>`

---

## Merging Code
### Merging Branches
1. Compare branches:
   ```bash
   git diff <branch_name>
   ```
2. Merge branches:
   ```bash
   git merge <branch_name>
   ```

### Pull Request (PR)
Create a PR to notify others about changes pushed to a branch in a repository on GitHub.

---

## Pull Command
Fetch and download content from a remote repository and update your local repository:
```bash
git pull origin main
```

---

## Merge Conflicts
Occur when Git cannot automatically resolve differences between two commits.

---

## Undoing Changes
### For Staged Changes
Unstage a file:
```bash
git reset <file_name>
```

### For Committed Changes
- Undo last commit:
  ```bash
  git reset HEAD~1
  ```
- Undo multiple commits:
  ```bash
  git reset <commit_hash>
  git reset --hard <commit_hash>
  ```

---

## Forking a Repository
A fork is a copy of a repository allowing you to make changes without affecting the original.

---

## Workflow Diagram
```
GitHub Repo → Clone → Changes → Add → Commit → Push
```

## Branching Diagram
```
          main
           |
    --------|--------
    branch1 | branch2
           ...
```

## Merging Diagram
```
  Branch A      Branch B
      |             |
      |             |
      -------------
            |
         Merge
```

---

## Basic Things to Know as a Cloud Engineer
1. **Version Control:** Track changes in code.  
   *Example:* Use `git commit` to save changes.

2. **Branching and Merging:** Manage feature development.  
   *Example:* Create a new branch with `git checkout -b feature-x`.

3. **Collaboration:** Contribute to projects using forks and PRs.  
   *Example:* Fork a repo, make changes, and submit a PR.

4. **CI/CD Integration:** Automate testing and deployment.  
   *Example:* Connect your repo to a CI tool like GitHub Actions.

5. **Remote Repositories:** Work with platforms like GitHub.  
   *Example:* Push changes to GitHub using `git push origin main`.

---
```
