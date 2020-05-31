# step by step guide 

Git isn't the same thing as GitHub. Git is a version-control system (i.e., a piece of software) that helps you keep track of your computer programs and files and the changes that are made to them over time. It also allows you to collaborate with your peers on a program, code, or file. GitHub and similar services (including GitLab and BitBucket)are websites that host a Git server program to hold your code.

how to create a repo

## Step 1: 

Create a GitHub account

The easiest way to get started is to create an account on GitHub.com (it's free). Pick a username (e.g., subho1234), enter your email address and a password, and click Sign up for GitHub.

## Step 2: 

 Create a new repository

A repository is like a place or a container where something is stored; in this case we're creating a Git repository to store code. To create a new repository, select New Repository from the + sign dropdown menu. Enter a name for your repository (e.g, "Demo") and click Create Repository. Don't worry about changing any other options on this page.

Congratulations! You have set up your first repo on GitHub.com.

## Step 3: 

 Create a file

Once your repo is created, you may feel puzzled. But don't panic, it's simpler than it looks. Stay with me. Look at the section that starts "...or create a new repository on the command line," and ignore the rest for now.

Open the Terminal program on your computer. Type git and hit Enter. If it says command bash: git: command not found, then install Git with the command for your Linux operating system or distribution. Check the installation by typing git and hitting Enter; if it's installed, you should see a bunch of information about how you can use the command.

In the terminal, type:

mkdir Demo

This command will create a directory (or folder) named Demo.

Change your terminal to the Demo directory with the command:

cd Demo

Then enter:

echo "#Demo" >> README.md

This creates a file named README.md and writes #Demo in it. To check that the file was created successfully, enter:

cat README.md

This will show you what is inside the README.md file, if the file was created correctly.

To tell your computer that Demo is a directory managed by the Git program, enter:

git init

Then, to tell the Git program you care about this file and want to track any changes from this point forward, enter:

git add README.md

## Step 4: 

 Make a commit

So far you've created a file and told Git about it, and now it's time to create a commit. Commit can be thought of as a milestone. Every time you accomplish some work, you can write a Git commit to store that version of your file, so you can go back later and see what it looked like at that point in time. Whenever you make a change to your file, you create a new version of that file, different from the previous one.

To make a commit, enter:

git commit -m "first commit"

That's it! You just created a Git commit and included a message that says first commit. You must always write a message in commit; it not only helps you identify a commit, but it also enables you to understand what you did with the file at that point. So tomorrow, if you add a new piece of code in your file, you can write a commit message that says, Added new code, and when you come back in a month to look at your commit history or Git log (the list of commits), you will know what you changed in the files.

## Step 5: 

Connect your GitHub repo with your computer

Now, it's time to connect your computer to GitHub with the command:

git remote add origin https://github.com/<your_username>/Demo.git

Let's focus this command step by step. We are telling Git to add a remote called origin with the address https://github.com/<your_username>/Demo.git (i.e., the URL of your Git repo on GitHub.com). This allows you to interact with your Git repository on GitHub.com by typing origin instead of the full URL and Git will know where to send your code. Why origin? Well, you can name it anything else if you'd like.

Now we have connected our local copy of the Demo repository to its remote counterpart on GitHub.com.

Now that we have added the remote, we can push our code (i.e., upload our README.md file) to GitHub.com.

And if you go to https://github.com/<your_username>/Demo and if you go to https://github.com/<your_username>/Demo will get to know about the above things. That's it! You have created your first GitHub repo, connected it to your computer, and pushed (or uploaded) a file from your computer to your repository called Demo on GitHub.com.

Now i will just let you know about some important topics on Git

Git workflow : Workflow has 4 fundamentals - A. Workspace B. Index C. local repository D. remote repository

A. Workspace: The Working Directory B. Index : A staging area between workspace and the repository C. Local Repository : Here we make the local changes D. Remote Repository : It is on the Server.

Different stages of a git project as commit,add :

A. Modified : The changes can be made in the code without further changing the actual code. B. Staged: staging area or index, the place where all the new files are finally ready to be joined to the remote repository. C. Committed : It means the current changes in the data is modified and safely stored in local repository.

Git diff :

git diff command is used to check or track the difference between the files , where they differ i.e., in the stage and the workspace.

# FORK :- 

A fork is a copy of a repository. Forking a repository allows you to freely experiment with changes without affecting the original project. Most commonly, forks are used to either propose changes to someone else's project or to use someone else's project as a starting point for your own idea.

##CLONE :- 

 Clone is same as what the word has in the literary terms, making a copy of the files present in the cloud on github server to your local machine. Cloning basically means you want to get a local copy of the code present in the repository. After cloning you can then do whatever changes you like in the code and then you can pull the changes back to the repository.

** fork is in essence a clone too but it doesn't keep up with the original repo. So you will not be able to track the changes made to the original repo when you do a 'git fetch', 'git status' and finally 'git merge' (or 'git pull') .

Branches in github :

Git branch is a feature in git used for separating a feature or part of code from you your master in order not to mess something in your main code like suppose you have a website as a project in git and you want to add a new feature to it so you do it by creating a new branch for it so your main code remain the same as it and once you complete it then you merge it with your master.

## PR : 

PR stands for pull request. A pull/merge request is submitted when you’ve worked on some code from a particular branch and want to inform the others of the changes you’ve made. A person/people can be assigned to review and subsequently approve the request before your changes can be incorporated into the branch. Do note that it is referred to as a “pull-request” on GitHub and Bitbucket, but other platforms like GitLab and Gitorious have opted to call it a “merge-request”.

# DELETING A BRANCH 

## Delete a remote branch 

a. git push origin --delete ( Git version 1.7.0 or newer )

b. git push origin :

(Git versions older than 1.7.0)

## Delete a local branch  


a. git branch --delete

b. git branch -d

( Shorter version)

C. git branch -D

(Force delete un-merged branches)

{☆Also in github, we can have head branches automatically deleted after pull requests are merged in your repo.}

## Merge conflicts : 

when we change the same file from different branches and tries to merge them ,they didnot get merged automatically and hence a conflict occurs . That conflict during merging those branches is known as merge conflicts. Basically , a merge conflict is an event that occurs when Git unables to resolve differences automatically between the commits made by the user.

Always remember we can have different multiple branches other than the master branch .

## git branch -d :  This is a command used to delete a branch.The branch must be fully merged in its upstream branch or in HEAD ( i.e., when it would be pushed and merged already with the remote branch.)

## git branch -D : 

This is a command use to delete a branch irrespective of its merged status(i.e., when we want to delete the branch forcefully even if it hasn't been merged or pushed till that moment )

Thats all about my knowledege and experience on Git and Github.
