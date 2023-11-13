# Courses
1. [Google IT Automation with Python (Course 3)](https://www.coursera.org/learn/introduction-git-github/)

> Bonus Tip: Since you can't `return` when not within a function, you can `import sys` then call `sys.exit (<whatever-you-want-to-return>)`
## Version Control
In simple terms, version control is like a time machine for your code. It's a system that helps you keep track of changes to your files over time, allowing you to see what you did, when you did it, and why you did it. This is particularly useful when working on software development projects or any collaborative work involving digital files.

**Git** is a popular and widely used tool for version control. Here's a simple explanation of Git:

1. **Snapshots of Your Work**: Git takes snapshots of your files at different points in time. Each snapshot represents the state of your project at a specific moment.

2. **Committing Changes**: You can make changes to your files and then "commit" those changes. Each commit is like a bookmark in your project's history, and you can add a message to describe what you changed.

3. **Branching**: Git allows you to create different "branches" of your project. Think of these as separate paths for development. You can work on a new feature or bug fix in one branch without affecting the main project until you're ready.

4. **Merging**: Once you're satisfied with your changes in a branch, you can "merge" it back into the main project or another branch. Git helps you resolve conflicts if two people made different changes to the same part of a file.

5. **Collaboration**: Git makes it easy for multiple people to work on the same project simultaneously. You can share your changes with others and incorporate their changes into your work.

6. **Remote Repositories**: Git also allows you to store your project on a remote server, like GitHub or GitLab, making it accessible from anywhere and enabling collaboration with people all over the world.

In summary, Git is a tool that helps you manage and keep track of changes to your files, collaborate with others, and maintain a history of your project's development. It's like having a detailed journal of your project's journey, making it easier to work on complex projects and ensuring that you can always go back in time if something goes wrong.

### Diff & Patch Commands
In the context of version control and Git, the Linux commands `diff` and `patch` are tools used to compare and apply differences between two sets of code or files.

1. **`diff` Command**:

   - **Purpose**: The `diff` command is used to compare two files or directories and identify the differences between them. It generates a "diff" or "patch" file that describes the changes needed to transform one file into another.
   
   - **Usage**: You provide two files or directories as arguments to `diff`, and it produces a list of differences, typically in a unified or context format.

   - **Example**: Suppose you have two versions of a text file, `file_old.txt` and `file_new.txt`, and you want to see the differences between them.

     ```bash
     diff file_old.txt file_new.txt > changes.diff
     ```

   - **Output**: The `changes.diff` file will contain a list of changes, showing lines that were added, removed, or modified between the two files.

> Tip: `diff -u` will show the individual lines that have been altered, similar to how it looks on GitHub.

2. **`patch` Command**:

   - **Purpose**: The `patch` command is used to apply the changes specified in a "diff" or "patch" file to an original file, effectively updating it to match the changes described in the patch file.
   
   - **Usage**: You provide the original file and the patch file as arguments to `patch`, and it makes the necessary changes to the original file.

   - **Example**: Assuming you have the `changes.diff` file from the previous example, you can apply those changes to `file_old.txt` to update it to the new version:

     ```bash
     patch file_old.txt < changes.diff
     ```

   - **Output**: After running this command, `file_old.txt` will be modified to match the changes specified in the `changes.diff` file.

In simple terms, think of `diff` as a tool to generate a "recipe" of changes between two files, and `patch` as a tool to follow that recipe and update one file to match the other. These commands are handy when you want to track and apply changes between different versions of your code or documents, which is a common use case in version control systems like Git.

### Git Config
The `git config -l` command is used to list the Git configuration settings for your Git repository. These settings can include your name, email, preferred text editor, and various other configuration options. It displays these settings in a simple list format.

Here's an example of how to use `git config -l` with a simple code example:

Suppose you have a Git repository and you want to check the configuration settings for that repository. You can use the following commands in your terminal:

```bash
# Navigate to your Git repository
cd /path/to/your/git/repo

# List Git configuration settings
git config -l
```

The `git config -l` command will display a list of configuration settings, which might look something like this:

```
user.name=Your Name
user.email=your@email.com
core.editor=your-favorite-editor
color.ui=auto
```

In this example:

- `user.name` is your Git username.
- `user.email` is your Git email address.
- `core.editor` is your preferred text editor for Git commit messages.
- `color.ui` is a setting for Git's command line interface to automatically enable color-coding for various outputs.

You can use `git config -l` to review or verify the configuration settings for your Git repository. These settings can be useful for customizing your Git workflow and ensuring that your commits are associated with the correct user information.

### Git Cheat Sheet

| -Command- |Explanation & Link|
|---|---|
|git commit -a|[Stages files automatically](https://git-scm.com/docs/git-commit#Documentation/git-commit.txt---all)|
|git log -p|[Produces patch text](https://git-scm.com/docs/git-log#_generating_patch_text_with_p)|
|git show|[Shows various objects](https://git-scm.com/docs/git-show)|
|git diff|[Is similar to the Linux `diff` command, and can show the differences in various commits](https://git-scm.com/docs/git-diff)|
|git diff --staged|[An alias to --cached, this will show all staged files compared to the named commit](https://git-scm.com/docs/git-diff)|
|git add -p|[Allows a user to interactively review patches to add to the current commit](https://git-scm.com/docs/git-add)|
|git mv|[Similar to the Linux `mv` command, this moves a file](https://git-scm.com/docs/git-mv)|
|git rm|[Similar to the Linux `rm` command, this deletes, or removes a file](https://git-scm.com/docs/git-rm)|
|git checkout| [Is effectively used to switch branches](https://git-scm.com/docs/git-checkout)|
|git reset| [Basically resets the repo, throwing away some changes. It’s somewhat difficult to understand, so reading the examples in the documentation may be a bit more useful.](https://git-scm.com/docs/git-reset#_examples) There are some other useful articles online, which discuss more aggressive approaches to [resetting the repo](https://jwiegley.github.io/git-from-the-bottom-up/3-Reset/4-doing-a-hard-reset.html).|
|git commit --amend| [Is used to make changes to commits after-the-fact, which can be useful for making notes about a given commit.](https://git-scm.com/docs/git-commit#Documentation/git-commit.txt---amend)|
|git revert| [Makes a new commit which effectively rolls back a previous commit. It’s a bit like an undo command.](https://git-scm.com/docs/git-revert) There are a [few ways](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things) you can rollback commits in Git.|
|git branch|[Used to manage branches](https://git-scm.com/docs/git-branch "https://git-scm.com/docs/git-branch")|
|git branch `<name>`|[Creates the branch](https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging "https://git-scm.com/book/en/v2/Git-Branching-Basic-Branching-and-Merging")|
|git branch -d `<name>`|[Deletes the branch](https://git-scm.com/docs/git-branch#Documentation/git-branch.txt--D "https://git-scm.com/docs/git-branch#Documentation/git-branch.txt--D")|
|git branch -D `<name>`|[Forcibly deletes the branch](https://git-scm.com/docs/git-branch#Documentation/git-branch.txt--D)|
|git checkout `<branch>`|[Switches to a branch.](https://git-scm.com/docs/git-checkout "https://git-scm.com/docs/git-checkout")|
|git checkout -b `<branch>`|Creates a new branch and [switches to it](https://git-scm.com/docs/git-checkout#Documentation/git-checkout.txt--bltnewbranchgt).|
|git merge `<branch>`|[Merge joins branches together](https://git-scm.com/docs/git-merge "https://git-scm.com/docs/git-merge").|
|git merge --abort|If there are merge conflicts (meaning files are incompatible), --abort can be used to abort the merge action.|
|git log --graph --oneline|[This shows a summarized view of the commit history for a repo](https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History "https://git-scm.com/book/en/v2/Git-Basics-Viewing-the-Commit-History").|

>.gitignore files are used to tell the git tool to intentionally ignore some files in a given Git repository. For example, this can be useful for configuration files or metadata files that a user may not want to check into the master branch. Check out more at: [https://git-scm.com/docs/gitignore](https://git-scm.com/docs/gitignore)
>
>A few common examples of file patterns to exclude can be found [here](https://gist.github.com/octocat/9257657).

