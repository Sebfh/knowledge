# Howto: Start using Git

This document describes the first basics commands that I used when I first started using Git. If you have the time, please read [this great online book](http://git-scm.com/book). 

	$ git init
	# Initializes an empty repository in the current folder

	$ git add .
	# Stages all files in the folder, adding it to the list of files to be committed

	$ git remote add git@github.com:Sebfh/knowledge.git
	# Creates a remote named "origin" pointing at the GitHub repo

	$ git commit -a -m "This is my first commit"
	# Commits your files, adding the message "This is my first commit"

	$ git push -u origin master
	# Sends your commits in the "master" branch to GitHub, the -u tells this local branch to track the remote branch

## Configure Git

	$ git config --global user.name "Your Name"
	# Sets the default name for git to use when you commit

	$ git config --global user.email your@email.com
	# Sets the default email for git to use when you commit

## Cloning an Existing Repository

If you want to get a copy of an existing Git repository — for example, a project you’d like to contribute to — the command you need is **git clone**.

You clone a repository with **git clone [url]**. For example, if you want to clone this repository, you can do so like this:

	$ git clone git://github.com/Sebfh/knowledge.git

That creates a directory named __knowledge__, initializes a .git directory inside it, pulls down all the data for that repository, and checks out a working copy of the latest version.

## Commit the changes you just made

If you don't had time to read all off [the Git Book](http://git-scm.com/book "Please do!") then just follow these instructions to commit you latest changes to the repo on Github.

	$ git add FILENAME
	# You can use . to stage all files in the folder
	
	$ git commit -m "Your commit message goes here"
	# Please be descriptive in your commit-messages, your not the only one working on the project...

	$ git push origin master
	# Push the branch you're on to Github, this is normally *master* but could be a different one.

## Reading

Please reed [http://git-scm.com/book](http://git-scm.com/book "It's easy, trust me...")