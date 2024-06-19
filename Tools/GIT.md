# GIT


## Inteview Questions

1.	How do you check the Git version?
2.	What is the command to configure your username globally in Git?
3.	How can you configure your email globally in Git?
4.	How does Git handle passwords? What methods are used for authentication?
5.	What command can be used to check the existing username from the global configuration?
6.	What command is used to clone a project from a repository URL?
7.	How do you initialize Git for a project?
8.	What command is used to check the status of your Git repository?
9.	What are the different areas in Git before committing, and what do they represent?
10.	How can you untrack unmodified, modified, and staged files in Git?
11.	How do you add a new file to the staging area in Git?
12.	What is the command to commit a new file along with a commit message?
13.	How do you check the commit logs in Git?
14.	How can you check a specific number of commit logs in Git?
15.	What command is used to check the changes between the staging area and the local file?
16.	How do you compare the changes between the staging area and the last commit?
17.	What is the command to remove a file from the Git directory?
18.	How do you create a new file in Git using the command line?
19.	What is the command to create a new branch in Git?
20.	How can you check the list of branches in Git?
21.	How do you switch from one branch to another branch in Git?
22.	What is the command to switch to a new branch and create it simultaneously?
23.	How do you merge branches in Git?
24.	How do you add a remote repository named "origin" in Git?
25.	What command is used to check the repository URLs for push and pull in Git?
26.	How do you push changes to a remote repository in Git?
27.	How do you pull changes from a remote repository to your local repository in Git?
28.	What is the difference between Git merge and Git rebase?
29. How to sink new updates from remote master branch to local master branch? 
30. How do you revert a commit in Git?
31. What is the difference between Git pull and Git fetch?

<!---
1.	Check the git version: git --version
2.	Configure username: git config --global user.name "Your Username"
3.	Configure email: git config --global user.email "your@email.com"
4.	Configure password: Git does not store passwords directly. It uses different authentication methods, such as SSH keys or credential managers, to handle passwords securely.
5.	Check the existing username from configuration: git config --global user.name
6.	Clone the project: git clone <repository_url> (no need to initlize)
7.	How to initialize git: git init
8.	Check status: git status
9.	What are the != areas in git before commit:   
The different areas in Git before committing are:
•	Working Directory: The current state of your files on disk.
•	Staging Area (Index): A place where you can prepare and stage changes before committing them.
•	Local Repository: The commit history and the current committed snapshot.
    Commit area
10.	Untrack unmodified, modified, and staged files: git reset \<file>
11.	How to add a new file to staging:  
 git add \<file>
12.	How to commit a new file with a message:  
 git commit -m "Commit message"
13.	check logs:   
  git log
14.	Check the specific nuber of commit logs:  
 git log -p -1
15.	Check the changes between staging and local file: git diff
16.	Check the changes between staging and the last commit: git diff --staged
17.	Remove a file from the Git directory: git rm \<file>
18.	Create a file from Git: touch filename
19.	Create a branch: git branch \<branch_name>
20.	Check branch: git branch
21.	Switch from one branch to another branch: git checkout <branch_name>
22. switch and create new branch : git checkout -b branchname
22.	Merge the branch: First, switch to the branch you want to merge into and then run git merge <branch_to_merge>
23.	Add origin: git remote add origin <repository_url>
24.	Check push or pull repository URL: git remote -v
25.	Push: git push \<remote> \<branch> ->  
git push origin master
26.	Pull: git pull \<remote> \<branch>  ->  
 git pull origin master

what is the difference between git merge and git rebase? 

When using git merge, the history of the feature branch is not stored in the master branch.
Git creates a new merge commit that combines the changes from the feature branch into the master branch, resulting in a different commit.

Q. When using git rebase, the commits of the feature branch are rewritten on top of the master branch.
The history of the feature branch is preserved, and the commits from the feature branch are moved to appear as if they were made on top of the latest master commit.


Q. how to sink new updates from remote master branch to local master branch? 
git checkout master
git fetch origin (Fetch the latest changes from the remote repository)
git merge origin/master (Merge the fetched changes into the local master branch)
or else 
git pull origin master
 
How do you revert a commit in Git?
git revert \<commit>  
git push

What is the difference between Git pull and Git fetch?
git fetch is used to update your local repository's knowledge of the remote repository without modifying your working directory, while git pull is used to fetch and merge the changes from the remote repository into your current branch.

How to resolve a merge conflict using IntelliJ:
The biggest problem faced when multiple people are working on the same project is a merge conflict.

If the same file is edited by two or more people, a merge conflict occurs and needs to be resolved before pushing the code to GitHub.

When attempting to pull or merge, an error message is encountered, indicating that the head is different and requesting the latest code to be pulled from upstream.

Pull the latest code using the UI plugin provided by IntelliJ to better resolve the conflict. The plugin displays the branches and files with merge conflicts, allowing for a clearer understanding of the changes to accept.

Choose to use the merge tool provided by IntelliJ, which runs the "git merge" command in the background. Click on "Merge."

The merge tool opens and displays the differences between the local changes, the file with a common head (from both local and remote), and the file from the remote containing changes made by Person B2.

Update the file in the center, taking the changes from either side using the double arrow buttons or manually copying the desired changes.

Choose to keep both changes if necessary and click "Apply."
Add and commit the resolved merge conflict with a message like "Resolved merge conflict."
Push the changes to update the remote branch, in this case, the master branch.
Verify the updates on the remote repository to confirm the successful resolution of the merge conflict.
--->
---
```java
git --version

To initialize git
git init   

To set username
git config --global user.name ‘newusername’

To check username
git config --global user.name

Similarly password and email can also be set:
git config --global user.password 
git config --global user.email

Phases of any file with git:
Untracked area
Untracked to staged 
Stage to commit area

Staged area:
Just before you commit your changes 

Repository / commit changes:
After committing staged area changes, push changes to repository

git status

git add -A    |  git add .
All files from current directory

git add nameofthefile.txt

Commit:
git commit -m “first commit” 

To check the last commits:
git log

Show the changes between local file and git repository file:
git diff 

Show the changes between staged file and git repository file:
git diff  --staged

Will undo changes in local file and will load the git repository file:
git checkout -f

git branch
git checkout branchname
git checkout -b branchname
git merge featurebranchname

git clone “url from where we want to make clone.”

**random operations reference commands for reference**
git config --global user.name
git config --global user.name
git config --global user.password
git config --global user.email
git --version
git config --global user.name
git init
git status
git add Hello.java
git status
git commit -m 'this is my first commit.'
git status
git status
git add -A
git status
git commit -m "my second commit "
git status
git log
git log -p -1
git status
git init
git status
git add .
git commit -m "first commit"
git status
git staus
git log
git checkout -f
git add .
git commit -m "second commit"
git checkout -f
git diff
git add .
git diff
git diff -staged
git diff -stage
git diff --staged
git diff --staged
git --version
git init
git config --global user.name
git config --global user.name heeren
git config --global user.name
git config --global user.name codewithheeren
git config --global user.name
git config --global user.email
git status
git status
git add hello.java
git status
git commit -m "this is my first commit."
git status
git status
git add .
git status
git commit -m "my changes done with second commit"
git status
git log
git log -p -1
git status
git checkout -f
git diff
git init
git status
git add .
git commit -m "first commit"
got branch
git branch
git checkout -b feature1
git branch
git status
git checkout -f
git add .
git diff -staged
git diff --staged
git branch
git branch branch1
git branch
git branch branch2
git branch
git checkout branch1
git branch
git checkout branch2
git branch
git checkout -b branch3
git branch
git branch -r branch1
git branch -rm branch1
git branch -d branch1
git branch
git status
git add .
git commit -m "first commit on feature branch"
git status
git log
git checkout master
git checkout featrue1
git checkout feature1
git checkout master
git merge feature1
git clone https://github.com/codewithheeren/Java.git
history
```
---
