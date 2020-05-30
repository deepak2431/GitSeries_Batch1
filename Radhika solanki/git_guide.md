# Github Basics

##  Git and Github

 **Git** is created by _Linus Torvald_.git is a distributed version control system. It is designed to track changes to file. It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed, data integrity, and support for distributed, non-linear workflows.


 **Github** is a software used for version control. it is useful when more than one person is working on a project.GitHub is built for collaboration. Set up an organization to improve the way your team works together, and get access to more features.

 **Github is so popular because :**
* it makes easy to contribute to your open source projects
* Can be accessed anytime anywhere
* provides secure cloud storage
* documentation.showcase your work
* markdown

**Other platforms similar to Github :**
* Gitlab
* Bitbucket
* Phabricator
* Beanstalk
* Sourceforge

**What is Git Bash?**

Git Bash is an application that adds an emulation layer on Microsoft Windows environments to use Git command-line experience. It is just like a package that installs some common bash utilities on a Windows operating system. It let us use all the Git features as well as most of the standard UNIX commands in a command-line interface on Windows.

## Working of Git
git workflow consist of 4  fundamental elements.
	
* Workspace
* Index(Stage)
* Local Repository
* Remote Repository
    
The file in the workspace can be in 3 states. It can be committed which means the changes in the file are safely saved to the local repository. It could be modified and it could be staged means the file is the part of the index.

**Some Basic Commands**

* clone: creates local copy of repository in the workspace.
* add(-u):add file from workspace to the index.
* commit:All the files which are staged that are listed to the local repository .
* commit -a:add files from workspace to local repository.
* push:it pushes files from local repository to remote repository.
* fetch : get the file from remote repository to local repository.
* merge: gets file from local repository to workspace.
* pull: It takes the file directly from remote repository to workspace.
* diff:diff command is used in git to track the difference between the changes made on a file.

## Branching
Branches allow you to move back and forth between 'states' of a project. For instance, if you want to add a new page to your website you can create a new branch just for that page without affecting the main part of the project. Once you're done with the page, you can merge your changes from your branch into the master branch. When you create a new branch, Git keeps track of which commit your branch 'branched' off of, so it knows the history behind all the files.

command for **creating** a new branch is: git checkout -b branchname

command for **deleting** a branch is: git branch -d branchname

## Forking

**fork** is a copy of original repository. By using fork we can get exact copy of original repository and we can update the files without disturbing original repository.Git Fork means you just create a copy of the main repository of a project source code to your own GitHub profile.Then make your changes and create a Pull Request to the main repository branch. If the Main Repository owners like your changes they will merge it to the main repository.

**steps to fork a Repo**
- Go to the Repo which you want to fork.
- click on fork button.

## Cloning

After forking you need to clone the forked repo to do changes inside that Repo.The git clone is a git command, which creates a clone/copy of an existing repository into a new directory.

**Steps for cloning:**
  
- click clone and download button 

- After clicking copy the link which it shows there.
  
- Then open Git Bash.
   
- Change the directory.

- After Changing the directory type command git clone followed by link which you copied after clicking on clone and download button.

**Pull Request**

A pull request (PR) is a method of submitting contributions to an open development project. It occurs when a developer asks for changes committed to an external repository to be considered for inclusion in a project's main repository after the peer review.

**Issues in Github**

You can collect user feedback, report software bugs, and organize tasks you'd like to accomplish with issues in a repository.

**steps to create issues:**
- go to the repository page in which you want to create issue.
- click on issues.
- click on create new issue.
- Type issue in comment box you can add labels like bug,enhancement,etc.
- submit the issue.


## Merge Conflict

In every situation where work can be parallelized, work will eventually overlap. Sometimes two developers will change the same line of code in two different ways  in such a case git conflict occurs.Git can handle most merges on its own with automatic merging features. A conflict arises when two separate branches have made edits to the same line in a file, or when a file has been deleted in one branch but edited in the other. Conflicts will most likely happen when working in a team environment.


Regards

Chetana Tijare

