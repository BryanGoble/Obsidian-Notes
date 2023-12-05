---
tags:
  - Python
  - Linux
  - Automation
  - UnitTesting
  - Git
  - Networks
  - Troubleshooting
---
Learn in-demand skills like Python, Git, and IT automation to advance your career
# Courses
1. [Google IT Automation with Python](https://www.coursera.org/professional-certificates/google-it-automation)
	1. [Crash Course on Python](https://www.coursera.org/learn/python-crash-course
	2. [Using Python to Interact with the Operating System](https://www.coursera.org/learn/python-operating-system)
	3. [Introduction to Git and Github](https://www.coursera.org/learn/introduction-git-github/)
	4. [Troubleshooting and Debugging Techniques](https://www.coursera.org/learn/troubleshooting-debugging-techniques/)
	5. [Configuration Management and the Cloud](https://www.coursera.org/learn/configuration-management-cloud/)
	6. [Automating Real-World Tasks with Python](https://www.coursera.org/learn/automating-real-world-tasks-python?specialization=google-it-automation)
## Introduction to Programming

- **Programming code** - Programming code is a set of written computer instructions, guided by rules, using a computer programming language. It might help to think of the computer instructions as a detailed, step-by-step recipe for performing tasks. The instructions tell computers and machines how to perform an action. Programming code may also be referred to as source code or scripts.

- **Programming languages** - Programming languages are similar to human spoken languages in that they both use syntax and semantics. Programming languages are used to write computer programs.  Some common programming languages include Python, Java, C, C++, C#, and R.

- **Syntax** - Syntax is a set of rules for how statements are constructed in both human and computer languages. Programming syntax includes rules for the order of elements in programming instructions, as well as the use of special characters and their placements in statements. This concept is similar to the syntax rules for grammar and punctuation in human language.

- **Semantics** - Semantics refers to the intended meaning or effect of statements, or collections of words, in both human and computer languages. Semantic errors are also referred to as logical errors.

- **Computer program** - A computer program is a step-by-step list of instructions that a computer follows to reach an intended goal. It is important to be clear and precise about the actions a computer program is supposed to perform because computers will do exactly what they are instructed to do. Computer programs can be long, complex, and accomplish a variety of tasks. They are often developed by computer programmers and software engineers, but anyone can learn to create them. Computer programs may involve a structured development cycle. They can be written in a wide variety of programming languages, such as Python, Java, C++,  R, and more. The completed format of a program is often a single executable file.

- **Script** - Scripts are usually shorter and less complex than computer programs. Scripts are often used to automate specific tasks. However, they can be used for complex tasks if needed. Scripts are often written by IT professionals, but anyone can learn to write scripts. Scripts have a shorter, less structured development cycle as compared to the development of complex computer programs and software. Scripts can be written in a variety of programming languages, like Python, JavaScript, Ruby, Bash, and more. Some scripting languages are interpreted languages and are only compatible with certain platforms.

- **Automation** - Automation is used to replace a repetitive manual step with one that happens automatically. 

- **Output** - Output is the end result of a task performed by a function or computer program. Output can include a single value, a report, entries into a database, and more. 

- **Input** - Input is information that is provided to a program by the end user. Input can be text, voice, images, biometrics, and more.   

- **Functions** - A function is a reusable block of code that performs a specific task.

- **Variables** - Variables are used to temporarily store changeable values in programming code.

- **Platform-specific / OS specific scripting language** - Platform-specific scripting languages, like PowerShell (for Windows) and Bash (for Linux), are used by system administrators on those platforms. 

- **Client-side scripting language** - Client-side scripting languages, like JavaScript, are used mostly for web programming. The scripts are transferred from a web server to the end-user’s internet browser, then executed in the browser.

- **Machine language** - Machine language is the lowest-level computer language. It communicates directly with computing machines in binary code (ones and zeros). In binary code, one equals a pulse of electricity and zero equals no electrical pulse. Machine language instructions are made from translating languages like Python into complex patterns of ones and zeros. 

- **Cross-platform** **language** - Programming language that is compatible with one or more platforms / operating systems (e.g., Windows, Linux, Mac, iOS, Android).

- **Object-oriented programming language** - In object-oriented programming languages, most coding elements are considered to be objects with configurable properties. For example, a form field is an object that can be configured to accept only dates as input in the mm/dd/yy format, and can be configured to read from and write to a specific database. 

- **Python interpreter -** An interpreter is the program that reads and executes Python code by translating Python code into computer instructions.

- **Built-in functions:** Functions that exist within Python and can be called directly

- **Comments:** Notes to yourself and/or other programmers to make the purpose of the code clear

- **Data types:** Classes of data (e.g., string, int, float, Boolean, etc.), which include the properties and behaviors of instances of the data type (variables)

- **Explicit conversion:** This occurs when code is written to manually convert one data type to another using a data type conversion function

- **Expression:** A combination of numbers, symbols, or other values that produce a result when evaluated

- **Implicit conversion:** This occurs when the Python interpreter automatically converts one data type to another

- **Logical operators:** Operators used to combine or manipulate Boolean values, `True` or `False`, to create complex conditions for decision-making. 

- **Parameter (argument):** A value passed into a function for use within the function, controlling the behavior of the CSV reader and writer

- **Refactoring:** When a code is updated to be more self-documenting and clarify the intent 

- **Return value**: This is the value or variable returned as the end result of a function
## Interpreted vs. Compiled Languages
**Interpreted Languages**:

1. **Execution**: Interpreted languages are executed line by line, directly by an interpreter software. The code is read and executed sequentially from top to bottom.
2. **Portability**: Code written in an interpreted language is generally more portable because it can run on any platform with the corresponding interpreter.
3. **Debugging**: Debugging is often easier in interpreted languages because errors can be caught and reported as soon as they occur in the code.
4. **Performance**: Interpreted languages tend to have slower execution speed compared to compiled languages because the code is translated and executed on the fly.

**Compiled Languages**:

1. **Compilation**: Compiled languages are first translated into machine code (or intermediate code) by a compiler before execution. This translation step creates a separate executable file.
2. **Execution**: The compiled program is executed directly by the computer's CPU, which can lead to faster execution times compared to interpreted languages.
3. **Portability**: Compiled programs are typically less portable because they are specific to the machine architecture and operating system for which they were compiled.
4. **Debugging**: Debugging in compiled languages can be more challenging since errors are detected during the compilation phase, which may require extra effort to identify and fix.

In summary, interpreted languages are easier to write, more portable, and offer better debugging capabilities but tend to be slower in terms of execution speed. Compiled languages produce faster-running programs but are less portable and can be more challenging to debug. The choice between them depends on the specific needs of a project and the trade-offs you are willing to make.
## Benefits of Automation
- Scalability - When more work is added to a system, the system can do whatever it needs to complete the work
- Centralizing Mistakes

`[time_to_automate < (time_to_perform * amount_of_times_performed*)]`

![https://xkcd.com/1205/](https://imgs.xkcd.com/comics/is_it_worth_the_time.png)
## Pareto Principle
One fifth of the sysadmin tasks you perform comprise four fifths of your total workload.
## I/O Streams
The basic mechanism for performing input and output operations in your programs. Called streams, because the data is always flowing.

- Standard Input (STDIN) - input()
- Standard Output (STDOUT) - print()
- Standard Error (STDERR) - Traceback
## Running System Commands in Python
In simple terms, the `subprocess` module in Python 3 is a built-in module that allows you to run external processes (other programs or commands) from within your Python script. It provides a way to interact with these external processes, capture their output, and control their execution.

Here are some key points to understand about the `subprocess` module:

1. **Running External Commands**: You can use `subprocess` to run external commands or programs, such as command-line utilities or system processes, directly from your Python script.
2. **Capture Output**: You can capture the output (stdout) and error messages (stderr) generated by the external process and use them in your Python code. This allows you to process or display the results.
3. **Communication**: You can interact with the external process by sending input to it and reading its output. This is useful for automating tasks or scripts that require interaction with external programs.
4. **Error Handling**: `subprocess` provides ways to handle errors that may occur during the execution of external processes, such as when a command fails to run.
5. **Control and Management**: You can control various aspects of the subprocess, including setting environment variables, specifying working directories, and more.

Here's a simple example of how you might use the `subprocess` module to run an external command and capture its output:

```python
import subprocess

# Run an external command (e.g., 'ls' to list files in a directory)
result = subprocess.run(['ls', '-l'], stdout=subprocess.PIPE, stderr=subprocess.PIPE, text=True)

# Print the output and error messages
print("Standard Output:")
print(result.stdout)

print("Standard Error:")
print(result.stderr)
```

In this example, the `subprocess.run()` function runs the 'ls' command to list files in a directory. It captures both the standard output and standard error, which can then be used or processed in your Python script.

Overall, the `subprocess` module is a powerful tool for integrating external processes into your Python applications and automating various system-related tasks.

```Python
import subprocess

subprocess.run(["date"])

# Tue 07 Jan 2023 02:34:44 PM PST
# CompletedProcess(args=['date'], returncode=0)
```
## Unit Tests
In simple terms, the `unittest` module in Python 3 is a built-in library that helps you write and run test cases for your Python code. It is part of the standard library and provides a framework for organizing and running tests to ensure that your code works as expected.

Here are some key points to understand about the `unittest` module:

1. **Test Cases**: You create test cases by defining classes that inherit from `unittest.TestCase`. Each test case class contains one or more test methods, which are regular Python methods that test specific parts of your code.

2. **Assertions**: Inside your test methods, you use various assertion methods provided by `unittest.TestCase` to check whether your code produces the expected results. Common assertions include `assertEqual`, `assertTrue`, `assertFalse`, and more.

3. **Test Discovery**: The `unittest` framework can automatically discover and run your test cases. It looks for methods that start with the word "test" within your test case classes.

4. **Test Suites**: You can group related test cases into test suites. Test suites help you organize and run multiple test cases together.

5. **Setup and Teardown**: You can use special methods `setUp` and `tearDown` to set up initial conditions before each test method and clean up after each test method, respectively.

6. **Test Runner**: Python includes a built-in test runner that you can use to execute your tests. You can run tests from the command line or integrate them into your development environment.

Here's a simple example of writing and running tests using the `unittest` module:

```python
import unittest

# Function to be tested
def add(a, b):
    return a + b

# Test case class
class TestAddition(unittest.TestCase):

    def test_add_positive_numbers(self):
        result = add(2, 3)
        self.assertEqual(result, 5)

    def test_add_negative_numbers(self):
        result = add(-2, -3)
        self.assertEqual(result, -5)

if __name__ == '__main__':
    unittest.main()
```

In this example:

- We define a simple function `add` that adds two numbers.
- We create a test case class `TestAddition` with two test methods, each testing a different scenario for the `add` function.
- We use the `self.assertEqual` assertion to check if the function produces the expected results.
- Finally, we run the tests using `unittest.main()`.

The `unittest` module helps you automate the testing process, ensuring that your code behaves correctly, and makes it easier to catch and fix issues as you develop your software.
## Basic Linux Commands
### Managing files and directories
- **cd** directory: changes the current working directory to the specified one
- **pwd:** prints the current working directory
- **ls:** lists the contents of the current directory
- **ls** directory: lists the contents of the received directory
- **ls** -l: lists the additional information for the contents of the directory
- **ls** -a: lists all files, including those hidden
- **ls** -la: applies both the -l and the -a flags
- **mkdir** directory: creates the directory with the received name
- **rmdir** directory: deletes the directory with the received name (if empty)
- **cp** `<old_name>` `<new_name>`: copies old_name into new_name
- **mv** `<old_name>` `<new_name>`: moves old_name into new_name
- **touch** `<file_name>`: creates an empty file or updates the modified time if it exists
- **chmod** modifiers files: changes the permissions for the files according to the provided modifiers; we've seen +x to make the file executable
- **chown** user files: changes the owner of the files to the given user
- **chgrp** group files: changes the group of the files to the given group
### Operating with the content of files
- **cat** file: shows the content of the file through standard output
- **wc** file: counts the amount of characters, words, and lines in the given file; can also count the same values of whatever it receives via stdin    
- **file** file: prints the type of the given file, as recognized by the operating system
- **head** file: shows the first 10 lines of the given file    
- **tail** file: shows the last 10 lines of the given file
- **less** file: scrolls through the contents of the given file (press "q" to quit)
- **sort** file: sorts the lines of the file alphabetically
- **cut -d** `<separator>` **-f** `<fields>` file: for each line in the given file, splits the line according to the given separator and prints the given fields (starting from 1)
### Additional commands
- **echo** "message": prints the message to standard output
- **date:** prints the current date
- **who:** prints the list of users currently logged into the computer
- **man**: shows the manual page of the given command; manual pages contain a lot of information explaining how to use each command (press "q" to quit)
- **uptime:** shows how long the computer has been running
- **free:** shows the amount of unused memory on the current system
## Redirections, Pipes, and Signals
### Managing streams
These are the redirectors that we can use to take control of the streams of our programs
- command **>** file: redirects standard output, overwrites file
- command **>>** file: redirects standard output, appends to file
- command **<** file: redirects standard input from file
- command **2>** file: redirects standard error to file
- command1 **|** command2: connects the output of command1 to the input of command2
### Operating with processes
These are some commands that are useful to know in Linux when interacting with processes. Not all of them are explained in videos, so feel free to investigate them on your own.
- **ps:** lists the processes executing in the current terminal for the current user
- **ps** ax: lists all processes currently executing for all users
- **ps** e: shows the environment for the processes listed
- **kill** PID: sends the SIGTERM signal to the process identified by PID
- **fg**: causes a job that was stopped or in the background to return to the foreground
- **bg:** causes a job that was stopped to go to the background
- **jobs:** lists the jobs currently running or stopped
- **top:** shows the processes currently using the most CPU time (press "q" to quit)
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

| Command | Explanation & Link |
| :-----: | -----------------|
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
|git clone URL|[Git clone is used to clone a remote repository into a local workspace](https://git-scm.com/docs/git-clone)|
|git push|[Git push is used to push commits from your local repo to a remote repo](https://git-scm.com/docs/git-push)|
|git pull|[Git pull is used to fetch the newest updates from a remote repository](https://git-scm.com/docs/git-pull)|
|git remote|[Lists remote repos](https://git-scm.com/docs/git-remote)|
|git remote -v|[List remote repos verbosely](https://git-scm.com/docs/git-remote#Documentation/git-remote.txt--v)|
|git remote show `<name>`|[Describes a single remote repo](https://git-scm.com/docs/git-remote#Documentation/git-remote.txt-emshowem)|
|git remote update|[Fetches the most up-to-date objects](https://git-scm.com/docs/git-remote#Documentation/git-remote.txt-emupdateem)|
|git fetch|[Downloads specific objects](https://git-scm.com/docs/git-fetch)|
|git branch -r|[Lists remote branches](https://git-scm.com/docs/git-branch#Documentation/git-branch.txt--r); can be combined with other branch arguments to manage remote branches|

>.gitignore files are used to tell the git tool to intentionally ignore some files in a given Git repository. For example, this can be useful for configuration files or metadata files that a user may not want to check into the master branch. Check out more at: [https://git-scm.com/docs/gitignore](https://git-scm.com/docs/gitignore)
>
>A few common examples of file patterns to exclude can be found [here](https://gist.github.com/octocat/9257657).
## Troubleshooting and Debugging Techniques

- Troubleshooting - The process of identifying, analyzing, and solving problems
- Debugging - The process of identifying, analyzing, and removing bugs in a system/program
- Debuggers - Let us follow the code line by line, inspect changes in variable assignments, interrupt the program when a specific condition is met, and more
- System calls - Calls that the programs running on our computer make to the running kernel
- Cache - Stores data in a form that's faster to access than its original form
- Memory Leak - Memory which is no longer needed is not getting released (made available)
- Undefined Behavior - The code is doing something that's not valid in the programming language
### Tools
- `strace <command>` - Look at the system calls made by a program
	- Use in conjunction with the following commands:
		- `less` - Allows us to scroll through the text
		- `-o <filename>` flag - Saves the output to a file
- `ltrace <command>` - Look at the library calls made by the software
- `iotop` - View which processes are using the most input/output
- `iostat` - View statistics on the input/output operations
- `vmstat` - View statistics on the virtual memory operations
- `psutil` - (Process and System Utilities) is a cross-platform library for retrieving information on running processes and system utilization (CPU, memory, disks, network, sensors) in Python.
- Valgrind - Very powerful tool that can tell us if the code is doing any invalid operations, no matter if it crashes or not
- `gdb` - Debug a core dump and stop where the failure was recorded
- `backtrace` - Used to show a summary of the function calls that were used to the point where the failure occurs.
### Reproduction Case
- A clear description of how and when the problem appears
#### Steps:
1. Getting Information
2. Finding the root cause
3. Performing the necessary remediation
### Logs
- Linux
	- /var/log/syslog
	- .xsession-errors (found in each users home directory)
- MacOS
	- /Library/Logs
- Windows
	- Event Viewer
- Centralized Logs Collection - A special server that gathers all the logs from all of the servers, or even all of the computers on the network (eg. SIEM)
### Linux Commands/Tools
- `netstat` - view open ports on system
	- Flags:
		- `-n` - Prints IPs instead of resolving hostnames
		- `-l` - Only check sockets that are listening
## Documentation
- Postmortems - Documents that describe details of incidents to help us learn from our mistakes
	- What caused the issue?
	- What the impact of the issue was
	- How it got diagnosed
	- The short-term remediation you applied
	- The long-term remediation you recommend
- Highlight the impact, root cause, and action items under an executive summary at the beginning.
- Break down the root cause and trigger followed by a "Lessons Learned"
## Writing Efficient Code
- Profiler - A tool that measures the resources that our code is using, giving us a better understanding of what's going on
	- Tools:
		1. gprof - Used to analyze programs written in C
		2. cProfile module - Used to analyze Python programs
		3. pprofile3 - Deterministic and Statistic Python 3 profiler
		4. `time` - Measures program completion time
- Expensive actions - Those that can take a long time to complete
- Time outputs the measurement in 3 formats:
	1. real - The amount of actual time that it took to execute the command, sometimes referred to as "wall-clock time".
	2. user - The time spent doing operations in the user space
	3. sys - The time spent doing system-level operations
## Transferring Files
- `rsync [Options] [Source-Files-Dir] [Destination]` - (Remote Sync) is a utility for efficiently transferring and synchronizing files between a computers and an external hard drive and across networked computers by comparing the modification time and size of files.
	- One of the important features of rsync is that it works on the "delta transfer algorithm", which means it'll only sync or copy the changes from the source to the destination instead of copying the whole file. This ultimately reduces the amount of data sent over the network.

- Basic syntax:

| Options | Uses |
| :-- | :-- |
| `-v` | Verbose Output |
| `-q` | Suppress message output |
| `-a` | Archive files and directory while synchronizing |
| `-r` | Sync files and directories recursively |
| `-b` | Take the backup during synchronization |
| `-z` | Compress file data during the transfer |

- Copy or sync files locally:
	- `rsync -zvh [Source-Files-Dir] [Destination]`
- Copy or sync directories locally:
	- `rsync -zavh [Source-Files-Dir] [Destination]`
- Copy files and directories recursively locally:
	- `rsync -zrvh [Source-Files-Dir] [Destination]`
## Introduction to Automation at Scale

Puppet is an automation tool used for managing and configuring computer systems, particularly in IT infrastructure and server environments. It helps organizations automate the deployment, configuration, and maintenance of software and settings on a large scale. Here's a simple explanation of how Puppet works and how it can be used with Python:

1. **Configuration Management:** Puppet allows you to define the desired state of your servers and infrastructure using code, which is called "Puppet manifests." These manifests specify how each system should be configured, including which software to install, what settings to apply, and how services should run.

2. **Agent-Based:** Puppet operates on a client-server model. It has a central server (Puppet Master) and agent nodes (Puppet Agents) installed on the managed systems. The Puppet Master stores and distributes the configuration manifests, while Puppet Agents apply those configurations on their respective systems.

3. **Declarative Language:** Puppet uses a declarative language, which means you describe what you want the system to look like rather than specifying the steps to get there. This makes it easier to manage complex configurations.

4. **Idempotent:** Puppet is idempotent, meaning it ensures that the desired system state is reached, even if you apply the configuration multiple times. If a configuration is already in the desired state, Puppet won't make unnecessary changes.

5. **Fact:** hash that stores information about the details of a particular system.

Now, regarding Python:

- Puppet can execute various actions on managed systems, including running scripts and commands. This is where Python comes into play. You can use Python scripts within your Puppet manifests to perform specific tasks or custom configurations on your servers.

- For example, you can write a Puppet manifest that installs Python on all your servers and then uses Python scripts to configure specific applications or services. Python is a versatile scripting language that can be integrated into Puppet to extend its capabilities.

- Puppet also has a built-in module for managing Python packages and virtual environments, making it easier to manage Python-related configurations.

In summary, Puppet is an automation tool that helps manage and configure computer systems, and it can work seamlessly with Python by allowing you to use Python scripts within your configuration manifests to customize and automate tasks on your servers. This combination provides flexibility and scalability in managing your infrastructure.

- Module - Used to organize the configuration management tools.
- Node Definitions - Used to apply different rule catalogs to various types of machines
- Certificate Authority (CA) - Either queues a certificate request for manual validation, or uses pre-shared data to verify before sending the certificate to the agent. (Validates the identity of each machine)
### Puppet Commands
- `puppet apply -v <manifest_file_here.pp>` - Applies the puppet manifest for future execution.
- `=>` - Used to define all rules
- `puppet parser validate` - Checks the syntax of the manifest.
## Cloud Computing
- Containers - applications that are packaged together with their configuration and dependencies.

- Infrastructure as a Service (IaaS) - provides users with the bare minimum needed to utilize a server's computational resources, such as a virtual machine. It is the user's responsibility to configure everything else.
- Software as a Service (SaaS) - A cloud provider delivers an entire application or program to the customer
- Platform as a Service (PaaS) - A cloud provider offers a preconfigured platform to the customer
### Scaling
- Automatic scaling - The service offered by the Cloud provider will use metrics to automatically increase or decrease the capacity of the system.
- Manual scaling - Changes are controlled by humans instead of software.
## Capstone Project
### Recap from previous courses
- Web Application - application that you interact with over HTTP. 
- Web Services - web application that also have an API.
- API Call - Used to send a message to a web service
- API Endpoint - The part of the program that listens on the network for API calls
- Data Serialization - process of taking an in-memory data structure, like a Python object, and turning it into something that can be stored on disk or transmitted across a network.

Example serialization with JSON
```Python
import json

with open('people.json', 'w') as people_json:
    json.dump(people, people_json, indent=2)
    
# This code uses the **json.dump()** function to serialize the **people** object into a JSON file.
[
  {
	"name": "Sabrina Green",
	"username": "sgreen",
	"phone": {
	  "office": "802-867-5309",
	  "cell": "802-867-5310"
	},
	"department": "IT Infrastructure",
	"role": "Systems Administrator"
  },
  {
	"name": "Eli Jones",
	"username": "ejones",
	"phone": {
	  "office": "684-348-1127"
	},
	"department": "IT Infrastructure",
	"role": "IT Specialist"
  },
]
```

Example serialization with YAML (Yet Another Markup Language)
```Python
import yaml

with open('people.yaml', 'w') as people_yaml:
    yaml.safe_dump(people, people_yaml)

# In this example, we’re using the **yaml.safe_dump()** method to serialize our object into YAML:
- department: IT Infrastructure
  name: Sabrina Green
  phone:
    cell: 802-867-5310
    office: 802-867-5309
  role: Systems Administrator
  username: sgreen
- department: IT Infrastructure
  name: Eli Jones
  phone:
    office: 684-348-1127
  role: IT Specialist
  username: ejones
```

#### JSON
- JSON is **human-readable**, which means it's encoded using printable characters, and formatted in a way that a human can understand.
- Supports a few elements of different data types:
	- **Strings** - enclosed in quotes
	- **Numbers**
	- **Objects** - key-value pair structures like Python dictionaries
		- These key-value pairs can also contain another object as a value.
	- **Arrays** - Equivalent to Python lists.
		- Can contain strings, numbers, objects, or other arrays.
- JSON elements are always **comma-delimited**.
- **.dump()** method is used to serialize JSON data to a file.
- **.dumps()** method will return the string of data rather than dumping to a file.
- **.load()** method does the inverse and will deserialize JSON from a file into basic Python objects.
- **.loads()** method also does the inverse and will deserialize JSON from a string into a basic Python object.
#### Requests library
Example basic request for a webpage
```Python
import requests

response = requests.get('https://www.google.com')

# To view what is stored in the response
print(response.text[:300]) # Grabs the first 300 characters

# <!doctype html><html itemscope="" itemtype="http://schema.org/WebPage" lang="de"><head><meta content="text/html; charset=UTF-8" http-equiv="Content-Type"><meta content="/images/branding/googleg/1x/googleg_standard_color_128dp.png" itemprop="image"><title>Google</title><script nonce="dZfbIAn803LDGXS9

# Instead, we can look at the raw response data
response = requests.get('https://www.google.com', stream=True)

# Output the first 100 characters of raw data
print(response.raw.read()[:100])

# b'\x1f\x8b\x08\x00\x00\x00\x00\x00\x02\xff\xc5Z\xdbz\x9b\xc8\x96\xbe\xcfS`\xf2\xb5-\xc6X\x02$t\xc28\xe3v\xdc\xdd\xee\xce\xa9\xb7\xdd;\xe9\x9d\xce\xf6W@\t\x88\x11`@>D\xd6\x9b\xce\xe5<\xc3\\\xcd\xc5\xfc\xab8\x08\xc9Nz\x1f.&\x8e1U\xb5j\xd5:\xfc\xb5jU\x15\x87;^\xe2\x16\xf7)\x97\x82b\x1e\x1d\x1d\xd2S'

# To check if a request was good or not
response.ok
# True or False

# You can also get the status code
response.status_code
# 200, 400, 404, etc.

# Always good practice to check status codes before proceeding
response = requests.get(url)
if not response.ok:
    raise Exception("GET failed with status code {}".format(response.status_code))
    
# The code block above isn't necessarily needed either as we can use the .raise_for_status() method
response = requests.get(url)
response.raise_for_status()
```

- GET method - By sending a GET request, you're asking the server to GET the resource for you.
	- A GET request can have parameters.
		- A question mark will be used to separate the URL from the parameters.
```Python
p = {"search": "grey kitten", "max_results": 15}
response = requests.get("https://example.com/path/to/api", params=p)
response.request.url

# 'https://example.com/path/to/api?search=grey+kitten&max_results=15'
```

- POST method - used to respond to forms or submit data to web sites.
	- Instead of setting the params attribute, which gets turned into a query string and appended to the URL, we use the **data** attribute, which contains the data that will be sent as part of the POST request.
```Python
p = {"description": "white kitten", "name": "Snowball", "age_months": 6}
response = requests.post("https://example.com/path/to/api", data=p)
response.request.url

# 'https://example.com/path/to/api'

# The data parameters have been tied into the body of the HTTP message rather than the URL, to see these we can use the **body** attribute
response.request.body

# 'description=white+kitten&name=Snowball&age_months=6'

# So, if we need to send and receive data from a web service, we can turn our data into dictionaries and then pass that as the **data** attribute of a POST request.

# Today, it's super common to send and receive data specifically in JSON format, so the Requests module can do the conversion directly for us, using the **json** parameter.

response = requests.post("https://example.com/path/to/api", json=p)
response.request.url

# 'https://example.com/path/to/api'

response.request.body

# b'{"description": "white kitten", "name": "Snowball", "age_months": 6}'
```

#### Email Message Module
- Email Header Fields (Always key-value pairs)
	- From
	- To
	- Subject

```Python
# Create an empty email message
>>> from email.message import EmailMessage
>>> message = EmailMessage()
>>> print(message) # Outputs the string representation of the object

# To see more than the above, we can start assigning values to message dictionary
>>> sender = 'me@example.com'
>>> recipient = 'you@example.com'

# Assign them to the From and To fields of the message
>>> message['From'] = sender
>>> message['To'] = recipient
>>> print(message)
# From: me@example.com
# To: you@example.com

# Subject assignment
>>> message['Subject'] = 'Greetings from {} to {}!'.format(sender, recipient)
>>> print(message)
# From: me@example.com
# To: you@example.com
# Subject: Greetings from me@example.com to you@example.com!

# Add the message body
>>> body = """Hey there!
...
... I'm learning to send emails using Python!"""
>>> message.set_content(body)
>>> print(message)
# From: me@example.com
# To: you@example.com
# Subject: Greetings from me@example.com to you@example.com!
# MIME-Version: 1.0
# Content-Type: text/plain; charset="utf-8"
# Content-Transfer-Encoding: 7bit

# Hey there!

# I'm learning to send email using Python!
```

- Adding Attachments
	- Whenever an attachment is sent in an email, the attachment is encoded into the email as some form of text. This is called the Multipurpose Internet Mail Extensions (MIME) standard or mime type.
```Python
# If you know the mime type, then you can use that directly otherwise you can use the mimetypes module to make a good guess.
>>> import os.path
>>> attachment_path = "/tmp/example.png"
>>> attachment_filename = os.path.basename(attachment_path)
>>> import mimetypes
>>> mime_type, _ = mimetypes.guess_type(attachment_path)
>>> print(mime_type)
# image/png

# Above, the mime_type string contains the MIME type and subtype, separated by a slash. The EmailMessage type needs a MIME type and subtype as separate strings, so we can split it up.
>>> mime_type, mime_subtype = mime_type.split('/', 1)
>>> print(mime_type)
# image
>>> print(mime_subtype)
# png

# Now we can add it to our email message
>>> with open(attachment_path, 'rb') as ap:
...     message.add_attachment(ap.read(),
...                            maintype=mime_type,
...                            subtype=mime_subtype,
...                            filename=os.path.basename(attachment_path))
... 
>>> print(message)
# Content-Type: multipart/mixed; boundary="===============5350123048127315795=="

# --===============5350123048127315795==
# Content-Type: text/plain; charset="utf-8"
# Content-Transfer-Encoding: 7bit

# Hey there!

# I'm learning to send email using Python!

# --===============5350123048127315795==
# Content-Type: image/png
# Content-Transfer-Encoding: base64
# Content-Disposition: attachment; filename="example.png"
# MIME-Version: 1.0

# iVBORw0KGgoAAAANSUhEUgAAASIAAABSCAYAAADw69nDAAAACXBIWXMAAAsTAAALEwEAmpwYAAAg
# AElEQVR4nO2dd3wUZf7HP8/M9k2nKIJA4BCUNJKgNJWIBUUgEggCiSgeVhA8jzv05Gc5z4KHiqin
# eBZIIBDKIXggKIeCRCAhjQAqx4UiCARSt83uzDy/PzazTDZbwy4BnHde+9qZydNn97Pf5/uUIZRS
# (...We deleted a bunch of lines here...)
# wgAAAABJRU5ErkJggg==

# --===============5350123048127315795==--
```

- Sending the Email through an SMTP Server
```Python
# Import the smptlib module
>>> import smtplib

# Create an smptlib.SMTP object and try to connect to the local machine
>>> mail_server = smtplib.SMTP('localhost')
# Traceback (most recent call last):
#   File "<stdin>", line 1, in <module>
#   (...We deleted a bunch of lines here...)
# ConnectionRefusedError: [Errno 61] Connection refused

# This means that we don't have an SMTP server up and running on our local host, but instead we can connect to the SMTP server for our personal emails.
# When setting this up, you'll most likely need to setup some sort of secure connection using SSL/TLS. To do this, the smtplib module has two classes, the standard .SMTP() class and the .SMTP_SSL() class which creates a connection over SSL/TLS.
>>> mail_server = smtplib.SMTP_SSL('smtp.example.com')

# If you care to see the behind the scenes messages that this module is sending then you can use the debug class
>>> mail_server.set_debuglevel(1)

# We've made the connection to the SMTP server above, but now we need to authenticate using username/password. For this, we'll use the getpass module to prevent leaving our password out in the open for prying eyes.
>>> import getpass
>>> mail_pass = getpass.getpass('Password? ')
# Password?
>>> '<Enter-password-here>'

# Be careful with the mail_pass variable, because it is still storing your password as a string
>>> print(mail_pass)
# It'sASecr3t!

# Now we can authenticate to the email server using the SMTP object's login method
>>> mail_server.login(sender, mail_pass)
# (235, b'2.7.0 Accepted')

# If the login attempt succeeds, the login method will return a tuple of the SMTP status code and a message explaining the reason for the status. If the login attempt fails, the module will raise a SMTPAuthenticationError exception.

# To send the email now
>>> mail_server.send_message(message)
# {}

# Done! The returned dictionary is only populated with recipients that weren't able to receive our message.

# Now that we're done. Close the connection to the server
>>> mail_server.quit()
```
#### Generating PDFs from Python
- There are a few tools available, but we're focusing on ReportLab since it has a ton of features for creating PDF documents.
```Python
# In this example, we have a dictionary of our fruit collection that we want to transcribe into a PDF.
fruit = {
  "elderberries": 1,
  "figs": 1,
  "apples": 2,
  "durians": 3,
  "bananas": 5,
  "cherries": 8,
  "grapes": 13
}

# We'll use the SimpleDocTemplate class to build our PDF
>>> from reportlab.platypus import SimpleDocTemplate
>>> report = SimpleDocTemplate("/tmp/report.pdf")

# The report object just generated a PDF using the filename '/tmp/report.pdf'. Now we can add some content to it.
# ReportLab uses something called Flowables. These are essentially chunks of a document that reportlab can arrange to make a complete report.
>>> from reportlab.platypus import Paragraph, Spacer, Table, Image

# Each of those classes build a part of the document, but we also need to tell reportlab how to style the document.
>>> from reportlab.lib.styles import getSampleStyleSheet
>>> styles = getSampleStyleSheet()

# Add a document title
>>> report_title = Paragraph("A Complete Inventory of My Fruit", styles["h1"])

# Now we'll add a table based on our fruit data
>>> table_data = []
>>> for k, v in fruit.items():
...   table_data.append([k, v])
...
>>> print(table_data)
# [['elderberries', 1], ['figs', 1], ['apples', 2], ['durians', 3], ['bananas', 5], ['cherries', 8], ['grapes', 13]]

# Now we have a list of lists that we can add to our report
>>> report_table = Table(data=table_data)
>>> report.build([report_title, report_table])

# The table is there, but it's pretty ugly so we can modify our code to style it.
>>> from reportlab.lib import colors
>>> table_style = [('GRID', (0,0), (-1,-1), 1, colors.black)]
>>> report_table = Table(data=table_data, style=table_style, hAlign="LEFT")
>>> report.build([report_title, report_table])

# Add graphics to the PDF. We'll add a pie chart
>>> from reportlab.graphics.shapes import Drawing
>>> from reportlab.graphics.charts.piecharts import Pie
>>> report_pie = Pie(width=3*inch, height=3*inch)

# For the Pie chart, we need two lists. One for the data and another for the labels.
>>> report_pie.data = []
>>> report_pie.labels = []
>>> for fruit_name in sorted(fruit):
...   report_pie.data.append(fruit[fruit_name])
...   report_pie.labels.append(fruit_name)
...
>>> print(report_pie.data)
# [2, 5, 8, 3, 1, 1, 13]
>>> print(report_pie.labels)
# ['apples', 'bananas', 'cherries', 'durians', 'elderberries', 'figs', 'grapes']

# The pie object isn't Flowable, but it can be placed inside of a Flowable Drawing.
>>> report_chart = Drawing()
>>> report_chart.add(report_pie)

# Add the Drawing to the report
report.build([report_title, report_table, report_chart])
```