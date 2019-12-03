# GitHub Tutorial

_by David Zeng_

---
## Git vs. GitHub
#### **Git:**
a version control system based on the command line that allows the user to quickly and efficiently make and track changes to a project they are working on both online and offline. In addition, Git does not require the use of Github.
#### **Github:**
a cloud based system that focuses on the collaboration side of projects between people online while containing the version control aspect of Git. This means using Github requires the use of Git.

---
## Initial Setup



---
## Repository Setup
* To create a repository, first choose the directory that you would like to make the repository in and us the command `git init`.
* After initializing a repository, you will want to create the files that you will be using in that specific repository using `touch (filename)`.
* To make changes to a file you will need to open it using the command `c9 (filename)`.
* Once the changes have been made, make sure that they have been saved within that file (no red dot on the tab of the file) and then you can proceed to add it to the stage.
* To add a file to the stage use the command `git add .`.
* Then you can commit the file by using `git commit -m "commit message"`.
* On github.com, create a new repository and make its name the same as the one in your ide.
* After you have done that, make sure the link under quick setup is the SSH key.
* Then, copy the 2 links under "push to an existing repository" and paste them individually to your ide.
* Once you are done with that use can use `git push` to send your current and future commits to that local repository that you just created.  

_(Make sure to use `git status` before you add, after you add, and after you commit)_

---
## Workflow & Commands
The workflow order of Git is pretty simple:
* make changes
* `git status`
* `git add .`
* `git commit -m "message"`
* `git push`
* repeat

Even though `git status` is shown once, it is recommended that it be used after each of the commands displayed to track the files that have been changed

`git status` is basically used to see if a file is being tracked/observed or not. It will show the user what state the file is in and can display whether or not changes were made to that specific file.

`git add .` puts the directory on to the stage, which includes the files that have changes within them to get ready for a commit.

`git commit -m "message"` saves a copy of the files on the stage, including the changes (The message should be in the present-tense and describe the changes made).

---
## Rolling Back Changes
Rolling back changes is the equivalent of undoing your mistakes. This includes undoing commits, edits and removing a file from the stage.
* To undo an **edit** that you made to a file, use `git checkout -- <file>`. You can also get a hint for this command by using `git status` and looking at the top section. However, make sure not to include `...` and `<>`when typing in the command (applies to most of commands listed).
* If you want to **unstage** a file (undo add), use `git reset HEAD <file>` and it will remove that specific file from the staging area.
 
There are different commands to undo a commit, depending on which situation you have (using `git status` won't give you hints to undo commits):  
* To undo **only** the commit but leave the edits and the file on the staging area, use `git reset --soft HEAD~1`. This will get rid of your previous commit while leaving the file on the staging area with its changes.
* To undo a commit **and** add, use `git reset HEAD~1`. This goes back to a previous commit but leaves your changes that you've made in the current commit while unstaging the file as well.
* To **completely destroy** a commit, use `git reset --hard HEAD~1`. This will completely erase the current commit and leave no trace of it behind (This is a very dangerous command, so make sure you actually want to destroy the commit before using it).

One more command that is useful to revert changes is `git revert SHA`. This command is used to revert changes that a commit has previously made. Use `git log` to look at your past history of commits. The SHA code is the yellow text that appears right next to the word "commit" and you only need to put the first 7 letter/digits. By doing this, the changes that a certain commit has made will be deleted while the changes from other commits remain the same.