	Topic: Reverse Engineering
	Name: A Christmas DOScovery: Tapes of Yule-tide Past

# DOS Cheat Sheet  

If you are familiar with the command prompt in Windows, DOS shouldn't be too much of a problem for you because their syntax and commands are the same. However, some utilities are only present on Windows and aren't available on DOS, so we have created a DOS cheat sheet below to help you in this task.

# Common DOS commands and Utilities:

| Commands  | Description  |
|---|---|
|CD|Change Directory|
|DIR|Lists all files and directories in the current directory|
|TYPE|Displays the contents of a text file|
|CLS|Clears the screen|
|HELP|Provides help information for DOS commands|
|EDIT|The MS-DOS Editor|

# File Signature/Magic Bytes

File signatures, commonly referred to as "magic bytes", are specific byte sequences at the beginning of a file that identify or verify its content type and format. These bytes often have corresponding ASCII characters, allowing for easier human readability when inspected. The identification process helps software applications quickly determine whether a file is in a format they can handle, aiding operational functionality and security measures.

In cyber security, file signatures are crucial for identifying file types and formats. You'll encounter them in malware analysis, incident response, network traffic inspection, web security checks, and forensics. Knowing how to work with these magic bytes can help you quickly identify malicious or suspicious activity and choose the right tools for deeper analysis.

Here is a list of some of the most common files and their magic:

|File Format|Magic Bytes|ASCII representation|
|---|---|:-:|
|PNG image file|89 50 4E 47 0D 0A 1A 0A|%PNG|
|GIF image file|47 49 46 38|GIF8|
|Windows and DOS executables|4D 5A|MZ|
|Linux ELF executables|7F 45 4C 46|.ELF|
|MP3 audio file|49 44 33|ID3|
