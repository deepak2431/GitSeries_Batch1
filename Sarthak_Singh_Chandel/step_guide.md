------------------------------------------------------------------------------------------------------------------------------------------------

# Introduction to Git and Github

### Git
Git is a free and open source distributed version control(Version control is a system that records changes to a file or set of files over time so that you can recall specific versions later. For example:If you are a graphic or web designer and want to keep every version of an image or layout which you would most certainly want to, a Version Control System (VCS) is a very wise thing to use) system designed to handle everything from small to very large projects with speed and efficiency.
Git is easy to learn and has a tiny footprint with lightning fast performance. It was created by Linus Torvalds in 2005 for development of the Linux kernel, with other kernel developers contributing to its initial development.
It is designed for coordinating work among programmers, but it can be used to track changes in any set of files. Its goals include speed, data integrity, and support for distributed, non-linear workflows. Git supports rapid branching and merging, and includes specific tools for visualizing and navigating a non-linear development history

### Git Identity
  The first thing you should do when you install Git is to set your user name and email address. This is important because every Git commit uses this information, and it’s immutably baked into the commits you start creating:
$ git config --global user.name
$ git config --global user.email

### How github works:
GitHub is a file or code sharing service to collaborate with different people. 
GitHub is a highly used software which is used for version control. It is helpful when more than just one person is working on a project.Github helps various users to build a centralized repository where everyone can upload, edit and manage the code files. 
GitHub is a central repository and Git is a tool which allows you to create a local repository.Git is a version control tool that will allow you to perform all kinds of operations to fetch data from the central server or push data to it whereas GitHub is a core hosting platform for version control collaboration. GitHub allows you to host a central repository in a remote server.

Other platforms similar to Github :

Gitlab
Bitbucket
Phabricator
Beanstalk
Sourceforge

**Git Bash**
Git Bash is an application that adds an emulation layer on Microsoft Windows environments to use Git command-line experience. It is just like a package that installs some common bash utilities on a Windows operating system. It let us use all the Git features as well as most of the standard UNIX commands in a command-line interface on Windows.

***GitHub  Workflow:***

**1. Workspace:**
The Workspace is the area where we are currently working. It is where our files are stored. If we make changes to files in your workspace git will recognize that they are modified.To know what is stored in our file: Run the command git status. This command will show you two things: The files in your Workspace and the files in your Staging Area. 

**2. The Staging Area (Index):**
The Staging Area is when git starts tracking and saving changes that occur in files. These saved changes reflect in the .git directory. If you want to track specific files, then git moves from Workspace to the Staging Area. If you make any more additional changes after adding a file to the Staging Area, git will not know about those specific changes until you tell it to see them. We explicitly have to tell git to notice the edits in our files. To know which files are in staging area click git status.

To add files to the Staging Area: Run the command (git add filename) will add a specific file to the Staging Area from your Workspace. If we want to add everything from the Workspace, then run the command (git add . ). The . operator is a wildcard meaning all the files from the workspace are staged in the stagin area.

**3. The Local Repository:**
The Local Repository is everything in our .git directory. Mainly what we will see in your Local Repository are all of our checkpoints or commits. It is the area that saves everything.

To add items from our Staging Area to our Local Repository: The git command git commit takes all changes in the Staging Area, wraps them together and puts them in our Local Repository. A commit is simply a checkpoint telling git to track all changes that have occurred up to this point using our last commit as a comparison. After committing, your Staging Area will be empty.

**4. Remote Repository:**
As we make changes to our project locally on our system, we can keep them up-to-date with our remote repository. In Git, a remote is the server where our code is stored. In our case, that server is a repository on GitHub.


### Cloning:
When we create a repository on our GitHub Server, it exists as a remote repository. Anyone can clone our repository (if it has public access) to create a local copy on their computer and sync between the two locations.
On GitHub, navigate to the main page of the repository. Under the repository name, click Clone. In the Clone with HTTPs section, click  to copy the clone URL for the repository. Clone URL button. Open Git Bash terminal. Change the current working directory to the location where you want the cloned directory to be made.Type git clone, and then paste the URL you copied. After it, Press Enter. Your local clone will be created on your system.

### Forking:
A fork is a copy of a repository. Forking a repository allows us to freely experiment with changes without affecting the original project. Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for our own idea.
A great way of using forks to propose changes is for bug fixes. Rather than logging an issue for a bug you've found, you can:
Fork the repository. Make the fix. And then submit a pull request to the project owner.If the project owner likes your work, they might pull your fix into the original repository!

### Git Branching:
A branch is a lightweight movable pointer to one of these commits. The default branch name in Git is master . As you start making commits, you're given a master branch that points to the last commit you made. Every time you commit, the master branch pointer moves forward automatically.
Creating a new Branch:
The $ git branch command lets you create, list, rename branches.

* Switching Branches: *
To switch to an existing branch, you run the git checkout command.

* To delete branch: *
Use Command $ git branch -d. The -d option will delete the branch only if it has already been pushed and merged with the remote branch. Use -D instead if you want to force the branch to be deleted, even if it hasn't been pushed or merged yet.

* Basic Merging- *
It is a process of merging a new branch into master branch.

* Creating Merge Conflict- *
This code example executes a sequence of commands that accomplish the following.
•Create a new directory named git-merge-test, change to that directory, and initialize it as a new Git repo.
•Create a new text file merge.txt with some content in it.
•Add merge.txt to the repo and commit it. Now, we have a new repo with one branch master and a file merge.txt with content in it.
•Next, we will create a new branch to use as the conflicting merge.
•Create and check out a new branch named new_branch_to_merge_later
•Overwrite the content in merge.txt
•Commit the new content
•git merge new_branch_to_merge_later

** When a conflict appears.

* To resolve Conflict- *
•The most direct way to resolve a merge conflict is to edit the conflicted file.
•Open the merge.txt file in your favorite editor. For our example lets simply remove all the conflict dividers. Once the file has been edited use git add merge.txt to stage the new merged content.
To finalize the merge create a new commit Git will see that the conflict has been resolved and creates a new merge commit to finalize the merge.

### Making Pull Requests:
Pull requests tell us others about changes we've pushed to a branch in a repository on GitHub. Once a pull request is opened, we can discuss and review the potential changes with collaborators and add follow-up commits before our changes are merged into the base branch.
After initializing a pull request, we'll see a review page that shows a high-level overview of the changes between our branch (the compare branch) and the repository's base branch. We can add a summary of the proposed changes, review the changes made by commits and add labels.
Once we've created a pull request, we can push commits from our branch to add them to our existing pull request. These commits will appear in chronological order within our pull request. Other contributors can review our proposed changes, add review comments, contribute to the pull request discussion, and even add commits to the pull request. After we're done with the proposed changes, we can merge the pull request. If we're working in a shared repository model, we create a pull request and someone else, will merge your changes from our branch into the base branch you specify in your pull request.We can link a pull request to an issue to show that a fix is in progress and to automatically close the issue when someone merges the pull request. 


# commands used to perform operations  :

## Checking your present directory
  - pwd

## Making new directory
  - mkdir directoryName

## Changing your directory
  - cd directoryName

## Cloning a repository
  - git clone URl (given at Clone & Download option in github)

## To check status i.e. working tree
  - git status

## Making a txt file
  - name.txt

## Making a readme file
  - file.md
  + **Note the ectensions to make such files**
  + **Important**
  Redme file should be in Markdown language.

  + **Inserting text in editor**
  press ESC + i
  
  + **Saving and quit out of file**
  press ESC + :
  then write `wq`

## Make change to project by add
  - git add

## Make changes through commit
  - git commit -m "any name"
  **Notice : You cannot commit before adding your work**

## push work done
  - git config --global user.email "mailid.com"
  - git config --global user.name "github User Name"
  - git log | head
  - git push

## Check your current branch
  - git branch

## Making & Entering in new branch
  - git checkout -b new-branch

## Changing the branch
  - git checkout branch-name

## delete a branch
  - git branch-name -d
  - git branch-name -D

## Merging new branch into master branch
  - git merge branch-name

# Raising an issue
+ Issues can be used to keep track of bugs, enhancements, or other requests.
+ Any GitHub user can create an issue in a public repository where issues have not been disabled.
  - 1. You can open a new issue based on code from an existing pull request.
  - 2. You can open a new issue directly from a comment in an issue or a pull request review.

# Flowchart to create an issue:
1. On GitHub, navigate to the main page of the repository.
2. Under your repository name, click Issues. 
3. Click New issue.
4. If there are multiple issue types, click Get started next to the type of issue you'd like to open.
5. Type a title and description for your issue.
6. If you're a project maintainer, you can assign the issue to someone, add it to a project board, associate it with a milestone, or apply a label.
7. When you're finished, click Submit new issue.

Hope this helps!
Happy Coding!!

------------------------------------------------------------------------------------------------------------------------------------------------


