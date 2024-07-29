
#git-commands-basic-commands


Certainly! Here's a beginner's guide to essential Git commands, formatted as notes with code examples:

**Git Basics for Beginners**

1. **Initial Setup**
   - Configure your name and email:
     ```
     git config --global user.name "Your Name"
     git config --global user.email "your.email@example.com"
     ```

2. **Starting a Repository**
   - Initialize a new repo:
     ```
     git init
     ```
   - Clone an existing repo:
     ```
     git clone https://github.com/username/repository.git
     ```

3. **Basic Workflow**
   - Check status of your repo:
     ```
     git status
     ```
   - Add files to staging area:
     ```
     git add filename.txt    # Add specific file
     git add .               # Add all changed files
     ```
   - Commit changes:
     ```
     git commit -m "Your commit message"
     ```
   - Push changes to remote repo:
     ```
     git push origin main
     ```

4. **Branches**
   - List all branches:
     ```
     git branch
     ```
   - Create a new branch:
     ```
     git branch new-branch-name
     ```
   - Switch to a branch:
     ```
     git checkout branch-name
     ```
   - Create and switch to a new branch:
     ```
     git checkout -b new-branch-name
     ```
   - Merge a branch into current branch:
     ```
     git merge branch-name
     ```

5. **Updating Local Repository**
   - Fetch changes from remote:
     ```
     git fetch origin
     ```
   - Pull changes from remote:
     ```
     git pull origin main
     ```

6. **Viewing Changes**
   - View changes in working directory:
     ```
     git diff
     ```
   - View commit history:
     ```
     git log
     ```

7. **Undoing Changes**
   - Discard changes in working directory:
     ```
     git checkout -- filename.txt
     ```
   - Unstage a file:
     ```
     git reset HEAD filename.txt
     ```
   - Amend the last commit:
     ```
     git commit --amend
     ```

8. **Remote Repositories**
   - View remote repositories:
     ```
     git remote -v
     ```
   - Add a remote repository:
     ```
     git remote add origin https://github.com/username/repo.git
     ```

Remember:
- Always pull before you push to avoid conflicts.
- Commit often with clear, descriptive messages.
- Use branches for new features or experiments.
- When in doubt, use `git status` to see what's going on.

These commands cover the basics of using Git for version control and collaborating via GitHub. As you become more comfortable, you can explore more advanced Git features and workflows.