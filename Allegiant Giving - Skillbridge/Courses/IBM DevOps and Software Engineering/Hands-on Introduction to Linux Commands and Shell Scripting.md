---
tags:
  - Linux
  - Scripting
  - Networks
---
# Courses
1. [IBM DevOps and Software Engineering Professional Certificate](https://www.coursera.org/programs/allegiant-giving-corporation-on-demand-learning-program-mjqmr/professional-certificates/devops-and-software-engineering)
	1. [Introduction to Linux Commands and Shell Scripting](https://www.coursera.org/learn/hands-on-introduction-to-linux-commands-and-shell-scripting/supplement/6RSNt/how-to-get-the-most-from-this-hands-on-course)

# Cheat Sheet - Introduction to Linux

## Linux terminal tips
---

> Use **tab completion** to autocomplete pathnames and command names.

> Scroll through your **command history** with the `Up Arrow` and `Down Arrow` keys to find and re-run a command you already used.
## Getting information
---
### Display the reference manual for the `ls` command:

1. `man ls`
## Browsing and navigating directories
---
### Special paths
|Symbol|Represents path to|
|---|---|
|`~`|home directory|
|`/`|root directory|
|`.`|present working directory|
|`..`|parent of present working directory|
### List files and directories in the current directory:

1. `ls`
### List files and directories in a directory:

1. `ls path_to_directory`
### Return path to present working directory:

1. `pwd`
### Change the current directory to a subdirectory:

1. `cd child_directory_name`

> **Tip**: Because `cd` looks in the current directory for `child_directory_name`, you don’t need to type the entire path.
### Change the current directory:

**Up one level:** `cd ../`

**To home:** `cd ~` or `cd`

**To some other directory:** `cd path_to_directory`

### Change the current directory to another one at the same level:

 Suppose you have two sibling directories within the same directory, `dir_1` and `dir_2`, and your present working directory is `dir_1`. To switch to `dir_2`, enter:
 	 `cd ../dir_2`

> **Tip**: Using `..`, you don't need to know the path to the parent directory to switch to a sibling.

### Change the current directory back to the directory you were in previously:

	 `cd -`
## Upgrading and installing packages
---
### Fetch and display up-to-date information about all upgradable packages:

1. `sudo apt update`
### Upgrade to the latest supported version of nano:

1. `sudo apt upgrade nano`
### Install Vim:

1. `sudo apt install vim`

## Creating and editing files
---
### Create a new text file and open it with nano:

1. `nano file_name.txt`

> **Tip**: If the file already exists, nano simply opens it for editing.

## Summary - Week 1

- Linux is a multi-user and portable operating system that supports multitasking. It originated in the 1980s when Linus Torvalds developed a free, open-source version of the Unix kernel.  
- Linux is widely used today in mobile devices, desktops, supercomputers, data centers, and cloud servers.
- Linux distributions (also known as distros) differ by their UIs, shell applications, and how the OS is supported and built.
- The design of a distro is catered toward its specific audience and/or use case. Popular Linux distributions include Red Hat Enterprise Linux (RHEL), Debian, Ubuntu, Suse (SLES, SLED, OpenSuse), Fedora, Mint, and Arch.
- The Linux system consists of five key layers: the UI, application, OS, kernel, and hardware. The user interface enables users to interact with applications. Applications enable users to perform tasks within the system. The operating system runs on top of the kernel and is vital for system health and stability, and the kernel is the lowest-level software that enables applications to interact with hardware. Hardware includes all the physical or electronic components of your PC.
- The Linux filesystem is a tree-like structure consisting of all directories and files on the system.
- A Linux shell is an OS-level application that you can use to enter commands. You use a terminal to send commands to the shell, and you can use the `cd` command to navigate around your Linux filesystem.
- You can use a variety of command-line or GUI-based text editors such as GNU nano, vim, vi, and gedit.
- .deb and .rpm are distinct file types used by package mangers in Linux operating systems.
- You can use GUI-based and command-line package managers to update and install software on Linux systems.

### Why do we need file permissions and ownership?

Linux is a multi-user operating system. This means that by default, other users will be able to view any files you store on the system. However, you may have some files - such as your personal tax documents or your employer's intellectual property documents - that are private or confidential. How can you protect these sensitive documents from being viewed or modified by others?

### File ownership and permissions

There are three possible levels of file ownership in Linux: user, group, and other.  
Whoever creates a file, namely the **user** at the time of creation, becomes the owner of that file by default. A **group** of users can also share ownership of a file. The **other** category essentially refers anyone in the universe with access to your Linux machine - careful when assigning ownership permission to this level!

Only an official owner of a file is allowed to change its permissions. This means that only owners can decide who can read the file, write to it, or execute it.

### Viewing file permissions

Let's say you've entered the following lines of code:

1. `$ echo "Who can read this file?" > my_new_file`
2. `$ more my_new_file`
3. `Who can read this file?`
4. `$ ls -l my_new_file`
5. `-rw-r--r-- 1 theia users 25 Dec 22 17:47 x`

Here we've echoed the string `"Who can read this file?"` into a new file called `my_new_file`. The next line uses the `more` command to print the contents of the new file. Finally, the `ls` command with the `-l` option displays the file's (default) permissions: `rw-r--r--`

The first three characters (`rw-`) define the **user** permissions, the next three (`r--`) the **group** pemissions, and the final three (`r--`) the **other** permissions.

So you, being the user, have the permission `rw-`, which means you have read and write permissions by default, but do not have execution permissions. Otherwise there would be an `x` in place of the last `-`.

Thus by looking at the entire line, `rw-r--r--`, you can see that anyone can read the file, nobody can execute it, and you are the only user that can write to it.

> **Note:** The `-` at the very beginning of the line in the terminal means that the permissions are referring to a file. If you were getting the permissions to a directory, you would see a `d` in the front for "directory".

### Directory permissions

The permissions for directories are similar but distinct for files. Though directories use the same `rwx` format, the symbols have slightly different meanings.

The following table illustrates the meanings of each permission for directories:

|Directory Permission|Permissible action(s)|
|---|---|
|`r`|List directory contents using `ls` command|
|`w`|Add or remove files or directories|
|`x`|Enter directory using `cd` command|

Setting appropriate permissions on directories is a best practice for both security and stability reasons. Though this reading focuses on security, you will learn more about other reasons for setting file permissions and ownership later in this course.

### Making a file private

You can revoke read permissions from your group and all other users by using the `chmod` command. Ensure successful modification by using the `ls -l` command again:

1. `chmod go-r my_new_file`
2. `ls -l my_new_file`
3. `-rw------- 1 theia users 24 Dec 22 18:49 my_new_file`

In the `chmod` command, `go-r` is the permission change to be applied, which in this case means removing for the group (`g`) and others (`o`) the read (`r`) permission. The `chmod` command can be used with both files and directories.

### Executable files - looking ahead

You've learned what it means to read or write to a file, but what does it mean to have permissions to **execute** a file in Linux?

A Linux file is executable if it contains instructions that can be directly interpreted by the operating system. Basically, an exectuable file is a ready-to-run program. They're also referred to as **binaries** or **executables**.

In this course, you will become very familiar with a particular kind of executable called a **script**, which is a program written in a scripting language. You'll learn all about **shell scripting**, or more specifically **Bash scripting**, which is writing scripts in Bash (_born-again shell_), a very popular shell scripting language. A shell script is a plain text file that can be interpreted by a shell.

Formally speaking, for a text file to be considered an executable shell script for a given user, it needs to have two things:

1. Execute permissions set for that user
2. A directive, called a "shebang", in its first line to declare itself to the operating system as a binary

All of this will become more clear to you soon when we get to the topic of shell scripting.

## Computer Networks

A **computer network** is a set of computers that are able to communicate with each other and share **resources** provided by **network nodes**.

> Examples of computer networks include Local Area Networks (LANs), Wide Area Networks (WANs), and the entire Internet. The Internet, or World Wide Web, is essentially a giant network of computer networks.

A network **resource** is any object, such as a file or document, which can be _identified_ by the network.

> An object is identifiable if it can be assigned a unique name and address that the network can use to identify and access it.

A **network node** is any device that participates in a network.

> A network can include any device which is not necessarily a computer but is part of the network’s infrastructure. Examples of network nodes include modems, network switches, hubs, and wifi hotspots.

## Hosts, Clients, and Servers

A **host** is a special type of node in a computer network - it is a computer that can function as a **server** or a **client** on a network.

A **server** is a host computer that is able to accept a connection from a **client** host and fulfill certain resource requests made by the client.

Many hosts can perform either role, acting as both client and server.

## Packets and Pings

A **network packet** is a formatted chunk of data that can be transmitted over a network.

Today's computer networks typically use communication protocols that are based on such packets of information. Every packet consists of two types of data: 1. the **control information**, and 2. the **payload**. The control information is data about how and where to deliver the payload, such as the source and destination network addresses, while the payload is the message being sent.

The `ping` command works by sending special 'echo request' packets to a host and waiting for a response from the host.

> `ping` is a utility available on most operating systems that have networking capability. Linux has its own implementation of the `ping` command that's used to test and troubleshoot connectivity to other network hosts.

## URLs and IP Adresses

IP stands for "Internet Protocol" which defines the format of data transmitted over the internet or a local network.

An **IP address** is a code used to uniquely identify any host on a network.

> An IP address can be used to establish a connection to a host and exchange packets with it, for example using the `ping` command. In addition to their payload, IP packets - a type of network packet that conforms to the Internet Protocol - contain the IP addresses of the source and destination hosts.

A **URL**, more commonly known as a web address, stands for _Uniform Resource Locator_.

> A URL uniquely identifies a web resource and enables access to that resource. Typically the resource that a URL points to is a web page, but it can also be used for tasks such as transferring files, sending emails, and accessing databases.

> For example, the URL to the Wikipedia page for URL is `https://en.wikipedia.org/wiki/URL`. Just like for a typical URL, its format indicates a protocol (`https`), a hostname (`en.wikipedia.org`), and a file name (`/wiki/URL`).

## Summary - Week 2

- A shell is an interactive user interface. You use shell commands to navigate and work with files and directories.
- The `curl` and `wget` commands display and download files from URLs, and the`cat` and `tail`commands display file contents.
- You can get user information with the `whoami` and `id`commands, and get operating system information using the `uname` command. You can check system disk usage using the `df` command and monitor processes and resource usage with `ps` and `top`.Print string or variable value using `echo`,print and extract information about the date with the `date` command, and read the manual for any command using `man`.
- `ls` lists all files and directories within a specified directory tree and `cd` navigates between directories. The `find` command finds files in your directories.
- Relative paths are relative to your current working directory, while absolute paths stand independently
- You can create files and directories with the `touch` and `mkdir` commands, delete them with `rm` and `rmdir`, and copy and move them `cp` and `mv`.
- The `cat`, `more`, `head`, and `tail` commands allow you to sort and view file contents or view only a certain number of lines. Determine line, word, and character counts with `wc`.
- You can use `sort` to view the lines of a file alphanumerically and `uniq` to remove repeated lines from your view. `grep` gets the lines of a file that match your desired criteria, and `cut` extracts slices and fields from lines. You can merge lines from different files using `paste`.
- `hostname` and `ifconfig` allow you to view the network configuration. You can test a network connection using `ping` and send and receive data using `curl` and `wget`.
- Compression preserves storage space, speeds data transfer, and reduces system load.
- `zip` compresses files and folders prior to archiving them. `tar` archives and compresses files and directories into a tarball. `unzip` unpacks and decompresses a zipped archive, and `tar` can also decompress and unpack a tar.gz archive.

# Module 2 Cheat Sheet - Introduction to Linux Commands

### Getting information

---

##### Return your user name:

1. 1

1. `whoami`

Copied!

##### Return your user and group id:

1. 1

1. `id`

Copied!

##### Return operating system name, username, and other info:

1. 1

1. `uname -a`

Copied!

##### Display reference manual for a command:

1. 1

1. `man top`

Copied!

##### List available `man` pages, including a brief description for each command:

1. 1

1. `man -k .`

Copied!

##### Get help on a command:

1. 1

1. `curl --help`

Copied!

##### Return the current date and time:

1. `date`
### Navigating and working with directories
---

##### List files and directories by date, newest to last:

1. 1

1. `ls -lrt`

Copied!

##### Find files in directory tree that end in `.sh`:

1. 1

1. `find -name \'\*.sh\'`

Copied!

##### Return path to present working directory:

1. 1

1. `pwd`

Copied!

##### Make a new directory:

1. 1

1. `mkdir new_folder`

Copied!

##### Change the current directory:

> **Up one level:**

1. 1

1. `cd ../`

Copied!

> **To home:**

1. 1

1. ``cd ~` or `cd``

Copied!

> **To some other directory:** `cd path_to_directory`

##### Remove directory verbosely:

1. 1

1. `rmdir temp_directory -v`

Copied!

### Monitoring system performance and status

---

##### List selection of/all running processes and their PIDs:

1. 1

1. `ps`

Copied!

1. 1

1. `ps -e`

Copied!

##### Display resource usage:

1. 1

1. `top`

Copied!

##### List mounted file systems and usage:

1. 1

1. `df`

Copied!

### Creating, copying, moving, and deleting files:

---

##### Create an empty file or update existing file's timestamp:

1. 1

1. `touch a_new_file.txt`

Copied!

##### Copy a file:

1. 1

1. `cp file.txt new_path/new_name.txt`

Copied!

##### Change file name or path:

1. 1

1. `mv this_file.txt that_path/that_file.txt`

Copied!

##### Remove a file verbosely:

1. 1

1. `rm this_old_file.txt -v`

Copied!

### Working with file permissions

---

##### Change/modify file permissions to 'execute' for all users:

1. 1

1. `chmod  +x  my_script.sh`

Copied!

##### Change/modify file permissions to 'execute' only for you, the current user:

1. 1

1. `chmod u+x my_file.txt`

Copied!

##### Remove 'read' permissions from group and other users:

1. 1

1. `chmod go-r`

Copied!

### Displaying file and string contents

---

##### Display file contents:

1. 1

1. `cat my_shell_script.sh`

Copied!

##### Display file contents page-by-page:

1. 1

1. `more ReadMe.txt`

Copied!

##### Display first 10 lines of file:

1. 1

1. `head -10 data_table.csv`

Copied!

##### Display last 10 lines of file:

1. 1

1. `tail -10 data_table.csv`

Copied!

##### Display string or variable value:

1. 1
2. 2

1. `echo "I am not a robot"`  
2. `echo "I am $USERNAME"`

Copied!

### Basic text wrangling

---

#### Sorting lines and dropping duplicates:

##### Sort and display lines of file alphanumerically:

1. 1

1. `sort text_file.txt`

Copied!

> ##### In reverse order:

1. 1

1. `sort -r text_file.txt`

Copied!

##### Drop consecutive duplicated lines and display result:

1. 1

1. `uniq list_with_duplicated_lines.txt`

Copied!

#### Displaying basic stats:

##### Display the count of lines, words, or characters in a file:

> **Lines:**

1. 1

1. `wc  -l table_of_data.csv`

Copied!

> **Words:**

1. 1

1. `wc  -w my_essay.txt`

Copied!

> **Characters:**

1. 1

1. `wc  -m some_document.txt`

Copied!

#### Extracting lines of text containing a pattern:

Some frequently used options for `grep`:

|Option|Description|
|---|---|
|`-n`|Print line numbers along with matching lines|
|`-c`|Get the count of matching lines|
|`-i`|Ignore the case of the text while matching|
|`-v`|Print all lines which do not contain the pattern|
|`-w`|Match only if the pattern matches whole words|

##### Extract lines containing the word "hello", case insensitive and whole words only:

1. 1

1. `grep  -iw hello  a_bunch_of_hellos.txt`

Copied!

##### Extract lines containing the pattern "hello" from all files in the current directory ending in `.txt`:

1. 1

1. `grep  -l hello  *.txt`

Copied!

#### Merge two or more files line-by-line, aligned as columns:

Suppose you have three files containing the first and last names of your customers, plus their phone numbers.

##### Use `paste` to align file contents into a Tab-delimited table, one row for each customer:

1. 1

1. `paste first_name.txt last_name.text phone_number.txt`

Copied!

##### Use a comma as a delimiter instead of the default Tab delimiter:

1. 1

1. `paste -d "," first_name.txt last_name.text phone_number.txt`

Copied!

#### Use the `cut` command to extract a column from a table-like file:

Suppose you have a text file whos rows consist of first and last names of customers, delimited by a comma.

##### Extract first names, line-by-line:

1. 1

1. `cut -d "," -f 1 names.csv`

Copied!

##### Extract the second to fifth characters (bytes) from each line of a file:

1. 1

1. `cut -b 2-5 my_text_file.txt`

Copied!

##### Extract the characters (bytes) from each line of a file, starting from the 10th byte to the end of the line:

1. 1

1. `cut -b 10- my_text_file.txt`

Copied!

### Compression and archiving

---

##### Archive a set of files:

1. 1

1. `tar -cvf my_archive.tar.gz file1 file2 file3`

Copied!

##### Compress a set of files:

1. 1
2. 2

1. `zip my_zipped_files.zip file1 file2`   
2. `zip my_zipped_folders.zip directory1 directory2`

Copied!

##### Extract files from a compressed zip archive:

1. 1
2. 2

1. `unzip my_zipped_file.zip` 
2. `unzip my_zipped_file.zip -d extract_to_this_direcory`

Copied!

### Working with networking commands

---

##### Print hostname:

1. 1

1. `hostname` 

Copied!

##### Send packets to URL and print response:

1. 1

1. `ping  www.google.com`

Copied!

##### Display or configure system network interfaces:

1. 1
2. 2

1. `ifconfig`   
2. `ip` 

Copied!

##### Display contents of file at a URL:

1. 1

1. `curl  <url>`

Copied!

##### Download file from a URL:

1. 1

1. `wget  <url>`

## What is a shell variable?

Shell variables offer a powerful way to store and later access or modify information such as numbers, character strings, and other data structures by name. Let's look at some basic examples to get the idea.

Consider the following example.

1. `$ firstname=Jeff`
2. `$ echo $firstname`
3. `Jeff`

The first line assigns the value `Jeff` to a new variable called `firstname`. The next line accesses and displays the value of the variable, using the `echo` command along with the special character `$` in front of the variable name to extract its value, which is the string `Jeff`.

Thus, we have created a new shell variable called `firstname` for which the value is `Jeff`.

This is the most basic way to create a shell variable and assign it to a value all in one step.

## Reading user input into a shell variable at the command line

Here's another way to create a shell variable, using the `read` command.  
After entering

1. `$ read lastname`

on the command line, the shell waits for you to enter some text:

1. `$ read lastname`  
2. `Grossman`  
3. `$` 

Now we can see that the value `Grossman` has just been stored in the variable `lastname` by the `read` command:

1. `$ read lastname`  
2. `Grossman`  
3. `$ echo $lastname`  
4. `Grossman`  

By the way, notice that you can echo the values of multiple variables at once.

1. `$ echo $firstname $lastname`  
2. `Jeff Grossman`  

As you will soon see, the `read` command is particularly useful in shell scripting. You can use it within a shell script to prompt users to input information, which is then stored in a shell variable and available for use by the shell script while it is running. You will also learn about **command line arguments**, which are values that can be passed to a script and automatically assigned to shell variables.

## What are pipes?

Put simply, pipes are commands in Linux which allow you to use the output of one command as the input of another.

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/module%201/images/pipes.jpeg)  
  
Pipes `|` use the following format:

1. 1

1. `[command 1] | [command 2] | [command 3] ... | [command n]`

Copied!

There is no limit to the number of times you can chain pipes in a row!

In this lab, you'll take a closer look at how you can use pipes and filters to solve basic data processing problems.

## Pipe examples

### Combining commands

Let's start with a commonly used example. Recall the following commands:

- [`sort`](https://man7.org/linux/man-pages/man1/sort.1.html) - sorts the lines of text in a file and displays the result
- [`uniq`](https://man7.org/linux/man-pages/man1/uniq.1.html) - prints a text file with any consecutive, repeated lines collapsed to a single line

With the help of the pipe operator, you can combine these commands to print all the unique lines in a file.

Suppose you have the file `pets.txt` with the following contents:

1. `$ cat pets.txt`
2. `goldfish`
3. `dog`
4. `cat`
5. `parrot`
6. `dog`
7. `goldfish`
8. `goldfish`

If you _only_ use `sort` on `pets.txt`, you get:

1. `$ sort pets.txt`
2. `cat`
3. `dog`
4. `dog`
5. `goldfish`
6. `goldfish`
7. `goldfish`
8. `parrot`

The file is sorted, but there are duplicated lines of "dog" and "goldfish".

On the other hand, if you _only_ use `uniq`, you get:

1. `$ uniq pets.txt`
2. `goldfish`
3. `dog`
4. `cat`
5. `parrot`
6. `dog`
7. `goldfish`

This time, you removed consecutive duplicates, but non-consecutive duplicates of "dog" and "goldfish" remain.

But by combining the two commands in the correct order - by first using `sort` then `uniq` - you get back:

1. `$ sort pets.txt | uniq`
2. `cat`
3. `dog`
4. `goldfish`
5. `parrot`

Since `sort` sorts all identical items consecutively, and `uniq` removes all consecutive duplicates, combining the commands prints only the unique lines from `pets.txt`!

## Applying a command to strings and files

Some commands such as `tr` only accept _standard input_ - normally text entered from your keyboard - but not strings or filenames.

- [`tr`](https://man7.org/linux/man-pages/man1/tr.1p.html) (translate) - replaces characters in input text

1. `tr [OPTIONS] [target characters] [replacement characters]`

In cases like this, you can use piping to apply the command to strings and file contents.

With strings, you can use `echo` in combination with `tr` to replace all the vowels in a string with underscores `_`:

1. `$ echo "Linux and shell scripting are awesome\!" | tr "aeiou" "_"`
2. `L_n_x _nd sh_ll scr_pt_ng _r_ _w_s_m_!`

To perform the complement of the operation from the previous example - or to replace all the _consonants_ (any letter that is not a vowel) with an underscore - you can use the `-c` option:

1. `$ echo "Linux and shell scripting are awesome\!" | tr -c "aeiou" "_"`
2. `_i_u__a_____e______i__i___a_e_a_e_o_e_`

With files, you can use `cat` in combination with `tr` to change all of the text in a file to uppercase as follows:

1. `$ cat pets.txt | tr "[a-z]" "[A-Z]"`
2. `GOLDFISH`
3. `DOG`
4. `CAT`
5. `PARROT`
6. `DOG`
7. `GOLDFISH`
8. `GOLDFISH`

The possibilities are endless! For example, you could add `uniq` to the above pipeline to only return unique lines in the file, like so:

1. `$ sort pets.txt | uniq | tr "[a-z]" "[A-Z]"`
2. `CAT`
3. `DOG`
4. `GOLDFISH`
5. `PARROT`
## Extracting information from JSON Files:

Let's see how you can use this json file to get the current price of Bitcoin (BTC) in USD, by using grep command.

1. `{`
2.   `"coin": {`
3.     `"id": "bitcoin",`
4.     `"icon": "https://static.coinstats.app/coins/Bitcoin6l39t.png",`
5.     `"name": "Bitcoin",`
6.     `"symbol": "BTC",`
7.     `"rank": 1,`
8.     `"price": 57907.78008618953,`
9.     `"priceBtc": 1,`
10.     `"volume": 48430621052.9856,`
11.     `"marketCap": 1093175428640.1146,`
12.     `"availableSupply": 18877868,`
13.     `"totalSupply": 21000000,`
14.     `"priceChange1h": -0.19,`
15.     `"priceChange1d": -0.4,`
16.     `"priceChange1w": -9.36,`
17.     `"websiteUrl": "http://www.bitcoin.org",`
18.     `"twitterUrl": "https://twitter.com/bitcoin",`
19.     `"exp": [`
20.       `"https://blockchair.com/bitcoin/",`
21.       `"https://btc.com/",`
22.       `"https://btc.tokenview.com/"`
23.     `]`
24.   `}`
25. `}`

Copy the above output in a file and name it as `Bitcoinprice.txt`.

The JSON field you want to grab here is `"price": [numbers].[numbers]"`. To get this, you can use the following `grep` command to extract it from the JSON text:

1. `grep -oE "\"price\"\s*:\s*[0-9]*?\.[0-9]*"`

Let's break down the details of this statement:

- `-o` tells `grep` to _only_ return the matching portion
- `-E` tells `grep` to be able to use extended regex symbols such as `?`
- `\"price\"` matches the string `"price"`
- `\s*` matches any number (including 0) of whitespace (`\s`) characters
- `:` matches `:`
- `[0-9]*` matches any number of digits (from 0 to 9)
- `?\.` optionally matches a `.`

Use the cat command to get the output of the JSON file and pipe it with the grep command to get the required output.

1. `cat Bitcoinprice.txt | grep -oE "\"price\"\s*:\s*[0-9]*?\.[0-9]*"`

You can also extract information directly from URLs and retreive any specific data using such grep commands.

Click here to see the process of extracting information directly from URLs and retreiving specific data:  

1. [](https://openapi.coinstats.app/)

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/images/loginpage.png)

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/images/apikey.png)

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/images/apidocs.png)

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/images/main-page.png)

![](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/images/try-API-output.png)

## Metacharacters

**Metacharacters** are characters having special meaning that the shell interprets as instructions.

|Metacharacter|Meaning|
|---|---|
|`#`|Precedes a comment|
|`;`|Command separator|
|`*`|Filename expansion wildcard|
|`?`|Single character wildcard in filename expansion|

### Pound `#`

The pound `#` metacharacter is used to represent comments in shell scripts or configuration files. Any text that appears after a `#` on a line is treated as a comment and is ignored by the shell.

1. 1
2. 2
3. 3
4. 4

1. `#!/bin/bash`

3. `# This is a comment`
4. `echo "Hello, world!"  # This is another comment`

Copied!

Comments are useful for documenting your code or configuration files, providing context, and explaining the purpose of the code to other developers who may read it. It's a best practice to include comments in your code or configuration files wherever necessary to make them more readable and maintainable.

### Semicolon `;`

The semicolon `;` metacharacter is used to separate multiple commands on a single command line. When multiple commands are separated by a semicolon, they are executed sequentially in the order they appear on the command line.

1. `$ echo "Hello, "; echo "world!"`
2. `Hello,`
3. `world!`

As you can see from the example above, the output of each `echo` command is printed on separate lines and follows the same sequence in which the commands were specified.

The semicolon metacharacter is useful when you need to run multiple commands sequentially on a single command line.

### Asterisk `*`

The asterisk `*` metacharacter is used as a wildcard character to represent any sequence of characters, including none.

1. `ls *.txt`

In this example, `*.txt` is a wildcard pattern that matches any file in the current directory with a `.txt` extension. The `ls` command lists the names of all matching files.

### Question mark `?`

The question mark `?` metacharacter is used as a wildcard character to represent any single character.

1. `ls file?.txt`

In this example, `file?.txt` is a wildcard pattern that matches any file in the current directory with a name starting with `file`, followed by any single character, and ending with the `.txt` extension.

## Quoting

**Quoting** is a mechanism that allows you to remove the special meaning of characters, spaces, or other metacharacters in a command argument or shell script. You use quoting when you want the shell to interpret characters literally.

|Symbol|Meaning|
|---|---|
|`\`|Escape metacharacter interpretation|
|`" "`|Interpret metacharacters within string|
|`' '`|Escape all metacharacters within string|

### Backslash `\`

The backslash character is used as an escape character. It instructs the shell to preserve the literal interpretation of special characters such as space, tab, and `$`. For example, if you have a file with spaces in its name, you can use backslashes followed by a space to handle those spaces literally:

1. `touch file\ with\ space.txt`

### Double quotes `" "`

When a string is enclosed in double quotes, most characters are interpreted literally, but metacharacters are interpreted according to their special meaning. For example, you can access variable values using the dollar `$` character:

1. `$ echo "Hello $USER"`
2. `Hello <username>`

### Single quotes `' '`

When a string is enclosed in single quotes, all characters and metacharacters enclosed within the quotes are interpreted literally. Single quotes alter the above example to produce the following output:

1. `$ echo 'Hello $USER'`
2. `Hello $USER`

Notice that instead of printing the value of `$USER`, single quotes cause the terminal to print the string `"$USER"`.

## Input/Output redirection

|Symbol|Meaning|
|---|---|
|`>`|Redirect output to file, overwrite|
|`>>`|Redirect output to file, append|
|`2>`|Redirect standard error to file, overwrite|
|`2>>`|Redirect standard error to file, append|
|`<`|Redirect file contents to standard input|

**Input/output (IO) redirection** is the process of directing the flow of data between a program and its input/output sources.

By default, a program reads input from _standard input_, the keyboard, and writes output to _standard output_, the terminal. However, using IO redirection, you can redirect a program's input or output to or from a file or another program.

### Redirect output `>`

This symbol is used to redirect the standard output of a command to a specified file.

> `ls > files.txt` will create a file called `files.txt` if it doesn't exist, and write the output of the `ls` command to it.

> Warning: When the file already exists, the output overwrites all of the file's contents!

### Redirect and append output `>>`

This notation is used to redirect and append the output of a command to the end of a file. For example,

> `ls >> files.txt` appends the output of the `ls` command to the end of file `files.txt`, and preserves any content that already existed in the file.

### Redirect standard output `2>`

This notation is used to redirect the standard error output of a command to a file. For example, if you run the ls command on a non-existing directory as follows,

> `ls non-existent-directory 2> error.txt` the shell will create a file called `error.txt` if it doesn't exist, and redirect the error output of the `ls` command to the file.

> Warning: When the file already exists, the error message overwrites all of the file's contents!

### Append standard error `2>>`

This symbol redirects the standard error output of a command and appends the error message to the end of a file without overwriting its contents.

> `ls non-existent-directory 2>> error.txt` will append the error output of the `ls` command to the end of the `error.txt` file.

### Redirect input `<`

This symbol is used to redirect the standard input of a command from a file or another command. For example,

> `sort < data.txt` will `sort` the contents of the `data.txt` file.

## Command Substitution

**Command substitution** allows you to run command and use its output as a component of another command's argument. Command substitution is denoted by enclosing a command in either backticks (**`command`**) or using the `$()` syntax. When the encapsulate command is executed, its output is substituted in place, and it can be used as an argument within another command. This is particularly useful for automating tasks that require the use of a command's output as input for another command.

For example, you could store the path to your current directory in a variable by applying command substitution on the `pwd` command, then move to another directory, and finally return to your original directory by invoking the `cd` command on the variable you stored, as follows:

1. `$ here=$(pwd)`
2. `$ cd path_to_some_other_directory`
3. `$ cd $here`
## Command Line Arguments

**Command line arguments** are additional inputs that can be passed to a program when the program is run from a command line interface. These arguments are specified after the name of the program, and they can be used to modify the behavior of the program, provide input data, or provide output locations. Command line arguments are used to pass arguments to a shell script.

For example, the following command provides two arguments, arg1, and arg2, that can be accessed from within your Bash script:

1. `$ ./MyBashScript.sh arg1 arg2`

## Conditionals

**Conditionals**, or `if` statements, are a way of telling a script to do something only under a specific condition.

Bash script conditionals use the following `if`-`then`-`else` syntax:

1. 1
2. 2
3. 3
4. 4
5. 5
6. 6

1. `if [ condition ]`
2. `then`
3.     `statement_block_1`  
4. `else`
5.     `statement_block_2`  
6. `fi`

Copied!

If the `condition` is `true`, then Bash executes the statements in `statement_block_1` before exiting the conditional block of code. After exiting, it will continue to run any commands after the closing `fi`.

Alternatively, if the `condition` is `false`, Bash instead runs the statements in `statement_block_2` under the `else` line, then exits the conditional block and continues to run commands after the closing `fi`.

> **Tips:**
> 
> - You must always put spaces around your condition within the square brackets `[` `]`.
> - Every `if` condition block must be paired with a `fi` to tell Bash where the condition block ends.
> - The `else` block is optional but recommended. If the condition evaluates to `false` without an `else` block, then nothing happens within the `if` condition block. Consider options such as echoing a comment in `statement_block_2` to indicate that the condition was evaluated as `false`.

In the following example, the condition is checking whether the number of command-line arguments read by some Bash script, `$#`, is equal to 2.

1. 1
2. 2
3. 3
4. 4
5. 5
6. 6

1. `if [[ $# == 2 ]]`
2. `then`
3.   `echo "number of arguments is equal to 2"`
4. `else`
5.   `echo "number of arguments is not equal to 2"`
6. `fi`

Copied!

Notice the use of the double square brackets, which is the syntax required for making integer comparisons in the condition `[[ $# == 2 ]]`.

You can also make string comparisons. For example, assume you have a variable called `string_var` that has the value `"Yes"` assigned to it. Then the following statement evaluates to `true`:

1. 1

1. `` `[ $string_var == "Yes" ]` ``

Copied!

Notice you only need single square brackets when making string comparisons.

You can also include multiple conditions to be satified by using the "and" operator `&&` or the "or" operator `||`. For example:

1. 1
2. 2
3. 3
4. 4
5. 5
6. 6

1. `if [ condition1 ] && [ condition2 ]`
2. `then`
3.     `echo "conditions 1 and 2 are both true"`
4. `else`
5.     `echo "one or both conditions are false"`
6. `fi`

Copied!

1. 1
2. 2
3. 3
4. 4
5. 5
6. 6

1. `if [ condition1 ] || [ condition2 ]`
2. `then`
3.     `echo "conditions 1 or 2 are true"`
4. `else`
5.     `echo "both conditions are false"`
6. `fi`

Copied!

## Logical operators

The following logical operators can be used to compare integers within a condition in an `if` condition block.

`==`: is equal to

If a variable `a` has a value of 2, the following condition evaluates to `true`; otherwise it evalutes to `false`.

1. 1

1. `$a == 2`

Copied!

`!=`: is not equal to

If a variable `a` has a value different from 2, the following statement evaluates to `true`. If its value is 2, then it evalutes to `false`.

1. 1

1. `a != 2`

Copied!

> **Tip**: The `!` logical negation operator changes `true` to `false` and `false` to `true`.

`<=`: is less than or equal to

If a variable `a` has a value of 2, then the following statement evaluates to `true`:

1. 1

1. `a <= 3`

Copied!

and the following statement evalutates to `false`:

1. 1

1. `a <= 1`

Copied!

Alternatively, you can use the equivalent notation `-le` in place of `<=`:

1. 1
2. 2
3. 3
4. 4
5. 5
6. 6
7. 7
8. 8

1. `a=1`
2. `b=2`
3. `if [ $a -le $b ]`
4. `then`
5.    `echo "a is less than or equal to b"`
6. `else`
7.    `echo "a is not less than or equal to b"`
8. `fi`

Copied!

We've only provided a small sampling of logical operators here. You can explore resources such as the [Advanced Bash-Scripting Guide](https://tldp.org/LDP/abs/html/comparison-ops.html) to find out more.

## Arithmetic calculations

You can perform integer addition, subtraction, multiplication, and division using the notation `$(())`.  
For example, the following two sets of commands both display the result of adding 3 and 2.

1. 1

1. `echo $((3+2))`

Copied!

or

1. 1
2. 2
3. 3
4. 4

1. `a=3`
2. `b=2`
3. `c=$(($a+$b))`
4. `echo $c`

Copied!

Bash natively handles integer arithmetic but does not handle floating-point arithmetic. As a result, it will always truncate the decimal portion of a calculation result.

For example:

1. 1

1. `echo $((3/2))`

Copied!

prints the truncated integer result, `1`, not the floating-point number, `1.5`.

The following table summarizes the basic arithmetic operators:

|Symbol|Operation|
|---|---|
|`+`|addition|
|`-`|subtraction|
|`*`|multiplication|
|`/`|division|

> Table: **Arithmetic operators**

## Arrays

The **array** is a Bash built-in data structure. An array is a space-delimited list contained in parentheses.ʊTo create an array, declare its name and contents:

1. 1

1. `my_array=(1 2 "three" "four" 5)`

Copied!

This statement creates and populates the array `my_array` with the items in the parentheses: `1`, `2`, `"three"`, `"four"`, and `5`.

You can also create an empty array by using:

1. 1

1. `declare -a empty_array`

Copied!

If you want to add items to your array after creating it, you can add to your array by appending one element at a time:

1. 1
2. 2

1. `my_array+=("six")`
2. `my_array+=(7)`

Copied!

This adds elements `"six"` and `7` to the array `my_array`.

By using indexing, you can access individual or multiple elements of an array:

1. 1
2. 2
3. 3
4. 4
5. 5
6. 6
7. 7
8. 8

1. `# print the first item of the array:`
2. `echo ${my_array[0]}`

4. `# print the third item of the array:`
5. `echo ${my_array[2]}`

7. `# print all array elements:`
8. `echo ${my_array[@]}`

Copied!

> **Tip:** Note that array indexing starts from 0, not from 1.

## `for` loops

You can use a construct called a `for` loop along with indexing to iterate over all elements of an array.

For example, the following `for` loops will continue to run over and over again until every element is printed:

1. 1
2. 2
3. 3

1. `for item in ${my_array[@]}; do`
2.   `echo $item`
3. `done`

Copied!

or

1. 1
2. 2
3. 3

1. `for i in ${!my_array[@]}; do`
2.   `echo ${my_array[$i]}`
3. `done`

Copied!

The `for` loop requires a `; do` component in order to cycle through the loop. Additionally, you need to terminate the `for` loop block with a `done` statement.

Another way to implement a `for` loop when you know how many iterations you want is as follows. For example, the following code prints the number 0 through 6.

1. 1
2. 2
3. 3
4. 4

1. `N=6`
2. `for (( i=0; i<=$N; i++ )) ; do`
3.   `echo $i`
4. `done`

Copied!

You can use `for` loops to accomplish all sorts of things. For example, you could count the number of items in an array or sum up its elements, as the following Bash script does:

1. `#!/usr/bin/env bash`
2. `# initialize array, count, and sum`
3. `my_array=(1 2 3)`
4. `count=0`
5. `sum=0`
6. `for i in ${!my_array[@]}; do`
7.   `# print the ith array element`
8.   `echo ${my_array[$i]}`
9.   `# increment the count by one`
10.   `count=$(($count+1))`
11.   `# add the current value of the array to the sum`
12.   `sum=$(($sum+${my_array[$i]}))`
13. `done`
14. `echo $count`
15. `echo $sum`

# Cheat Sheet - Introduction to Shell Scripting

### Bash shebang
---

1. 1

1. `#!/bin/bash`

Copied!

### Get the path to a command
---

1. 1

1. `which bash`

Copied!

### Pipes, filters, and chaining
---

##### Chain filter commands together using the pipe operator:

1. 1

1. `ls | sort -r`

Copied!

##### Pipe the output of manual page for `ls` to `head` to display the first 20 lines:

1. 1

1. `man ls | head -20`

Copied!

##### Use a pipeline to extract a column of names from a csv and drop duplicate names:

1. 1

1. `cut -d "," -f1 names.csv | sort | uniq`

Copied!

### Working with shell and environment variables:
---

##### List all shell variables:

1. 1

1. `set`

Copied!

##### Define a shell variable called `my_planet` and assign value `Earth` to it:

1. 1

1. `my_planet=Earth`

Copied!

##### Display value of a shell variable:

1. 1

1. `echo $my_planet`

Copied!

##### Reading user input into a shell variable at the command line:

1. 1

1. `read first_name`

Copied!

> **Tip:** Whatever text string you enter after running this command gets stored as the value of the variable `first_name`.

##### List all environment variables:

1. 1

1. `env`

Copied!

##### Environment vars: define/extend variable scope to child processes:

1. 1
2. 2

1. `export my_planet`
2. `export my_galaxy='Milky Way'`

Copied!

### Metacharacters
---

##### Comments `#`:

1. 1

1. `# The shell will not respond to this message`

Copied!

##### Command separator `;`:

1. 1

1. `echo 'here are some files and folders'; ls`

Copied!

##### File name expansion wildcard `*`:

1. 1

1. `ls *.json`

Copied!

##### Single character wildcard `?`:

1. 1

1. `ls file_2021-06-??.json`

Copied!

### Quoting
---

##### Single quotes `''` - interpret literally:

1. 1

1. `echo 'My home directory can be accessed by entering: echo $HOME'`

Copied!

##### Double quotes `""` - interpret literally, but evaluate metacharacters:

1. 1

1. `echo "My home directory is $HOME"`

Copied!

##### Backslash `\` - escape metacharacter interpretation:

1. 1

1. `echo "This dollar sign should render: \$"`

Copied!

### I/O Redirection
---

##### Redirect output to file and overwrite any existing content:

1. 1

1. `echo 'Write this text to file x' > x`

Copied!

##### Append output to file:

1. 1

1. `echo 'Add this line to file x' >> x`

Copied!

##### Redirect standard error to file:

1. 1

1. `bad_command_1 2> error.log`

Copied!

##### Append standard error to file:

1. 1

1. `bad_command_2 2>> error.log`

Copied!

##### Redirect file contents to standard input:

1. 1

1. `$ tr “[a-z]” “[A-Z]” < a_text_file.txt`

Copied!

##### The input redirection above is equivalent to:

1. 1

1. `$cat a_text_file.txt | tr “[a-z]” “[A-Z]”`

Copied!

### Command Substitution
---

##### Capture output of a command and echo its value:

1. 1
2. 2

1. `THE_PRESENT=$(date)`
2. `echo "There is no time like $THE_PRESENT"`

Copied!

##### Capture output of a command and echo its value:

1. 1

1. `echo "There is no time like $(date)"`

Copied!

### Command line arguments
---

1. 1

1. `./My_Bash_Script.sh arg1 arg2 arg3`

Copied!

### Batch vs. concurrent modes
---

##### Run commands sequentially:

1. 1

1. `start=$(date); ./MyBigScript.sh ; end=$(date)`

Copied!

##### Run commands in parallel:

1. 1

1. `./ETL_chunk_one_on_these_nodes.sh  & ./ETL_chunk_two_on_those_nodes.sh`

Copied!

### Scheduling jobs with cron
---

##### Open crontab editor:

1. 1

1. `crontab -e`

Copied!

##### Job scheduling syntax:

1. 1

1. `m  h  dom  mon  dow   command`

Copied!

> (minute, hour, day of month, month, day of week)

> **Tip:** You can use the `*` wildcard to mean "any".

##### Append the date/time to a file every Sunday at 6:15 pm:

1. 1

1. `15 18 * * 0 date >> sundays.txt`

Copied!

##### Run a shell script on the first minute of the first day of each month:

1. 1

1. `1  0 1 * * ./My_Shell_Script.sh`

Copied!

##### Back up your home directory every Monday at 3:00 am:

1. 1

1. `0 3 * * 1  tar -cvf my_backup_path\my_archive.tar.gz $HOME\`

Copied!

##### Deploy your cron job:

> Close the crontab editor and save the file.

##### List all cron jobs:

1. 1

1. `crontab -l`

Copied!

### Conditionals

##### `if`-`then`-`else` syntax:

1. 1
2. 2
3. 3
4. 4
5. 5
6. 6

1. `if [[ $# == 2 ]]`
2. `then`
3.   `echo "number of arguments is equal to 2"`
4. `else`
5.   `echo "number of arguments is not equal to 2"`
6. `fi`

Copied!

##### 'and' operator `&&`:

1. 1

1. `if [ condition1 ] && [ condition2 ]`

Copied!

##### 'or' operator `||`:

1. 1

1. `if [ condition1 ] || [ condition2 ]`

Copied!

### Logical operators

|Operator|Definition|
|---|---|
|`==`|is equal to|
|`!=`|is not equal to|
|`<`|is less than|
|`>`|is greater than|
|`<=`|is less than or equal to|
|`>=`|is greater than or equal to|

### Arithmetic calculations

##### Integer arithmetic notation:

1. 1

1. `$(())`

Copied!

##### Basic arithmetic operators:

|Symbol|Operation|
|---|---|
|`+`|addition|
|`-`|subtraction|
|`*`|multiplication|
|`/`|division|

##### Display the result of adding 3 and 2:

1. 1

1. `echo $((3+2))`

Copied!

##### Negate a number:

1. 1

1. `echo $((-1*-2))`

Copied!

### Arrays

##### Declare an array that contains items `1`, `2`, `"three"`, `"four"`, and `5`:

1. 1

1. `my_array=(1 2 "three" "four" 5)`

Copied!

##### Add an item to your array:

1. 1
2. 2

1. `my_array+="six"`
2. `my_array+=7`

Copied!

##### Declare an array and load it with lines of text from a file:

1. 1

1. `my_array=($(echo $(cat column.txt)))`

Copied!

### `for` loops

##### Use a `for` loop to iterate over values from 1 to 5:

1. 1
2. 2
3. 3

1. `for i in {0..5}; do`
2.     `echo "this is iteration number $i"`
3. `done`

Copied!

##### Use a `for` loop to print all items in an array:

1. 1
2. 2
3. 3

1. `for item in ${my_array[@]}; do`
2.   `echo $item`
3. `done`

Copied!

##### Use array indexing within a `for` loop, assuming the array has seven elements:

1. 1
2. 2
3. 3

1. `for i in {0..6}; do`
2.     `echo ${my_array[$i]}`
3. `done`

# Summary - Week 3

- A shell script is a program that begins with a ‘shebang’ directive and is used to run commands and programs. Scripting languages are interpreted rather than compiled.
- Filters are shell commands. The pipe operator `|` allows you to chain filter commands. 
- Shell variables can be assigned values with `=` and listed using `set.` Environment variables are shell variables with extended scope, and you can list them with `env.`
- Metacharacters are special characters that have meaning to the shell.
- Quoting specifies whether the shell should interpret special characters as metacharacters or 'escape' them.
- Input/Output, or I/O redirection, refers to a set of features used for redirecting.
- You can use command substitution to replace a command with its output.
- Command line arguments provide a way to pass arguments to a shell script.
- In concurrent mode, multiple commands can run simultaneously.
- You can schedule cron jobs to run periodically at selected times. `m h dom mon dow command` is the cron job syntax.
- You can edit cron jobs by running `crontab -e,` and `crontab -l` lists all cron jobs in the cron table.

