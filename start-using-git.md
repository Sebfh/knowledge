# Howto: Start using Git

This document describes the first basics commands that I used when I first started using Git.

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