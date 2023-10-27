# Courses
1. [Programming For Everybody (Getting Started With Python)](https://www.coursera.org/learn/python/)
2. [Programming For Everybody (Python Data Structures)](https://www.coursera.org/learn/python-data/)
3. [Programming For Everybody (Using Python to Access Web Data)](https://www.coursera.org/learn/python-network-data)

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

Regular expressions can become quite complex for advanced tasks, but they're incredibly useful for text processing and searching when you need to work with specific patterns in your data.

Python Regular Expression Quick Guide

^        Matches the beginning of a line
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
