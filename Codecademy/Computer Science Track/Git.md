## Basic Git Workflow
- A Git project will normally consist of a basic three parts
	- A Working Directory: This is where you are doing all the work
		- `C:\Users\user\Git Projects\Project1`
	- A Staging Area: This is where you'll list changes you make to the working directory
	- A Repository: This is where Git permanently stores those changes as different versions of the project
- Workflow:
	- `git init` -> Working Directory -> `git add` -> Staging Area -> `git commit` -> Repository

## Common Git Commands
- `git status` - Check the status of changes made to the Working Directory
- `git add <filename>` - Tells git to start tracking the specified file and adds it to the staging area to be committed later.
- `git diff <filename>` - Check the difference between the active file in the Working Directory and what was already added to the Staging Area
- `git commit -m "Commit Comment Here"` - A commit permanently stores changes from the staging area inside the local repository.
	- If the `-m` option is not specified, git will open a local document where you will type in your comment.
- `git log` - Commits are stored chronologically in the repository and can be viewed with this command.
	- The output of this command is:
		- A 40-character code (SHA) that uniquely identifies the commit. (Appears in orange text)
		- The commit author
		- The date and time of the commit
		- The commit message
- `git config --global user.email` - View email associated with current repository/branch.
	- This is the email being used for all commits
	- This needs to be changed if using a private GitHub email
- `git config --global user.email {ID}+{username}@users.noreply.github.com` - Allows you to change the email associated with the current repository/branch
	- Find the email used with your account in GitHub account settings -> Under 'Access' -> Emails
	- If you had already ran `git commit` before this change then use `git commit --amend --reset-author` to update your commit before pushing.
- `git checkout <branch-name>` - Moves your tree to the position of which branch you want to work in.

[GitHub/Git CLI Cheatsheet](/Cheatsheets/git-cheat-sheet-education.pdf)