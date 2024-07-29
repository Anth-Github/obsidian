https://www.youtube.com/watch?v=8JJ101D3knE

#git

**Version Control System**

- Records changes made to code, stored in a repository
    
- Allows reverting back to previous versions
    

**Old Method**

- Physically storing folders and emailing changes
    
- Manually merging changes into code
    

**Types of Version Control**

- **Centralized**: Single point of failure
    
- **Distributed**: Every team member has a copy of the code (e.g., Git, Mercurial)
    

**Git**

- Most popular, free, open-source, fast, and scalable
    
- Cheap branching and merging
    
- Essential skill to have in your resume
    

**Using Git**

- Command line
    
- Code editor/IDE source control panel (e.g., Git Lens)
    
- Graphical user interfaces (GUIs)
    
- Tools for Windows (e.g., GitKraken, Sourcetree)
    

**Why Command Line?**

- GUI tools have limitations
    
- Command line is always available
    

**Command Line Basics**

- Install Git
    
- Open terminal
    
- Check version: `git --version`
    
- Use Git Bash (born again shell)
    

**Configuring Git**

- **System Level**: All users
    
- **Global**: All repositories of the current user
    
- **Local**: The current repository
    

**Git Config Commands**

- `git config --global user.name "Your Name"`
    
- `git config --global user.email "Your Email"`
    
- `git config --global core.editor "code --wait"` (sets default editor)
    
- `git config --global -e` (opens Git config file in editor)
    
- `git config --global core.autocrlf true` (sets end-of-line format for Windows)
    

**End of Lines**

- `core.autocrlf` config ensures consistent line endings
    
- Example: prevents issues when collaborating between Windows and Linux users
    

**.gitconfig File**

- Stores Git configuration settings

[user]
	name = Anthony Prakash
	email = prakash.anton31@gmail.com

[core]
	editor = code --wait
.autocrlf = true

[alias]
	st = status
	br = branch



This example `.gitconfig` file sets:

- The user's name and email
    
- The default editor to Visual Studio Code with the `--wait` flag
    
- The end-of-line format to `true` (for Windows)
    
- Aliases for common Git commands:
    

- `st` for `status`
    
- `br` for `branch`
    

Note: The `.gitconfig` file is usually located in the user's home directory (e.g., `~/.gitconfig` on Linux/Mac or `C:\Users\YourUsername\.gitconfig` on Windows).

    
- More information: https://git-scm.com/docs/git-config




  
Here are the notes rewritten for clarity and concision, with added explanations and references:

**Git Commands**

- `git status -s`: Displays a short summary of the repository status, showing modified, staged, and untracked files.
    

**Initializing a Git Repository**

1. Create a new directory for your project: `mkdir moon`
    
2. Navigate into the directory: `cd moon`
    
3. Initialize a new Git repository: `git init`
    

**Basic Git Workflow**

1. **Staging**: Add modified files to the staging area using `git add <file>` or `git add .` to stage all changes.
    
2. **Committing**: Create a snapshot of the staged changes using `git commit -m "<commit message>"`
    

**Staging Files**

- `echo "hello" > file1.txt`: Creates a new file with the content "hello"
    
- `git add file1.txt`: Stages the new file
    
- `git status -s`: Shows the file as staged
    

**Committing Changes**

- `git commit -m "Initial commit"`: Creates a new commit with the message "Initial commit"
    
- `git commit`: Opens a text editor to write a commit message
    

**Commit Best Practices**

- Commit often (5-10 times a day)
    
- Each commit should represent a logical, separate change set
    
- Use present tense in commit messages (e.g., "Fix bug")
    
- Keep commits concise, but not too small or too big
    

**Skipping the Staging Area**

- `git commit -am "Fix bug"`: Commits all changes without staging them first
    

**Removing Files**

- `rm file2.txt`: Deletes the file
    
- `git status`: Shows the file as deleted
    
- `git add file2.txt`: Stages the deletion
    
- `git commit -m "Removed unused files"`: Commits the deletion
    

**Renaming or Moving Files**

- `mv file1.txt main.js`: Renames the file
    
- `git status`: Shows the file as renamed
    
- `git add main.js`: Stages the rename
    
- `git mv main.js file1.js`: Renames the file using Git
    
- `git commit -m "Refactor code"`: Commits the rename
    

**Git Ignore**

- Create a `.gitignore` file in the root directory to ignore files or directories, with no filename just the extension
    
- `echo logs/ > .gitignore`: Ignores the `logs` directory
    
- `git add .gitignore`: Stages the `.gitignore` file
    
- `git commit -m "Add git ignore"`: Commits the `.gitignore` file


github/gitignore, you can have base templates for gitignore for different languages. 

Note: For more information on Git commands, you can use `git <command> --help` or visit the official Git documentation by searching for "git <command>" on Google.

**Short Status**

- `git status -s`: Displays a short summary of the repository status, showing modified, staged, and untracked files.
    

**Viewing Changes**

- `git status`: Displays the status of the repository, including modified and untracked files.
    
- `git status -s`: Displays a short summary of the status.
    
- `git diff --staged`: Shows the changes between the staging area and the last commit.
    

**Visual Diff Tools**

- `kdiff3`, `p4Merge`, and `winMerge` are tools for visually comparing file changes.
    

**Viewing History**

- `git log`: Displays the commit history.
    
- `git log --oneline`: Displays a concise version of the commit history, showing only the commit message.
    
- `git log --oneline --reverse`: Displays the commit history in reverse order.
    
- `git show <commit_id>`: Displays the details of a specific commit.
    
- `git show HEAD~1`: Displays the details of the previous commit.
    
- `git ls-tree HEAD~1`: Displays the file tree of the previous commit.
    

**Unstaging Files**

- `git restore --staged <file>`: Unstages a file, moving it from the staging area to the working directory.
    

**Discarding Local Changes**

- `git restore <file>`: Discards local changes to a file, reverting it to the last committed version.
    
- `git clean`: Removes untracked files and directories.
    
**Restoring a File to an Earlier Version**:

When working with Git, it's common to make changes to files and then realize you want to revert to a previous version. Git provides a way to restore a file to an earlier version using the `git restore` command.

**Syntax:**

`git restore --source=<commit_id> <file>`

**Explanation:**

- `--source=<commit_id>`: Specifies the commit ID from which to restore the file. You can find the commit ID using `git log`.
    
- `<file>`: Specifies the file to restore.
    

**Example:**

Suppose you've made changes to `file1.js` and want to restore it to the version from commit `d601b90`.

1. Find the commit ID: `git log`
    
2. Copy the commit ID: `d601b90`
    
3. Run the restore command: `git restore --source=d601b90 file1.js`
    

This will restore `file1.js` to the version from commit `d601b90`, overwriting any local changes.

**Alternative:**

You can also use `git checkout` to restore a file to an earlier version:

`git checkout <commit_id> -- <file>`

This command is similar to `git restore`, but it checks out the file from the specified commit, whereas `git restore` restores the file from the specified commit.

**Important Notes:**

- `git restore` and `git checkout` will overwrite local changes. Make sure to commit or stash your changes before restoring a file.
    
- If you want to restore multiple files, separate them with spaces: `git restore --source=<commit_id> file1.js file2.js`
    

By using `git restore` or `git checkout`, you can easily revert files to earlier versions, making it a powerful tool for managing changes in your Git repository.

Video completed. 


























































