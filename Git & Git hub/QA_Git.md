

### Basic Questions
1. **What is Git?**
   - A distributed version control system that allows collaboration without overwriting changes.

2. **Difference between repository and branch?**
   - A repository stores project files and history; a branch is a pointer to a specific commit for isolated development.

3. **Purpose of `.gitignore`?**
   - Specifies files/directories that Git should ignore, like temporary files or sensitive data.

### Intermediate Questions
4. **Create and switch to a new branch?**
   - Use `git checkout -b <branch-name>`.

5. **What is a merge conflict?**
   - Occurs when changes in different branches clash; resolve by editing the conflicting files and committing.

6. **Difference between `git fetch` and `git pull`?**
   - `git fetch` updates your local copy; `git pull` fetches and merges changes into your current branch.

### Advanced Questions
7. **What is a Git tag?**
   - A marker for specific commits, often used for releases.

8. **Purpose of rebasing?**
   - Re-applies commits on another branch to maintain a linear history; useful for cleaner project logs.

9. **Revert a pushed commit?**
   - Use `git revert <commit-hash>` to create a new commit that undoes the changes.

### GitHub-Specific Questions
10. **What are GitHub Actions?**
    - Automate workflows for CI/CD directly in GitHub.

11. **Create a pull request?**
    - Push your branch and use the "Pull Requests" tab to compare and submit.

12. **Significance of forking?**
    - Creates a personal copy of a repo for experimentation without affecting the original.

### Scenario-Based Questions
13. **Handle simultaneous edits?**
    - Resolve merge conflicts by manually editing the file and committing the combined changes.

14. **Use Git to solve a problem?**
    - Implemented feature toggles to reduce merge conflicts in a team project.

15. **Accidentally committed sensitive info?**
    - Remove it with `git revert`, then clean history using tools like BFG Repo-Cleaner, and notify the team.

Here are some practical Git and GitHub questions you might encounter in an interview, along with concise answers:

### Practical Questions
1. **How do you clone a repository?**
   - **Answer:** Use `git clone <repository-url>` to create a local copy of the repository.

2. **How can you check the status of your Git repository?**
   - **Answer:** Run `git status` to see the current state of the repository, including staged, unstaged, and untracked files.

3. **How do you stage changes to be committed?**
   - **Answer:** Use `git add <file-name>` to stage a specific file, or `git add .` to stage all changes.

4. **What command would you use to view the commit history?**
   - **Answer:** Use `git log` to display the commit history, including commit IDs, authors, and messages.

5. **How do you undo the last commit without losing changes?**
   - **Answer:** Use `git reset --soft HEAD~1` to undo the last commit while keeping the changes staged.

6. **How can you see the differences between your working directory and the last commit?**
   - **Answer:** Run `git diff` to view unstaged changes or `git diff --cached` to see staged changes.

7. **How do you rename a branch?**
   - **Answer:** Use `git branch -m <new-branch-name>` while on the branch you want to rename.

8. **How can you cherry-pick a commit from another branch?**
   - **Answer:** Use `git cherry-pick <commit-hash>` to apply a specific commit from another branch onto your current branch.

9. **What command do you use to push changes to a remote repository?**
   - **Answer:** Use `git push origin <branch-name>` to push your changes to the specified branch on the remote.

10. **How can you view the changes introduced by a specific commit?**
    - **Answer:** Use `git show <commit-hash>` to display the changes made in that commit.




