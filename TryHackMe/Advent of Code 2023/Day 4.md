	Topic: Brute-forcing
	Name: Baby, it's CeWLd outside

# Overview

CeWL (pronounced "cool") is a custom word list generator tool that spiders websites to create word lists based on the site's content. Spidering, in the context of web security and penetration testing, refers to the process of automatically navigating and cataloguing a website's content, often to retrieve the site structure, content, and other relevant details. This capability makes CeWL especially valuable to penetration testers aiming to brute-force login pages or uncover hidden directories using organisation-specific terminology.

Beyond simple wordlist generation, CeWL can also compile a list of email addresses or usernames identified in team members' page links. Such data can then serve as potential usernames in brute-force operations.

# How to use CeWL?

In the terminal, type `cewl -h` to see a list of all the options it accepts, complete with their descriptions.

```shell-session
$ cewl -h
CeWL 6.1 (Max Length) Robin Wood (robin@digi.ninja) (https://digi.ninja/)
Usage: cewl [OPTIONS] ... 

    OPTIONS:
	-h, --help: Show help.
	-k, --keep: Keep the downloaded file.
	-d ,--depth : Depth to spider to, default 2.
	-m, --min_word_length: Minimum word length, default 3.
	-x, --max_word_length: Maximum word length, default unset.
	-o, --offsite: Let the spider visit other sites.
	--exclude: A file containing a list of paths to exclude
	--allowed: A regex pattern that path must match to be followed
	-w, --write: Write the output to the file.
	-u, --ua : User agent to send.
	-n, --no-words: Don't output the wordlist.
	-g , --groups : Return groups of words as well
	--lowercase: Lowercase all parsed words
	--with-numbers: Accept words with numbers in as well as just letters
	--convert-umlauts: Convert common ISO-8859-1 (Latin-1) umlauts (ä-ae, ö-oe, ü-ue, ß-ss)
	-a, --meta: include meta data.
	--meta_file file: Output file for meta data.
	-e, --email: Include email addresses.
	--email_file : Output file for email addresses.
	--meta-temp-dir : The temporary directory used by exiftool when parsing files, default /tmp.
	-c, --count: Show the count for each word found.
	-v, --verbose: Verbose.
	--debug: Extra debug information.
[--snip--]
```

This will provide a full list of options to further customise your wordlist generation process. If CeWL is not installed in your VM, you may install it by using the command `sudo apt-get install cewl -y`

To generate a basic wordlist from a website, use the following command:

```shell-session
user@tryhackme$ cewl http://10.10.157.22                                     
CeWL 6.1 (Max Length) Robin Wood (robin@digi.ninja) (https://digi.ninja/)
Start
End
and
the
AntarctiCrafts
[--snip--]
```

To save the wordlist generated to a file, you can use the command below:

```shell-session
user@tryhackme$ cewl http://10.10.157.22 -w output.txt
user@tryhackme$ ls
output.txt
```

# Why CeWL?

CeWL is a wordlist generator that is unique compared to other tools available. While many tools rely on pre-defined lists or common dictionary attacks, CeWL creates custom wordlists based on web page content. Here's why CeWL stands out:

1. **Target-specific wordlists:** CeWL crafts wordlists specifically from the content of a targeted website. This means that the generated list is inherently tailored to the vocabulary and terminology used on that site. Such custom lists can increase the efficiency of brute-forcing tasks.
2. **Depth of search:** CeWL can spider a website to a specified depth, thereby extracting words from not just one page but also from linked pages up to the set depth.
3. **Customisable outputs:** CeWL provides various options to fine-tune the wordlist, such as setting a minimum word length, removing numbers, and including meta tags. This level of customisation can be advantageous for targeting specific types of credentials or vulnerabilities.
4. **Built-in features:** While its primary purpose is wordlist generation, CeWL includes functionalities such as username enumeration from author meta tags and email extraction.
5. **Efficiency:** Given its customisability, CeWL can often generate shorter but more relevant word lists than generic ones, making password attacks quicker and more precise.
6. **Integration with other tools:** Being command-line based, CeWL can be integrated seamlessly into automated workflows, and its outputs can be directly fed into other cyber security tools.
7. **Actively maintained:** CeWL is actively maintained and updated. This means it stays relevant and compatible with contemporary security needs and challenges.

In conclusion, while there are many wordlist generators out there, CeWL offers a distinct approach by crafting lists based on a target's own content. This can often provide a strategic edge in penetration testing scenarios.

# How To Customise the Output for Specific Tasks

CeWL provides a lot of options that allow you to tailor the wordlist to your needs:

1. **Specify spidering depth:** The `-d` option allows you to set how deep CeWL should spider. For example, to spider two links deep: `cewl http://10.10.157.22 -d 2 -w output1.txt`
2. **Set minimum and maximum word length:** Use the `-m` and `-x` options respectively. For instance, to get words between 5 and 10 characters: `cewl http://10.10.157.22 -m 5 -x 10 -w output2.txt`
3. **Handle authentication:** If the target site is behind a login, you can use the `-a` flag for form-based authentication.
4. **Custom extensions:** The `--with-numbers` option will append numbers to words, and using `--extension` allows you to append custom extensions to each word, making it useful for directory or file brute-forcing.
5. **Follow external links:** By default, CeWL doesn't spider external sites, but using the `--offsite` option allows you to do so.