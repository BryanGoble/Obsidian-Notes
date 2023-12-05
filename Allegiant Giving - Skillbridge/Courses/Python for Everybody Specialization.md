---
tags:
  - Python
  - DataStructures
  - Networks
  - BeautifulSoup
  - JSON
  - API
  - SQL
  - CRUD
  - XML
  - OOP
---
# Courses
1. [Python for Everybody Specialization](https://www.coursera.org/specializations/python)
	1. [Programming For Everybody (Getting Started With Python)](https://www.coursera.org/learn/python/)
	2. [Python Data Structures](https://www.coursera.org/learn/python-data/)
	3. [Using Python to Access Web Data](https://www.coursera.org/learn/python-network-data)
	4. [Using Databases with Python](https://www.coursera.org/learn/python-databases)
## 2.1 - Expressions
In simple terms, a Python expression is like a small piece of code that produces a value or result. It's a combination of variables, operators, and functions that you can use to perform calculations or manipulate data. When you write and run an expression in Python, it typically returns a single value.

For example, here are some basic Python expressions:

1. **Mathematical Expression**: 
   ```python
   result = 3 + 4
   ```
   In this expression, `3 + 4` is a mathematical operation, and it produces the value `7`, which is assigned to the variable `result`.

2. **String Concatenation Expression**:
   ```python
   greeting = "Hello, " + "world!"
   ```
   Here, `"Hello, " + "world!"` is an expression that combines two strings to create a new string, and `greeting` stores the result, which is `"Hello, world!"`.

3. **Function Call Expression**:
   ```python
   length = len("Python")
   ```
   The `len()` function is called with the argument `"Python"`, and it returns the length of the string, which is `6`. This result is stored in the variable `length`.

In summary, Python expressions are building blocks of code that perform operations and produce values. They can be as simple as basic math or as complex as calling functions and manipulating data, but at their core, they're all about generating results.
## 3.1 - Conditional Statements
Python conditional statements are used to make decisions in your code. They allow your program to execute different blocks of code depending on whether certain conditions are met. Here's a simple explanation:

1. **if statement**: It starts with the keyword `if` followed by a condition (a test that evaluates to either True or False). If the condition is True, the code inside the `if` block is executed.

   ```python
   if condition:
       # Code to execute if the condition is True
   ```

2. **else statement**: If you want to provide an alternative code block to execute when the condition in the `if` statement is False, you can use an `else` statement.

   ```python
   if condition:
       # Code to execute if the condition is True
   else:
       # Code to execute if the condition is False
   ```

3. **elif statement** (short for "else if"): When you have multiple conditions to check in sequence, you can use `elif` statements. The first condition that evaluates to True will execute its associated code block, and the rest will be skipped.

   ```python
   if condition1:
       # Code to execute if condition1 is True
   elif condition2:
       # Code to execute if condition1 is False and condition2 is True
   elif condition3:
       # Code to execute if condition1 and condition2 are False, and condition3 is True
   else:
       # Code to execute if all conditions are False
   ```

These conditional statements allow you to control the flow of your program based on different situations, making your code more flexible and responsive.

1. **Try Block**: The code that you suspect might raise an error is placed inside a `try` block. Python will attempt to execute this code.

   ```python
   try:
       # Code that might raise an error
   ```

2. **Except Block**: If an error occurs inside the `try` block, instead of crashing your program, Python will jump to the `except` block. This block contains code to handle the error in a controlled manner.

   ```python
   except SomeErrorType:
       # Code to handle the error
       quit() # Prevents Traceback errors
   ```

In this structure:

- You specify the type of error you want to handle (e.g., `SomeErrorType`), or you can use a more general `except` without specifying an error type to catch any exception.
- If the error of the specified type occurs in the `try` block, Python will execute the code inside the corresponding `except` block.

Using try/except blocks helps prevent your program from crashing due to unexpected errors, making your code more robust and user-friendly.
## 6.1 - Strings
In simple terms, a string in Python 3 is a sequence of characters, like letters, numbers, symbols, or spaces, enclosed within either single (' '), double (" "), or triple (''' ''' or """ """) quotation marks. Strings are used to represent and manipulate textual data.

Here's an example:

```Python
my_string = "Hello, Python 3!"

print(my_string) #Hello, Python 3!
```
### String Concatenation
In Python 3, string concatenation is a way of combining or joining two or more strings together to create a single longer string. You can think of it as "string addition." To concatenate strings in Python 3, you can use the `+` operator. When you use the `+` operator between two strings, it combines them into one, placing the second string right after the first. 

Here's an example:

```python
first_name = "John"
last_name = "Doe"
full_name = first_name + " " + last_name
```
### String Comparison
In Python 3, string comparison is the process of determining whether one string is equal to, greater than, or less than another string. Here's a simple explanation:

1. **Equality Comparison (`==`)**: You can use the `==` operator to check if two strings have the same contents. If they do, the comparison returns `True`, indicating that the strings are equal; otherwise, it returns `False`.

   Example:
   ```python
   string1 = "apple"
   string2 = "apple"
   
   if string1 == string2:
       print("Both strings are equal")
   ```

2. **Inequality Comparison (`!=`)**: The `!=` operator checks if two strings are not equal. If they are not the same, it returns `True`; otherwise, it returns `False`.

   Example:
   ```python
   string1 = "apple"
   string2 = "banana"
   
   if string1 != string2:
       print("The strings are not equal")
   ```

3. **Greater Than (`>`) and Less Than (`<`) Comparison**: Strings can also be compared based on their lexicographic (dictionary) order. When using `>` (greater than), it checks if the first string comes after the second string in dictionary order. When using `<` (less than), it checks if the first string comes before the second string.

   Example:
   ```python
   string1 = "apple"
   string2 = "banana"
   
   if string1 < string2:
       print("string1 comes before string2")
   ```

These string comparison operators allow you to make decisions in your code based on the relationships between strings, such as checking if they match exactly or determining their order in a sorted list.
### String Library
In Python 3, the string library provides a collection of functions and methods that allow you to work with text (strings) in various ways. Here's a simple explanation of some common string functions and methods:

1. **len()**: This function returns the length (the number of characters) of a string.

   ```python
   text = "Hello, World!"
   length = len(text)  # length will be 13
   ```

2. **str()**: You can use the `str()` function to convert other data types into strings.

   ```python
   number = 42
   text = str(number)  # text will be "42"
   ```

3. **.upper()** and **.lower()**: These methods convert a string to all uppercase or all lowercase letters, respectively.

   ```python
   text = "Hello, World!"
   upper_text = text.upper()  # upper_text will be "HELLO, WORLD!"
   lower_text = text.lower()  # lower_text will be "hello, world!"
   ```

4. **.strip()**: This method removes leading and trailing whitespace (spaces, tabs, and newline characters) from a string.

   ```python
   text = "   Some Text   "
   clean_text = text.strip()  # clean_text will be "Some Text"
   ```

5. **.split()**: You can use this method to split a string into a list of substrings based on a specified delimiter (usually a space by default).

   ```python
   text = "Apple Banana Cherry"
   words = text.split()  # words will be ["Apple", "Banana", "Cherry"]
   ```

6. **.join()**: This method is used to join a list of strings into a single string, using the original string as a delimiter.

   ```python
   words = ["Apple", "Banana", "Cherry"]
   text = ", ".join(words)  # text will be "Apple, Banana, Cherry"
   ```

7. **.find()**: It searches for a substring within a string and returns the index of the first occurrence (or -1 if not found).

   ```python
   text = "Hello, World!"
   index = text.find("World")  # index will be 7
   ```

8. **.replace()**: This method replaces all occurrences of a specified substring with another substring.

   ```python
   text = "Hello, World!"
   new_text = text.replace("World", "Python")  # new_text will be "Hello, Python!"
   ```

These are just a few examples of the many functions and methods available in the Python string library. They are useful for manipulating and working with text data in your Python programs.

1. **`dir()` function**: The `dir()` function in Python is used to get a list of all the attributes (functions and variables) that are associated with a particular object, such as a string. When you call `dir()` on a string, it shows you a list of all the things you can do with that string.

   For example:
   ```python
   my_string = "Hello, World!"
   print(dir(my_string))
   ```

   This will display a list of methods and properties you can use with the `my_string` object, like `upper()`, `lower()`, and `replace()`, among others.

2. **`type()` function**: The `type()` function in Python is used to determine the data type or class of an object. When you call `type()` on an object, it tells you what kind of data that object represents.

   For example:
   ```python
   my_string = "Hello, World!"
   print(type(my_string))
   ```

   This will tell you that `my_string` is of type `str`, which means it's a string.

In summary, `dir()` helps you discover what you can do with an object by listing its attributes, and `type()` tells you what kind of data or object you're working with.
## 7.1 - Files
Python 3 file handling is the way Python allows you to work with files, which can be used to read data from files, write data to files, or perform various operations on files. Here's a simple explanation:

1. **Opening a File**: To work with a file, you first need to open it using the `open()` function. You specify the file's name and the mode (read, write, or append) in which you want to open the file. For example:

   ```python
   file = open("example.txt", "r")  # Opens "example.txt" in read mode
   ```

2. **Reading from a File**: If you open a file in read mode (`"r"`), you can read its contents using methods like `read()`, `readline()`, or `readlines()`. For instance:

   ```python
   content = file.read()  # Reads the entire file into a string
   ```

3. **Writing to a File**: If you open a file in write mode (`"w"`), you can write data to it using methods like `write()`. Be careful, as this mode overwrites the existing content:

   ```python
   file.write("Hello, World!")  # Writes the text to the file
   ```

4. **Appending to a File**: If you open a file in append mode (`"a"`), you can add data to the end of the file without overwriting its existing content:

   ```python
   file = open("example.txt", "a")
   file.write("This is a new line.")
   ```

5. **Closing a File**: After you're done with a file, it's important to close it using the `close()` method to free up system resources:

   ```python
   file.close()
   ```

6. **With Statement**: A better practice is to use a `with` statement, also known as a context manager. It automatically closes the file when you're done with it:

   ```python
   with open("example.txt", "r") as file:
       content = file.read()
   # File is automatically closed here
   ```

Python's file handling allows you to read data from files, write data to files, and manipulate file content, making it a useful tool for tasks like reading configuration files, processing data, and saving information. Remember to handle exceptions and close files properly to ensure your code is robust and efficient.
## 8.1 - Lists
In simple terms, a Python 3 list is like a container or a box that can hold multiple items. These items can be of any data type, such as numbers, text, or even other lists. Here's a straightforward explanation:

1. **Collection of Items**: A Python list is a collection that allows you to store and organize multiple items, like numbers, words, or other pieces of data.

2. **Ordered**: Lists maintain the order of the items you put in them. The first item you add will be at the beginning, the second item will be next, and so on. This order is preserved unless you change it.

3. **Mutable**: Lists can be changed after they are created. You can add, remove, or modify items in a list as needed.

4. **Access by Index**: You can access individual items in a list by using their position, called an index. Python uses zero-based indexing, so the first item is at index 0, the second at index 1, and so on.

Here's an example of creating and working with a simple list in Python:

```python
my_list = [1, 2, 3, 4, 5]  # Creating a list of numbers

print(my_list[0])  # Accessing the first item (prints 1)
print(my_list[2])  # Accessing the third item (prints 3)

my_list.append(6)  # Adding an item to the end of the list
print(my_list)     # Prints [1, 2, 3, 4, 5, 6]

my_list.remove(3)  # Removing an item by value
print(my_list)     # Prints [1, 2, 4, 5, 6]
```

In this example, `my_list` is a Python list containing numbers. You can access items using their index, add items with `append()`, and remove items with `remove()`. Lists are a fundamental data structure in Python, widely used for storing and managing collections of data.
### Manipulating Lists
In simple terms, Python 3 list manipulations refer to the various operations you can perform on lists, which are a fundamental data structure in Python for storing collections of items. Here are some common list manipulations explained:

1. **Creating a List**: You can create a list by enclosing items in square brackets `[]` and separating them with commas.

   ```python
   my_list = [1, 2, 3, 4, 5]
   ```

2. **Accessing Elements**: You can access individual elements in a list using their index, which starts at 0 for the first element.

   ```python
   first_item = my_list[0]  # Access the first element (1)
   ```

3. **Modifying Elements**: You can change the value of an element in a list by assigning a new value to its index.

   ```python
   my_list[2] = 99  # Change the third element to 99
   ```

4. **Appending Elements**: You can add new elements to the end of a list using the `append()` method.

   ```python
   my_list.append(6)  # Add 6 to the end of the list
   ```

5. **Removing Elements**: You can remove elements from a list by their value using the `remove()` method, or by their index using the `pop()` method.

   ```python
   my_list.remove(3)  # Remove the element with the value 3
   popped_element = my_list.pop(1)  # Remove and return the second element
   ```

6. **Slicing Lists**: You can create a new list by extracting a portion of an existing list using slicing.

   ```python
   sublist = my_list[1:4]  # Get a new list containing elements at index 1, 2, and 3
   ```

7. **Concatenating Lists**: You can combine two or more lists into a single list using the `+` operator.

   ```python
   combined_list = my_list + [7, 8, 9]
   ```

8. **Finding the Length**: You can find the number of elements in a list using the `len()` function.

   ```python
   length = len(my_list)  # Get the number of elements in the list
   ```

9. **Checking if an Element is in a List**: You can use the `in` keyword to check if a specific element exists in a list.

   ```python
   is_present = 5 in my_list  # Check if 5 is in the list
   ```

These are some of the basic list manipulations in Python. Lists are versatile and widely used for storing and working with collections of data in Python programs.
## 9.1 - Dictionaries
In simple terms, a Python 3 dictionary is like a real-world dictionary, but instead of words and their definitions, it stores pairs of keys and values. Here's a straightforward explanation:

- **Keys**: Think of keys as the words in a dictionary. They are unique and used to look up associated values.

- **Values**: Values are like the definitions in a dictionary. They are associated with keys and can be any data type, such as numbers, strings, lists, or even other dictionaries.

A dictionary is enclosed in curly braces `{}` and consists of key-value pairs separated by colons. Here's an example:

```python
my_dict = {
    "apple": 2,
    "banana": 3,
    "cherry": 5
}
```

In this dictionary:

- "apple," "banana," and "cherry" are keys.
- 2, 3, and 5 are their corresponding values.

You can access the values by using the keys. For example:

```python
print(my_dict["banana"])  # This will print 3
```

Dictionaries are flexible and allow you to store and retrieve data efficiently. They are commonly used for tasks like looking up information based on a key or organizing data in a structured way.
### Counting with Dictionaries
In Python 3, counting with dictionaries is a way to keep track of how many times different items or elements appear in a collection, like a list, by using a dictionary data structure. Here's a simple explanation:

1. **Dictionary**: A dictionary in Python is a collection that stores data in key-value pairs. Each key is unique, and it is associated with a specific value.

2. **Counting Elements**: To count elements, you can use the elements as keys in the dictionary and use the corresponding values to keep track of how many times each element appears.

Here's how it works in simple terms:

```python
# Create an empty dictionary to count elements
element_count = {}

# Suppose you have a list of elements
elements = [1, 2, 2, 3, 3, 3, 4, 4, 4, 4]

# Count the elements and store the counts in the dictionary
for element in elements:
    if element in element_count:
        element_count[element] += 1  # Increment the count for the existing element
    else:
        element_count[element] = 1   # Initialize the count for a new element

# Now, element_count will contain the counts of each element
print(element_count)
```

In this example, we have a list of elements, and we use a dictionary called `element_count` to count how many times each element appears in the list. The keys in the dictionary are the elements themselves, and the values are the counts.

So, after running this code, `element_count` would look something like this:

```
{1: 1, 2: 2, 3: 3, 4: 4}
```

This means that, for example, the number 2 appeared twice in the list, and the number 4 appeared four times. Counting with dictionaries is a useful technique for various tasks, such as analyzing data and finding the frequency of elements in a collection.
### Retrieving from Dictionaries
In Python 3, dictionaries are used to store collections of key-value pairs. You can retrieve items (key-value pairs) from dictionaries using the following methods:

1. **.keys()**: This method returns a list of all the keys in the dictionary.

   In simple terms, it's like getting a list of labels that you can use to access the corresponding values in the dictionary. Here's how it works:

   ```python
   my_dict = {'name': 'Alice', 'age': 30, 'city': 'New York'}

   keys = my_dict.keys()
   print(keys)  # Outputs: dict_keys(['name', 'age', 'city'])
   ```

2. **.values()**: This method returns a list of all the values in the dictionary.

   It gives you access to the actual data associated with the keys. Here's an example:

   ```python
   my_dict = {'name': 'Alice', 'age': 30, 'city': 'New York'}

   values = my_dict.values()
   print(values)  # Outputs: dict_values(['Alice', 30, 'New York'])
   ```

3. **.items()**: This method returns a list of all the key-value pairs (items) in the dictionary as tuples.

   It provides a way to access both the keys and their associated values. Here's how it's used:

   ```python
   my_dict = {'name': 'Alice', 'age': 30, 'city': 'New York'}

   items = my_dict.items()
   print(items)  # Outputs: dict_items([('name', 'Alice'), ('age', 30), ('city', 'New York')])
   ```

In summary:

- `.keys()` gives you the keys.
- `.values()` gives you the values.
- `.items()` gives you the key-value pairs as tuples.

These methods are useful for iterating through the elements in a dictionary or for checking if a specific key or value is present in the dictionary.
## 10 - Tuples
In simple terms, a Python 3 tuple is a data structure that allows you to store a collection of elements, just like a list, but with some key differences:

1. **Immutable**: The most significant difference is that tuples are immutable, which means once you create a tuple, you cannot change its elements. In contrast, lists are mutable, and you can modify their contents.

2. **Ordered**: Tuples, like lists, are ordered, which means they maintain the order of elements in the way you define them.

3. **Heterogeneous**: Tuples can contain elements of different data types, including numbers, strings, and even other tuples.

Here's how you create a tuple:

```python
my_tuple = (1, "apple", 3.14)
```

And you can access elements using indexing, just like with lists:

```python
print(my_tuple[0])  # Access the first element (1)
print(my_tuple[1])  # Access the second element ("apple")
```

Since tuples are immutable, you cannot change their elements once they're created:

```python
my_tuple[0] = 2  # This will result in an error because tuples are immutable
```

Tuples are often used when you want to group related pieces of data together and ensure that they **cannot be modified accidentally**. For example, you might use a tuple to represent the (x, y) coordinates of a point on a graph or to store a date as (year, month, day).
## 11.1 - Regular Expressions (Regex)
In simple terms, Python 3 regex, short for "regular expressions," is a powerful tool for searching and manipulating text patterns in strings. It allows you to perform tasks like finding specific words, validating email addresses, or extracting information from text by describing patterns of characters you want to match.

Here's a basic explanation:

1. **Patterns**: You define a pattern that describes the text you want to find. This pattern can include letters, numbers, special characters, and placeholders for various types of characters.

2. **Matching**: You can use this pattern to search within a larger text (a string). When the pattern matches a part of the text, it returns a match.

3. **Functions**: Python provides functions and libraries (like `re` module) for working with regex. You use these functions to perform operations like searching, replacing, or extracting text based on your pattern.

For example, suppose you want to find all email addresses in a text. You could create a regex pattern for email addresses and use it to search through the text. When a match is found, you can extract or process those email addresses.

Here's a simple example of using regex in Python:

```python
import re

text = "My email addresses are john@example.com and mary@email.org."
pattern = r'\b[\w\.-]+@[\w\.-]+\.\w+\b'

matches = re.findall(pattern, text)

for match in matches:
    print("Found email:", match)
```

In this example:

- We import the `re` module, which provides regex functionality.

- We define a regex pattern (`r'\b[\w\.-]+@[\w\.-]+\.\w+\b'`) that matches typical email addresses.
	- Let's break down the regex pattern `r'\b[\w\.-]+@[\w\.-]+\.\w+\b'` into smaller parts:

	1. `r`: This is a prefix used before the pattern string to indicate that it is a "raw string." In Python, raw strings are often used with regular expressions to avoid the need to escape backslashes.
	
	2. `'\b`: This is the `\b` part at the beginning of the pattern. It represents a word boundary, which is a position between a word character (like a letter or digit) and a non-word character (like whitespace or punctuation). It ensures that the email address starts at the beginning of a word.
	
	3. `[\w\.-]+`: This part represents the username part of the email address. Here's the breakdown:
	   - `[\w\.-]`: This is a character set enclosed in square brackets (`[...]`). It matches a single character that is either a word character (`\w` includes letters, digits, and underscores), a dot (`.`), or a hyphen (`-`).
	   - `+`: This is a quantifier that means "one or more." It indicates that the character set `[\w\.-]` should be repeated one or more times to match a username with multiple characters.
	
	4. `@`: This is a literal character that matches the "@" symbol in an email address.
	
	5. `[\w\.-]+`: This part is similar to the username part but matches the domain name. It includes letters, digits, dots, and hyphens.
	
	6. `\.`: This matches a literal dot (".") in the email address.
	
	7. `\w+`: This matches one or more word characters, representing the top-level domain (TLD) such as "com," "org," or "net."
	
	8. `\b`: This is another word boundary, similar to the one at the beginning. It ensures that the email address ends at the end of a word.
	
	- So, when you put all these parts together, the regex pattern `r'\b[\w\.-]+@[\w\.-]+\.\w+\b'` matches a complete email address with the following characteristics:
	
	- It starts and ends at word boundaries.
	- It has a username part that can include word characters, dots, and hyphens.
	- It is followed by the "@" symbol.
	- It has a domain name part that can include word characters, dots, and hyphens.
	- It ends with a top-level domain (TLD) like "com," "org," or "net."

- We use `re.findall()` to find all matches of this pattern in the `text` string.

- We loop through the matches and print each email address found in the text.

- `.search()` and `.match()` are two functions provided by the `re` module for working with regular expressions (regex).

1. **`.search()` Function**:

   - **Purpose**: The `.search()` function is used to search for a pattern within a string. It looks for the first occurrence of the pattern in the string and returns a match object if found.
   
   - **Usage**: You provide the regex pattern you want to find as the first argument, and the string you want to search in as the second argument.

   - **Example**:
     ```python
     import re

     text = "Hello, my email is example@email.com"
     pattern = r"\w+@\w+\.\w+"

     match = re.search(pattern, text)

     if match:
         print("Email found:", match.group())
     else:
         print("Email not found")
     ```

   - **Explanation**: In this example, `.search()` looks for an email pattern within the `text` string. It finds the first occurrence of an email address and returns a match object. We then use `match.group()` to retrieve the matched email address.

2. **`match()` Function**:

   - **Purpose**: The `.match()` function checks if a pattern matches at the beginning of a string. It only returns a match if the pattern is found at the start of the string.
   
   - **Usage**: Like `.search()`, you provide the regex pattern as the first argument, but `.match()` is typically used when you want to check if a string starts with a specific pattern.

   - **Example**:
     ```python
     import re

     text = "apple banana cherry"
     pattern = r"apple"

     match = re.match(pattern, text)

     if match:
         print("Pattern found at the beginning of the string")
     else:
         print("Pattern not found at the beginning of the string")
     ```

   - **Explanation**: In this example, `.match()` checks if the `text` string starts with the word "apple." Since it does, the function returns a match object, and we print that the pattern was found at the beginning of the string.

In summary:
- `.search()` searches for a pattern anywhere in the string and returns the first match found.
- `.match()` checks if the pattern matches only at the beginning of the string. It returns a match if the pattern is at the start of the string.

Regular expressions can become quite complex for advanced tasks, but they're incredibly useful for text processing and searching when you need to work with specific patterns in your data.

Python Regular Expression Quick Guide

^        Matches the beginning of a line **or** doesn't match the following characters or symbols
$        Matches the end of the line
.        Matches any character
\s       Matches whitespace
\S       Matches any non-whitespace character
`*`        Repeats a character zero or more times
*?       Repeats a character zero or more times 
         (non-greedy)
`+`        Repeats a character one or more times
+?       Repeats a character one or more times 
         (non-greedy)
[aeiou]  Matches a single character in the listed set
[^XYZ]   Matches a single character not in the listed set
[a-z0-9] The set of characters can include a range
(        Indicates where string extraction is to start
)        Indicates where string extraction is to end
|        Match either item on each side of the pipe
`\`       Escapes special characters to match a search like ".com"
`{ }`   Curly braces represent repetition. 
## 12.1 - Networked Technology
1. TCP Connections / Sockets - In computer networking, an Internet socket or network socket is an endpoint of a bidirectional inter-process communication flow across an Internet Protocol-based computer network, such as the Internet.
2. TCP Ports
	- A port is an application-specific or process-specific software communications endpoint
	- Allows multiple networked applications to coexist on the same server
	- Common TCP Ports
		- Telnet (23) - Remote Access
		- SSH (22) - Secure Remote Access
		- HTTP (80) - Web Browsing
		- HTTPS (443) - Secure Web Browsing
		- SMTP (25) - Mail
		- IMAP (143/220/993) - Mail Retrieval
		- POP (109/110) - Mail Retrieval
		- DNS (53) - Domain Name
		- FTP (21) - File Transfer
### Sockets in Python
Python has built-in support for TCP Sockets

```Python
import socket
mysock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
mysock.connect( ('data.pr4e.org', 80) ) # Host, Port
```

Three lines of code is all that's needed to make a basic connection to an endpoint

You can also use the above code to send commands to a site/server to retrieve/send files/data.

```Python
import socket
mysock = socket.socket(socket.AF_INET, socket.SOCK_STREAM)
mysock.connect( ('data.pr4e.org', 80) ) # Host, Port

mysock.send('GET http://data.pr4e.org/romeo.txt HTTP/1.0\r\n\r\n'.encode())

while True:
	data = mysock.recv(512) # Receive upto 512 bytes of data
	if (len(data) < 1):
		break
	print(data.decode())
mysock.close()
```
## 12.3 - Unicode Characters and Strings
In simple terms, Unicode characters and strings in Python 3 allow you to work with a wide range of characters and symbols from various languages and writing systems, making it easier to handle text in a global context.

1. **Unicode Characters**:
   - Unicode is a standard that assigns a unique number (called a code point) to every character, symbol, and emoji from almost all the world's writing systems.
   - Unicode characters include letters from different languages (e.g., English, Chinese, Arabic), special symbols (e.g., ©, €), and emojis (e.g., 😊).
   - Unicode ensures that you can represent and work with text in multiple languages and character sets within a single program.

2. **Strings**:
   - In Python 3, a string is a sequence of Unicode characters. It can be made up of letters, digits, symbols, and spaces.
   - Strings are enclosed in single (' '), double (" "), or triple (''' ''' or """ """) quotes.
   - Examples of strings:
     - `"Hello, world!"` (English text)
     - `"你好，世界！"` (Chinese text)
     - `"مرحبا بالعالم!"` (Arabic text)
     - `"😊"` (Emoji)
   
So, in Python 3, you can work with text that includes characters and symbols from different languages and cultures using Unicode. This makes it a powerful tool for handling multilingual and diverse text data in your programs.

In simple terms, `.encode()` and `.decode()` are methods in Python 3 that allow you to convert between strings and bytes when working with networking or file I/O.

1. **.encode()**:
   - When you have a text string (a sequence of characters), you can use `.encode()` to convert it into a sequence of bytes.
   - This is particularly useful when you want to send text data over a network or save it in a binary file.
   - You specify an encoding method (e.g., UTF-8) when using `.encode()`, which determines how the characters in the string are converted to bytes.
   - Example:

     ```python
     text_string = "Hello, World!"
     byte_data = text_string.encode("utf-8")
     ```

2. **.decode()**:
   - Conversely, when you receive a sequence of bytes (e.g., from a network connection or reading a binary file) and want to interpret it as a text string, you use `.decode()`.
   - You need to know the encoding that was used when the bytes were created in order to correctly decode them.
   - Example:

     ```python
     byte_data = b'Hello, World!'
     text_string = byte_data.decode("utf-8")
     ```

In networking, these methods help ensure that data is properly converted between text and binary representations when it's transmitted over the network, allowing different systems to communicate using a common encoding scheme, such as UTF-8, which supports a wide range of characters from various languages.

### Using urllib
In simple terms, Python 3's `urllib` is a built-in library that allows you to work with URLs (Uniform Resource Locators) in your Python programs. It provides a set of modules for fetching data from the internet, making HTTP requests, and handling URLs. Here's a basic explanation:

1. **urllib.request**: This module within `urllib` lets you open and read URLs. You can use it to send HTTP requests to web servers and retrieve the content from web pages or other online resources.

   ```python
   import urllib.request

   # Open a URL and read its content
   response = urllib.request.urlopen('https://www.example.com')
   html_content = response.read()
   print(html_content)
   ```

2. **urllib.parse**: This module helps you parse URLs into their components, like scheme (http, https), hostname, path, query parameters, etc., and also construct URLs from their individual components.

   ```python
   import urllib.parse

   # Parse a URL
   url = 'https://www.example.com/somepage?param=value'
   parsed_url = urllib.parse.urlparse(url)
   print(parsed_url.scheme)
   print(parsed_url.netloc)
   print(parsed_url.path)
   print(parsed_url.query)
   ```

3. **urllib.error**: This module contains exceptions that are raised when there are errors during URL operations, such as HTTP errors or network issues.

   ```python
   import urllib.error

   try:
       response = urllib.request.urlopen('https://www.nonexistentpage.com')
   except urllib.error.HTTPError as e:
       print("HTTP error:", e)
   except urllib.error.URLError as e:
       print("URL error:", e)
   ```

In simple terms, `urllib` is a handy tool for fetching web content, parsing URLs, and handling errors related to internet communication in Python. It's often used in web scraping, web API access, and other network-related tasks. However, some developers prefer using more feature-rich libraries like `requests` for HTTP requests due to its simpler and more user-friendly interface.

### BeautifulSoup
In simple terms, web scraping with BeautifulSoup in Python 3 is a way to extract information from websites. Here's an explanation:

1. **Getting Web Content**: Python can make requests to a website, just like a web browser. With web scraping, you use Python to fetch the web page's HTML code, which contains the information you want to extract.

2. **Parsing HTML**: BeautifulSoup is a Python library that helps you parse (read and understand) the HTML code of a web page. It organizes the HTML structure into a more accessible format that you can work with.

3. **Finding Data**: After parsing the HTML, you can use BeautifulSoup's functions to locate specific pieces of information on the web page, such as text, links, or images.

4. **Extracting Data**: Once you've identified the data you want, you can extract it from the HTML. You can then use this data in your Python program for various purposes, like analysis, storage, or display.

Here's a simple example:

```python
import requests
from bs4 import BeautifulSoup

# Make a request to a website
response = requests.get("https://example.com")

# Parse the HTML content of the webpage
soup = BeautifulSoup(response.text, "html.parser")

# Find and extract specific data
title = soup.title.string  # Extract the title of the webpage
paragraphs = soup.find_all("p")  # Find all paragraphs on the page

# Print the extracted data
print("Title:", title)
for p in paragraphs:
    print("Paragraph:", p.text)
```

In this code:

- We use the `requests` library to make an HTTP request to a website and get its HTML content.
- Then, we use BeautifulSoup to parse the HTML and navigate it to find specific elements like the webpage's title and paragraphs.
- Finally, we extract and print the desired data.

Web scraping can be used for various purposes, such as data analysis, content aggregation, or monitoring websites for changes. However, it's essential to respect websites' terms of service and legal regulations when scraping their content.

- *Code snippet to ignore SSL certificate errors
```Python
ctx = ssl.create_default_context()
ctx.check_hostname = False
ctx.verify_mode = ssl.CERT_NONE

# Set .urlopen(url, context=ctx) to refer back to the empty SSL
```

## 13.1 - XML
In simple terms, XML (Extensible Markup Language) is a way to structure and store data in a text-based format. It uses tags to define elements and their relationships, making it easy to represent structured data. Here's a basic explanation of parsing XML in Python 3:

**XML**: 
- XML is like a language for organizing information.
- It uses tags enclosed in angle brackets (`<tag>`) to define elements.
- Elements can have attributes (additional information) inside the tags.
- Elements can be nested within each other to create a hierarchy.

**Parsing XML in Python**:
- Parsing XML means reading an XML document and extracting information from it.
- Python provides libraries like `xml.etree.ElementTree` and `xml.dom.minidom` for XML parsing.
- The process involves opening and reading an XML file or string, then navigating through the elements to access the data you need.

Here's a simple example using `xml.etree.ElementTree`:

```python
import xml.etree.ElementTree as ET

# Sample XML data
xml_data = '''
<data>
    <item>
        <name>Apple</name>
        <price>1.00</price>
    </item>
    <item>
        <name>Banana</name>
        <price>0.50</price>
    </item>
</data>
'''

# Parse the XML data
root = ET.fromstring(xml_data)

# Access and print information
for item in root.findall('item'):
    name = item.find('name').text
    price = float(item.find('price').text)
    print(f"Item: {name}, Price: ${price:.2f}")
```

In this example:
- We create a sample XML data string.
- We use `ET.fromstring()` to parse it and get the root element.
- We then use `find()` and `.text` to access the data inside the XML elements and print it.

This is a basic example of how you can parse XML data in Python to extract and work with structured information. You can adapt this approach for more complex XML documents and real-world scenarios.

### XSD
In simple terms, XSD stands for XML Schema Definition. It's a way to define the structure and constraints of XML data. XSD serves as a blueprint or a set of rules that describe what valid XML data should look like. It's often used to ensure that XML documents conform to a specific structure and data format.

Here's a simple example to illustrate XSD and data parsing in Python 3:

Suppose you have an XSD schema that defines the structure of a simple XML document representing information about books:

```xml
<!-- books.xsd -->
<xs:schema xmlns:xs="http://www.w3.org/2001/XMLSchema">
  <xs:element name="book">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="title" type="xs:string"/>
        <xs:element name="author" type="xs:string"/>
        <xs:element name="published" type="xs:date"/>
      </xs:sequence>
    </xs:complexType>
  </xs:element>
</xs:schema>
```

In this XSD schema:

- We define an XML element called "book."
- Inside "book," we specify that it should contain "title," "author," and "published" elements in that order.
- We also specify the data types for each element (e.g., "title" and "author" should be strings, and "published" should be a date).

Now, let's say you have an XML document (`books.xml`) that follows this schema:

```xml
<!-- books.xml -->
<book>
  <title>Python Programming</title>
  <author>John Doe</author>
  <published>2023-10-30</published>
</book>
```

To parse this XML data in Python 3 and validate it against the XSD schema, you can use the `lxml` library, which provides support for XML parsing and validation:

```python
from lxml import etree

# Load the XSD schema
xsd_schema = etree.XMLSchema(file="books.xsd")

# Load and parse the XML document
xml_doc = etree.parse("books.xml")

# Validate the XML document against the XSD schema
if xsd_schema.validate(xml_doc):
    print("XML document is valid according to the XSD schema.")
else:
    print("XML document is not valid according to the XSD schema.")
```

In this Python script:

- We load the XSD schema using `etree.XMLSchema`.
- We load and parse the XML document using `etree.parse`.
- We validate the XML document against the XSD schema using `xsd_schema.validate`.

If the XML document conforms to the XSD schema, it will be considered valid, and the script will print "XML document is valid according to the XSD schema." Otherwise, it will print "XML document is not valid according to the XSD schema."
## 13.5 - JavaScript Object Notation (JSON)
In simple terms, JSON (JavaScript Object Notation) is a lightweight and easy-to-read data interchange format. It's used to store and exchange data between different programs or systems, especially when they're written in different programming languages. JSON data is represented as text, making it human-readable and machine-readable.

Here's a simple explanation of JSON and an example in Python 3:

**JSON Basics:**
- JSON data consists of key-value pairs enclosed in curly braces `{}`.
- Keys are strings enclosed in double quotes.
- Values can be strings, numbers, objects (nested key-value pairs), arrays (ordered lists of values), `true`, `false`, or `null`.

**Example:**
Suppose you want to represent information about a person using JSON:

```json
{
  "name": "John Doe",
  "age": 30,
  "is_student": false,
  "hobbies": ["reading", "hiking"],
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA"
  }
}
```

In this JSON example:

- `"name"` is a key with a string value.
- `"age"` is a key with a numeric value.
- `"is_student"` is a key with a Boolean (true or false) value.
- `"hobbies"` is a key with an array of strings as its value.
- `"address"` is a key with an object (nested key-value pairs) as its value.

In Python, you can work with JSON data using the built-in `json` module. Here's an example of how to parse (read) JSON data in Python:

```python
import json

# JSON data as a string (you can also read it from a file)
json_data = '''
{
  "name": "John Doe",
  "age": 30,
  "is_student": false,
  "hobbies": ["reading", "hiking"],
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA"
  }
}
'''

# Parse the JSON data into a Python dictionary
data = json.loads(json_data)

# Accessing values in the parsed JSON
print("Name:", data["name"])
print("Age:", data["age"])
print("Hobbies:", ", ".join(data["hobbies"]))
print("City:", data["address"]["city"])
```

In this example, we first import the `json` module, then use `json.loads()` to parse the JSON data into a Python dictionary. Once parsed, you can access and manipulate the data using regular Python syntax.
## 13.6 - Service-Oriented Architecture
In simple terms, Service-Oriented Architecture (SOA) in Python 3 refers to a way of designing and building software systems where different parts of the system are organized as independent services. Each service performs a specific function and communicates with other services through well-defined interfaces or APIs (Application Programming Interfaces).

Here's how SOA applies to Python 3:

1. **Services**: In Python 3, services are typically implemented as separate Python programs or modules. Each service focuses on a specific task or capability within the larger software system. For example, you might have one service for handling user authentication, another for processing payments, and another for generating reports.

2. **Intercommunication**: Services in SOA communicate with each other using standard protocols and data formats. Python 3 provides libraries and frameworks for building APIs and handling communication between services. Common methods for communication include HTTP, JSON, and RESTful APIs.

3. **Independence**: Services are designed to be independent, meaning they can be developed, deployed, and scaled separately from each other. This makes it easier to update or replace one service without affecting the entire system.

4. **Flexibility and Reusability**: SOA promotes flexibility and reusability of code. Python's modular and object-oriented programming features are well-suited for building reusable service components. You can create libraries or modules that provide specific functionality and reuse them across multiple services.

5. **Scalability**: Python 3 and SOA allow you to scale different services independently based on their specific demands. For example, if one service experiences high traffic, you can scale it up without affecting the performance of other services.

6. **Maintenance**: When using Python 3 in SOA, maintenance becomes more manageable. You can update or fix issues in one service without disrupting the operation of the entire system. This modular approach simplifies debugging and maintenance efforts.

In summary, in Python 3, Service-Oriented Architecture involves designing and implementing software systems as a collection of independent services that communicate with each other through well-defined interfaces. This approach offers flexibility, scalability, and maintainability, making it easier to build and manage complex applications.
## 13.7 - Application Programming Interfaces (API)

**1. What is an API?**
   - An API is like a set of rules and tools that allows different software programs to communicate and work together. It defines how one piece of software can request and exchange data with another.

**2. Using APIs in Python 3:**
   - Python 3 can interact with various APIs to access data or services provided by other software systems, websites, or services.

**3. Making API Requests:**
   - In Python 3, you can use libraries like `requests` to make HTTP requests to web APIs. These requests can be used to retrieve data from a remote server.

   Example:
   ```python
   import requests

   response = requests.get("https://api.example.com/data")
   data = response.json()  # Convert the response to Python data
   ```

   - In this example, we use the `requests` library to send a GET request to an API, and we receive a response containing data, which we can then parse and use.

**4. Parsing API Responses:**
   - API responses often come in JSON format. Python 3 can easily parse JSON data using the built-in `json` module.

   Example:
   ```python
   import json

   json_data = '{"name": "John", "age": 30}'
   data = json.loads(json_data)
   print(data["name"])  # Accessing data from the JSON response
   ```

   - In this code, we parse a JSON response into a Python dictionary so that we can work with the data more easily.

**5. Using API Data:**
   - Once you have the data from an API, you can use it for various purposes, such as displaying it on a website, analyzing it, or integrating it into your own application.

**6. Authentication and API Keys:**
   - Some APIs require authentication to access data. In Python 3, you can include API keys or tokens in your API requests to authenticate yourself.

**7. API Documentation:**
   - When using an API in Python 3, it's essential to refer to the API's documentation, which provides information on how to make requests, what data is available, and any special requirements or limitations.

In summary, Python 3 can interact with APIs to retrieve and work with data from various sources, allowing you to access and utilize external services and information in your Python applications.
### REST vs SOAP
In simple terms, **REST (Representational State Transfer)** and **SOAP (Simple Object Access Protocol)** are two different approaches for creating APIs (Application Programming Interfaces) that allow different software systems to communicate with each other. Here are the key differences between REST and SOAP APIs:

1. **Protocol**:
   - **REST**: It is an architectural style and does not rely on a specific protocol. However, it is commonly implemented over HTTP.
   - **SOAP**: It is a protocol with a specific set of rules and uses XML for message formatting. It can work over various lower-level protocols like HTTP, SMTP, and more.

2. **Message Format**:
   - **REST**: Uses a variety of message formats, such as JSON, XML, HTML, and plain text, but JSON is the most common choice.
   - **SOAP**: Uses XML exclusively for message formatting.

3. **Ease of Use**:
   - **REST**: Generally considered simpler and easier to work with, especially for web services. It relies on standard HTTP methods like GET, POST, PUT, DELETE, which are familiar to web developers.
   - **SOAP**: Typically more complex due to its strict XML structure and additional standards. It often requires specialized libraries or tools to work with.

4. **Statelessness**:
   - **REST**: Emphasizes statelessness, meaning each request from a client to a server must contain all the information needed to understand and process the request. Sessions can be managed on the client side.
   - **SOAP**: Supports both stateful and stateless operations. It has built-in features for maintaining session state.

5. **Flexibility**:
   - **REST**: Provides flexibility in data formats and is often used in scenarios where simplicity and efficiency are essential, such as mobile applications and web services.
   - **SOAP**: Offers strict rules and standards, which can be advantageous in some enterprise-level scenarios where reliability and security are critical.

6. **Error Handling**:
   - **REST**: Uses standard HTTP status codes for indicating errors, making it easy to understand error responses.
   - **SOAP**: Has a more elaborate error handling mechanism using its own fault codes and structures.

7. **Caching**:
   - **REST**: Supports caching, which can improve performance by storing and reusing responses.
   - **SOAP**: Typically does not have built-in caching mechanisms.

8. **Security**:
   - **REST**: Offers security through HTTPS and can implement various authentication mechanisms, but it requires additional considerations for security.
   - **SOAP**: Provides built-in security features like WS-Security, which can be useful in enterprise-level applications.

In summary, REST is often preferred for its simplicity, speed, and widespread use in web and mobile applications. SOAP, on the other hand, is commonly used in enterprise-level systems where strict standards and reliability are crucial, even though it comes with additional complexity. The choice between REST and SOAP depends on the specific needs and constraints of a given project or system.
## 14.1 - Object Oriented Definitions and Terminology
Object-Oriented Programming (OOP) is a programming paradigm that organizes code into objects, which are instances of classes. It's a way of structuring and designing code to model real-world entities, making it more modular, reusable, and easier to maintain.

In simple terms, here's what OOP entails:

1. **Objects**: Objects are instances of classes, and they represent real-world entities or concepts. These objects have attributes (properties) and methods (functions) that define their behavior.

2. **Classes**: Classes serve as blueprints for creating objects. They define the structure (attributes) and behavior (methods) that objects of that class should have.

3. **Encapsulation**: Encapsulation is the concept of bundling data (attributes) and the methods (functions) that operate on that data into a single unit (an object). It allows you to control access to the internal state of an object.

4. **Inheritance**: Inheritance allows you to create new classes (child or subclass) based on existing classes (parent or superclass). The child class inherits attributes and methods from the parent class and can also have its own unique attributes and methods.

5. **Polymorphism**: Polymorphism enables different objects to respond to the same method or function call in a way that's appropriate for their specific class. It allows you to write more generic and flexible code.

In Python 3, OOP is implemented using classes and objects. Here's a simple example to illustrate how OOP is used in Python:

```python
# Define a class
class Dog:
    def __init__(self, name, breed):
        self.name = name
        self.breed = breed

    def bark(self):
        print(f"{self.name} says Woof!")

# Create objects (instances) of the class
dog1 = Dog("Buddy", "Golden Retriever")
dog2 = Dog("Charlie", "Poodle")

# Access attributes and call methods of objects
print(f"{dog1.name} is a {dog1.breed}.")
dog2.bark()
```

> Bonus Tip: Since you can't `return` when not within a function, you can `import sys` then call `sys.exit (<whatever-you-want-to-return>)`

In this example:

- We define a class called `Dog`, which has attributes (`name` and `breed`) and a method (`bark`).
- We create two instances of the `Dog` class (`dog1` and `dog2`) with different attribute values.
- We access attributes (`name` and `breed`) and call the `bark` method on the objects.

This demonstrates the fundamental concepts of OOP in Python: classes, objects, attributes, and methods, allowing you to model and manipulate objects with ease, making your code more organized and reusable.
## 15.1 - Relational Databases
In simple terms, a relational database in Python 3 is a structured and organized way to store and manage large amounts of data, where the data is organized into tables with rows and columns. It's called "relational" because it maintains relationships between different pieces of data.

Here are some key points to understand:

1. **Tables**: Data is stored in tables, which are similar to spreadsheets. Each table has rows and columns. Rows represent individual records or data entries, and columns represent different attributes or properties of those records.

2. **SQL**: Relational databases are typically managed using a language called SQL (Structured Query Language). You use SQL commands to create, retrieve, update, and delete data from the database. Python provides libraries and modules like SQLAlchemy and sqlite3 to interact with relational databases using SQL.

3. **Data Integrity**: Relational databases enforce data integrity through constraints. This means you can define rules that ensure the data in the database remains accurate and consistent. For example, you can specify that a certain column should only contain unique values or that a column cannot be left empty (a constraint called "NOT NULL").

4. **Relationships**: You can establish relationships between tables. For example, you can have one table that stores information about customers and another table that stores their orders. By using keys (like customer IDs), you can link records in these tables to represent that each order is associated with a specific customer.

5. **ACID Properties**: Relational databases follow the ACID (Atomicity, Consistency, Isolation, Durability) properties to ensure data reliability and transactional consistency. This means that database operations are guaranteed to be reliable and maintain the integrity of the data.

Here's a simple example using Python's built-in SQLite database:

```python
import sqlite3

# Connect to a SQLite database (or create one if it doesn't exist)
connection = sqlite3.connect('mydatabase.db')

# Create a cursor to interact with the database
cursor = connection.cursor()

# Create a table to store data
cursor.execute('''CREATE TABLE IF NOT EXISTS students (
                    id INTEGER PRIMARY KEY,
                    name TEXT,
                    age INTEGER
                )''')

# Insert data into the table
cursor.execute("INSERT INTO students (name, age) VALUES (?, ?)", ("Alice", 25))

# Retrieve data from the table
cursor.execute("SELECT * FROM students")
data = cursor.fetchall()
for row in data:
    print("ID:", row[0])
    print("Name:", row[1])
    print("Age:", row[2])

# Commit changes and close the connection
connection.commit()
connection.close()
```

In this example, we create a SQLite database, define a table called "students," insert data, retrieve data, and follow the ACID properties to maintain data integrity. This demonstrates the basic concepts of working with a relational database in Python 3.
### Database Administrator (dba)
A person responsible for the design, implementation, maintenance, and repair of an organization's database. The role includes the development and design of database strategies, monitoring and improving database performance and capacity, and planning for future expansion requirements. They may also plan, coordinate, and implement security measures to safeguard the database.
### Database Model
A database model or database schema is the structure or format of a database, described in a formal language supported by the database management system, in other words, a "database model" is the application of a data model  when used in conjunction with a database management system.
### Common Database Systems
Three major Database Management Systems in wide use:
- Oracle - Large, commercial, enterprise-scale, very very tweakable
- MySQL - Simpler but very fast and scalable - commercial open source
- SqlServer - Very nice - from Microsoft (also Access)
Many other smaller projects, free and open source
- HSQL, SQLite, Postgress, ...
## 15.3 - Single Table CRUD
CRUD is an acronym that stands for Create, Read, Update, and Delete. It represents the four fundamental operations that can be performed on data within a relational database system:

1. **Create**: This operation involves adding new data or records to a database. In simple terms, it's like inserting a new row into a table. For example, you might create a new customer record in a database by adding their name, contact information, and other details.

2. **Read**: Reading refers to retrieving or querying data from the database. You can think of it as looking up information that already exists in the database. For instance, you might read or retrieve all the product names and prices from a product catalog.

3. **Update**: Updating allows you to modify existing data in the database. You might use this operation to change the address of a customer, update the quantity of a product in inventory, or edit any other information that needs modification.

4. **Delete**: Deletion is the process of removing data or records from the database. It's like erasing a row from a table. For example, you might delete a customer record if they are no longer associated with your business.

These CRUD operations are essential for interacting with and managing data in a relational database. They provide a way to create, retrieve, modify, and delete information, allowing you to maintain and manipulate the data stored in your database system.
### SQL and Common Commands
SQL (Structured Query Language) is a language used to manage and manipulate relational databases. In simple terms, SQL is like a set of instructions you give to a database to perform tasks like storing, retrieving, updating, and deleting data. Here are some common SQL commands explained in simple terms:

1. **SELECT**: This command is used to retrieve data from a database. You specify which columns you want to retrieve and from which table.

   Example:
   ```sql
   SELECT first_name, last_name FROM employees;
   ```

2. **INSERT**: Use this command to add new data (rows) to a table.

   Example:
   ```sql
   INSERT INTO customers (first_name, last_name, email) VALUES ('John', 'Doe', 'john@example.com');
   ```

3. **UPDATE**: This command is used to modify existing data in a table.

   Example:
   ```sql
   UPDATE products SET price = 15.99 WHERE id = 123;
   ```

4. **DELETE**: Use this command to remove data (rows) from a table.

   Example:
   ```sql
   DELETE FROM orders WHERE order_id = 456;
   ```

5. **CREATE TABLE**: This command is used to define a new table and its columns.

   Example:
   ```sql
   CREATE TABLE students (
       student_id INT PRIMARY KEY,
       first_name VARCHAR(50),
       last_name VARCHAR(50),
       age INT
   );
   ```

6. **ALTER TABLE**: Use this command to modify an existing table structure, such as adding or deleting columns.

   Example:
   ```sql
   ALTER TABLE employees ADD COLUMN department VARCHAR(100);
   ```

7. **DROP TABLE**: This command removes an entire table and all its data.

   Example:
   ```sql
   DROP TABLE customers;
   ```

8. **SELECT with WHERE**: You can add a `WHERE` clause to a `SELECT` statement to filter data based on a specified condition.

   Example:
   ```sql
   SELECT product_name, price FROM products WHERE category = 'Electronics';
   ```

9. **JOIN**: When you have multiple tables with related data, you can use `JOIN` to combine data from those tables based on a common column.

   Example:
   ```sql
   SELECT orders.order_id, customers.first_name
   FROM orders
   JOIN customers ON orders.customer_id = customers.customer_id;
   ```

These are some of the fundamental SQL commands. SQL allows you to interact with databases, retrieve specific data, modify records, and structure your data efficiently for various applications like web applications, business systems, and data analysis.
## 15.4 - Designing a Data Model
- Drawing a picture of the data objects for our application and then figuring out how to represent the objects and their relationships
- **Basic Rule: Don't put the same string data in twice - use a relationship instead**
- When there is one thing in the "real world" there should be one copy of that thing in the database
### Database Design
- Is an art form of its own with particular skills and experience
- Our goal is to avoid the really bad mistakes and design clean and easily understood databases
- Others may performance tune things later
- Database design starts with a picture...
### Representing a Data Model in Tables
In the context of relational databases and representing data models in tables:

1. **Primary Keys**:
   - **Use**: Primary keys are unique identifiers for each row (record) in a table. They ensure that each row in the table is distinct and can be uniquely identified.
   - **Example**: In a table of "Students," each student might have a unique student ID as the primary key.
   - **Purpose**: Primary keys help in data integrity, data retrieval, and establishing relationships between tables (via foreign keys).

2. **Logical Keys**:
   - **Use**: Logical keys are identifiers that have a meaningful business or logical significance but may not necessarily be unique. They help in organizing and querying data.
   - **Example**: In an "Employees" table, a logical key could be the employee's email address, which is unique within the organization but not globally unique.
   - **Purpose**: Logical keys provide a human-readable way to access data and often have business relevance.

3. **Foreign Keys**:
   - **Use**: Foreign keys are attributes in a table that refer to the primary key of another table. They establish relationships between tables in a relational database.
   - **Example**: In a "Orders" table, there might be a foreign key column that references the primary key (e.g., order ID) of a "Customers" table, indicating which customer placed the order.
   - **Purpose**: Foreign keys maintain data integrity and enforce referential integrity constraints. They ensure that data in related tables is consistent and that records can be linked together.

In summary:
- **Primary keys** uniquely identify each row in a table.
- **Logical keys** are meaningful identifiers but not necessarily unique.
- **Foreign keys** establish relationships between tables by referencing primary keys in other tables, ensuring data consistency and enabling data retrieval across related tables.
#### Relational Power
By removing the replicated data and replacing it with references to a single copy of each bit of data we build a "web" of information that the relational database can read through very quickly - even for very large amounts of data

- Often when you want some data it comes from a number of tables linked by these **foreign keys**.
### Implementing a Data Model

```SQL
CREATE TABLE Album (
	id        INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT UNIQUE,
	artist_id INTEGER,
	title     TEXT
)

CREATE TABLE Track (
	id       INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT UNIQUE,
	title    TEXT,
	album_id INTEGER,
	genre_id INTEGER,
	len      INTEGER,
	rating   INTEGER,
	count    INTEGER
)
```
### Inserting Relational Data

Single Values
```SQL
INSERT INTO Artist (name) VALUES ('Led Zepplin')

INSERT INTO Genre (name) VALUES ('Rock')
```

Multiple Values
```SQL
INSERT INTO Album (title, artist_id) VALUES ('Who Made Who', 2)
```
## 15.7 - Reconstructing Data with JOIN

The JOIN operation **links across several tables** as part of a select operation

You must tell the JOIN how to use the keys that make the connection between the tables using an ON clause.
- If you don't use an ON clause, then ALL COMBINATIONS are combined. Essentially number of data from one table multiplied by the other table
## 15.8 - Many-Many Relationships
Sometimes we need to model a relationship that is many-many. We need to add a "connection" table with two foreign keys. **There is usually no separate primary key.**
### Creating the Tables
```SQL
CREATE TABLE User (
	id    INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT UNIQUE,
	NAME  TEXT,
	email TEXT
)

CREATE TABLE Course (
	id    INTEGER NOT NULL PRIMARY KEY AUTOINCREMENT UNIQUE,
	title TEXT
)

CREATE TABLE Member (
	user_id   INTEGER,
	course_id INTEGER,
	role      INTEGER,
	PRIMARY KEY (user_id, course_id)
)
```
### Retrieving data from the Tables
```SQL
SELECT User.name, Member.role, Course.title FROM User JOIN Member JOIN Course ON Member.user_id = User.id AND Member.course_id = Course.id ORDER BY Course.title, Member.role DESC, User.name
```
## Multi-Step Data Analysis
Multi-Step Data Analysis applies to how your raw data source is handled from the beginning of your project to the end.

Steps:
1. Gather
2. Clean/Process
3. Visualize and/or Analyze