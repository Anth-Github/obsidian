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


#unformatted 

whenver you need git documentation files for references, you can go to google and type "git config"
you will get the details. 

we can get the same details on the terminal by typing 
git config --help, press space to go to the next page. and q to exit. 

git config -h for short summary. 

download the cheat sheet from the description of the youtube video. 

git commit 


creating snapshots. 
create a directory for your project. 
mkdir moon. 
cd moon. 
git init. 

initialized empty git repository and the full path is shown. 
by default an empty .git folder is created which you should not touch. it is hidded by default. 
ls 
ls -a
shows the .git file which is hidden by default. 

windows install posh-git for colourful git front end. 
post-git completely optiona; 

rm -rf .git. 
 removes the directory.  this deletes the git repo. 


git init. now that we have the repository. 

Basic, Git workflow: 

creating a commit is taking a snapshot. 

staging area, add the modified files to staging area. permanently store in our repo. 


unstash them if you dont want to upload. 



give me an real example here. 

Tell me more about the staging command 

git commit -m "staging message"


Each commit gets an 
 ID
 Message
 Date/time
 Author
 complete Snapshot. 

How git stores data, tell me more on this!

Staging files, 
echo "standard unix or linux command"

echo hello > file1.txt writing hell to file1 
echo hello > file2.txt 


git status - summary give me an summary of this command here. 
git add file1.txt file2.txt
git add .  adds the entire directory. 

git status - summary give me an summary of this command here. 

echo world >>(append) file1.txt
git status to check the file status. 

use the git status to track the files that have been changed or modified. 


when we used the add command git took the snapshot of that file, when we make new changes to the file these are not captured again. you need to restage the files again. 


git add . 
git add file1.txt 

commiting changes, 
git commit -m "Initial commit"
git commit 


short and long description within  a commit message file. 


commiting best practices. 

it shouldn't be too small or too big. 
commit often, 
5 to 10 times a day. 
as you reach a state you want to record then make a commit. 
fixing a bug, 
each commit should represent a logical separate chain set .
example, bug an typo and in two separate commits. 

make it mean something. 
present tense in the meaning. fixed a bug. 

Skipping the staging area, 
you dont have to stage your files all the time you need. 

echo test >> file1.txt
git commit -am "fix the bug that prevented users from sigining up"

commits all the files with -a flag without the need to add files to the staging. 

removing files, 

rm file2.txt

git status. 

we have one file removed. 

git ls-files, files that are still in the staging area. 

git add file2.txt

git ls-files

git status
git commit -m "removed unused files"

git rm file2.txt 


renaming or moving files: 
file1.txt. 

mv file1.txt main.js
git status. 


git add file1.txt 
git add main.js

git status

git mv main.js file1.js
git status

git commit -m "refactor code"

git ignore, 
echo hello > logs/dev.log

create a file called .gitignore should be in the root of your extension, noname only extension. 

echo logs/ > .gitignore

git status
git add .gitignore
	git commit -m "addgit ignore"


mkdir bin, contains compile source code. 
echo hello > bin/app.bin. 























28:39





Devops, 

























































