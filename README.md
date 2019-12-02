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
* After you have done that, Make sure the link under quick setup is the SSH key.
* Then, copy the 2 links under "push to an existing repository" and paste them individually to your ide.
* Once you are done with that use can use `git push` to send your current and future commits to that local repository that you just created.  

_(Make sure to use `git status` before you add, after you add, and after you commit)_

---
## Workflow & Commands



---
## Rolling Back Changes