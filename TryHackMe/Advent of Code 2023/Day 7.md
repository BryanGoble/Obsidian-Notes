	Topic: Log Analysis
	Name: 'Tis the season for log chopping!

# Log Primer

Before analyzing a dataset of proxy logs, let's first revisit what log files are.

A log file is like a digital trail of what's happening behind the scenes in a computer or software application. It records important events, actions, errors, or information as they happen. It helps diagnose problems, monitor performance, and record what a program or application is doing. For clarity, let's look at a quick example.

```session-shell
158.32.51.188 - - [25/Oct/2023:09:11:14 +0000] "GET /robots.txt HTTP/1.1" 200 11173 "-" "curl/7.68.0"
```

The example above is an entry from an Apache web server log. We can interpret it easily by breaking down each value into its corresponding purpose.

|   |   |   |
|---|---|---|
|**Field**|**Value**|**Description**|
|**Source IP Address**|158.32.51.188|The source (computer) that initiated the HTTP request.|
|**Timestamp**|[25/Oct/2023:09:11:14 +0000]|The date and time when the event occurred.|
|**HTTP Request**|GET /robots.txt HTTP/1.1|The actual HTTP request made, including the request method, URI path, and HTTP version.|
|**Status Code**|200|The response of the web application.|
|**User Agent**|curl/7.68.0|The user agent used by the source of the request. It is typically tied up to the application used to invoke the HTTP request.|

Being able to interpret a log entry allows you to contextualize the events, whether for debugging purposes or for hunting potential threat activity.

# What Is a Proxy Server

Since the data to be analyzed is a proxy log, we must understand a proxy server.

A proxy server is an intermediary between your computer or device and the internet. When you request information or access a web page, your device connects to the proxy server instead of connecting directly to the target server. The proxy server then forwards your request to the internet, receives the response, and sends it back to your device. To visualize this, refer to the diagram below.

![Comparison of connection flow, with or without a proxy server.](https://tryhackme-images.s3.amazonaws.com/user-uploads/5dbea226085ab6182a2ee0f7/room-content/da0a30d91c289c95f741feaa308d2a45.svg)  

A proxy server offers enhanced visibility into network traffic and user activities, since it logs all web requests and responses. This enables system administrators and security analysts to monitor which websites users access, when, and how much bandwidth is used. It also allows administrators to enforce policies and block specific websites or content categories.

# Common examples of malicious activities:

|**Attack Technique**|**Potential Indicator**|
|---|---|
|**Download attempt of a malicious binary**|Connection to a known malicious URL binary<br><br>(e.g. www[.]evil[.]com/malicious[.]exe)|
|**Data exfiltration**|High count of outbound bandwidth due to file upload<br><br>(e.g. outbound connection to OneDrive)|
|**Continuous C2 connection**|High count of outbound connections to a single domain in regular intervals<br><br>(e.g. connections every five minutes to a single domain)|

# Linux Commands

1. **cat:** Short for con**cat**enate, allows you to combine and display the contents of multiple files. This command on a single file will enable you to display its contents. You can try this command by following the one below. 

```shell-session
ubuntu@tryhackme:~/Desktop/artefacts$ cat access.log
[2023/10/25:15:42:02] 10.10.120.75 sway.com:443 CONNECT - 200 0 "-"
[2023/10/25:15:42:02] 10.10.120.75 sway.com:443 GET / 301 492 "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 Safari/537.36"
--- REDACTED FOR BREVITY ---
```

   You might have been overwhelmed by the contents of the proxy log. This is because the **cat** command dumps all the contents and only stops once the end of the file has been rendered. But don't worry; we'll learn more tricks to optimize the output of our commands in the following sections.
    
2. **less:** The less command allows you to view the contents of a file one page at a time. Compared to the cat command, this allows you to easily review the contents without being overwhelmed by the large quantity of the log file.

```shell-session
ubuntu@tryhackme:~/Desktop/artefacts$ less access.log
```

  After opening the file using **less**, press your `Up/Down` button to move one line at a time and `Page Up (b)/Page Down (space)` buttons to move one page at a time. Then, you can exit the view by pressing the `q` button.
   
3. **head:** The head command lets you view the contents at the top of the file. Try executing `head access.log` to view the first 10 entries of the log. To specify the number of lines to be displayed, use the `-n` option together with the count of lines, similar to the command below.

```shell-session
ubuntu@tryhackme:~/Desktop/artefacts$ head -n 1 access.log
[2023/10/25:15:42:02] 10.10.120.75 sway.com:443 CONNECT - 200 0 "-"
```
   
1. **tail:** In contrast to the head command, the tail command allows you to view the end of the file easily. To display the last 10 entries of the log, execute `tail access.log` on the terminal. Like the head command, you can specify the number of lines displayed using the `-n` option (as shown in the command below).

```shell-session
ubuntu@tryhackme:~/Desktop/artefacts$ tail -n 1 access.log
[2023/10/25:16:17:14] 10.10.140.96 storage.live.com:443 GET / 400 630 "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 Safari/537.36"
```
 
5. **wc:** The wc command stands for **word count**. It's a command-line tool that counts the number of lines, words, and characters in a text file. Try executing `wc access.log`. By default, it prints the count of **lines, words**, and **characters** as shown in your terminal.

```shell-session
ubuntu@tryhackme:~/Desktop/artefacts$ wc -l access.log
49081 access.log
```

   You can probably tell why we got overwhelmed by the cat command. The line count of access.log is 49081!
   
6. **nl:** The nl command stands for **number lines**. It renders the contents of the file in a numbered line format.

```shell-session
ubuntu@tryhackme:~/Desktop/artefacts$ nl access.log
	 1	[2023/10/25:15:42:02] 10.10.120.75 sway.com:443 CONNECT - 200 0 "-"
	 2	[2023/10/25:15:42:02] 10.10.120.75 sway.com:443 GET / 301 492 "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.0.0 Safari/537.36"
	 3	[2023/10/25:15:42:02] 10.10.120.75 sway.office.com:443 CONNECT - 200 0 "-"
--- REDACTED FOR BREVITY ---
```
   
   This command is very helpful if used before the head or tail command since the line number can be used as a reference in trimming the output. Knowing the line number of the log entry allows you to easily manage the values rendered as output.