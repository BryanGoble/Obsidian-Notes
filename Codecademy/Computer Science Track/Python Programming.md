
# Syntax [^2]

- Multi-line Strings
		- Python strings can occupy multiple lines by surrounding the text in three quotation marks either double or single `'''` `"""`.
- Comments
	- Annotate comments with a `#`.
- Data Types:
	- Strings `str`
	- Numbers: `int`, `float`, `complex`
	- Binary: `bytes`, `bytearray`, `memoryview`
	- Booleans `bool`
	- Sequence: `list`, `range`, `tuple`
	- Sets: `set`, `frozenset`
	- Dictionary: `dict`
- Built-in functions:
	- `type(<variable>)`
		- Used to retrieve the data type of an object
	- `isinstance(<variable>, <data_type>)`
		- Used to test if an object is an instance of a specified type.
		- Returns either `True` or `False`
	- `zip(<list1>, <list2>)`
		- Used to quickly combine associated data-sets without needing to rely on multi-dimensional lists (2D).
		- Takes two (or more) lists as inputs and returns an object (location of the assigned variable in our computers memory) that contains a list of **tuple** pairs.
			- The output will look like this: `0x7f1631e86b48`
			- To convert this object to a human readable format just convert the object or assigned variable to a list - `list(<variable>)`
	- `list()` - converts an object to a list
	- `range()` - takes an input then generates numbers from 0 to right before the number specified unless the starting value is also noted.
		- You can also specify a 3rd value to note the 'skips' or increments
	- `sorted()` - contrary to the `.sort()` method, `sorted()` actually creates a new list rather than modifying the existing one
- Built-in Methods:
	- In Python, for any specific data type there are built-in functions called *methods* that we can use to create, manipulate, or delete data.
	- Most follow the format of `<variable_name>.method()`. Some methods require an input value between the parentheses.
	- Common Methods:
		- `.append()` - allows us to add an element to the end of a list
		- `.pop()` - removes the last item in a list or you can specify by index
		- `.count()` - Counts number of iterations of a specified item in a list
		- `.sort()` - Sorts items in a list by alphabetical or numerical order.
			- can also add `reverse=True` within the parentheses to reverse the output
		- `.split(delimiter)` - split a string at the specified delimiter(s)
			- If a delimiter is not specified, then splitting at the spaces is default.
		- `'delimiter'.join(list-to-combine)` - Joins the items in a list with the delimiter.
			```Python
			my_munequita = ['My', 'Spanish', 'Harlem', 'Mona', 'Lisa']  
			print(' '.join(my_munequita))  
			# => 'My Spanish Harlem Mona Lisa'
			```
		- `.strip()` - Removes all of the whitespace before and after the string. if you specify an item to strip in the parentheses, the method will only strip that item and no longer strip the whitespace.
		- `.replace(argument1, argument2)` - Takes two arguments and replaces all instances of the first argument with the second
		- `.find()` - takes a string as an argument and searches the string it was ran on for the index of the first instance of the specified string.
			```Python
			print('smooth'.find('t'))  
			# => '4'
			```
		- `.title()` - Capitalizes every first letter of each word in the string
		- `.lower()` - Changes each character in a string to its lowercase form
		- `.upper()` - Changes each character in a string to its uppercase form
		- `.format(arg1, arg2, etc)` - used to dynamically replace values based on the values of the arguments specified
## Read/Write a File
- You can import other files in your project with the `with` statement.
	- The `with` statement, creates a context-manager, which performs cleanup after exiting the adjacent indented block. This replaces the old method of having to open and close the included file.
	- Default action is to open the file in read-only mode. An `'r'` argument can be specified in `open()`, but not necessary due to default.
	- If `'w'` is specified, that opens the file in write mode. This will write over the contents of the file when `.write()` is called.
	- If `a` is specified, this will open the file in append mode and will only append to the document when `.write()` is called.
	```Python
	with open('real_cool_document.txt', <optional_arg>) as cool_doc:
		cool_contents = cool_doc.read()
	print(cool_contents)
	```
- `.read()` allows us to read the content of the imported file
- `.readlines()` will read each line of the file one at a time
- `.readline()` will read one line at a time in succession every time the method is called.
	```Python
	# Example.txt
	You do look, my son, in a moved sort,
	As if you were dismayed: be cheerful, sir.

	with open('Example.txt') as first_line_doc:
	  first_line = first_line_doc.readline()
	print(first_line) # You do look, my son, in a moved sort,
	```
- `.write()` used to write/append to the file depending on whether 'w' or 'a' was specified.
### CSV Handling
- Using the standard `with` statement, we can read csv files just like any other file.
- CSVs are, of course, different from standard text files as they can store/organize data to be used elsewhere.
- CSV isn't built-in to Python, so you do need to import the `csv` module first.
#### CSV Read
- Replace the second argument in `open()` with `newline=''` to ignore escape characters, `\n`, and specify that the end of the row is at the end of each row of text.
- The first row in each CSV file is by default the header row, so you can use the text of each header as an index to pick data from the rest of the rows.
	```Python
	import csv  
  
	list_of_email_addresses = []  
	with open('users.csv', newline='') as users_csv:  
	  user_reader = csv.DictReader(users_csv)  
	  for row in user_reader:  
	    list_of_email_addresses.append(row['Email'])
```
- `.DictReader(<alt_file_name>, delimiter=';')` - csv module method to convert the lines of the CSV file to dictionaries that can be referenced using the header name.
	- An optional `delimiter=` argument can be specified if the file doesn't use commas as the default data separator.
#### CSV Write
- Just as we can read CSV files, we can also write/create them from prebuilt dictionaries.
- Using `with` open the csv and use `'w'` as the second argument.
- `DictWriter(<alt_file_name>, fieldnames=<field_variable>)` - csv method to write to a CSV file.
	- `fieldnames=` is specified to reference the headers for each row.
- `.writeheader()` will write the `fieldnames` as the file header
- `.writerow()` will write the specified item(s) to the following rows.
	```Python
	big_list = [{'name': 'Fredrick Stein', 'userid': 6712359021, 'is_admin': False}, {'name': 'Wiltmore Denis', 'userid': 2525942, 'is_admin': False}, {'name': 'Greely Plonk', 'userid': 15890235, 'is_admin': False}, {'name': 'Dendris Stulo', 'userid': 572189563, 'is_admin': True}]  
	  
	import csv  
	  
	with open('output.csv', 'w') as output_csv:  
	  fields = ['name', 'userid', 'is_admin']  
	  output_writer = csv.DictWriter(output_csv, fieldnames=fields)  
	  
	  output_writer.writeheader()  
	  for item in big_list:  
	    output_writer.writerow(item)
```
### JSON Handling
- Python is also able to handle JavaScript Object Notation (JSON) files. 
- JSON format is very similar to Python's dictionaries which makes it easily readable from the developers standpoint.
- Just like CSV files, JSON handling is also not built-in. Use `import json` to bring in the JSON package.
#### JSON Read
- `.load(<alt_file_name>)` - Reads and converts the data to a python dictionary, similar to `.DictReader()`
#### JSON Write
- As standard practice, remember to specify `'w'` in `open()`
- `.dump(<dictionary_var>, <alt_file_name>)` - Converts a Python dictionary to JSON format then writes that data to the specified JSON file.
## Control Flow
- Boolean Expressions (bool) = `True` or `False`
	- Logical Operators
		- `and`
			- Only True/True equal to True, otherwise False
		- `or`
			- Only one side needs to be True
		- `not`
			- Flips from True to False and vice versa
- Relational Operators
	- Equals `==`
	- Not Equals `!=`
	- Greater than `>`
	- Greater than or equal to `>=`
	- Less than `<`
	- Less than or equal to `<=`
- Conditional Statements
	- `if`
	- Else if `elif`
	- `else`
## Loops
### For
- Used to iterate over and perform an action one time for each element in a list or range.
```Python
for <temporary value> in <list>:
	print(<temporary value>)
```
### While
- Will repeatedly execute a code block as long as a condition evaluates to `True`.
- Condition of a `while` loop is always checked first before the block of code runs. If the condition is not met, then the code never runs or stops running.
```Python
while <condition>:
	# Code here

hungry = True 

while hungry: # This while loop will run once then stop
	print("Time to eat!")
	hungry = False
```
### Nested Loops
- Loops can be nested inside of other loops.
```Python
groups = [['Jobs', 'Gates'], ['Newton', 'Euclid'], ['Einstein', 'Feynman']]

for i in groups:
	for name in i:
		print(name)

# Output would be:
# Jobs
# Gates
# Newton
# Euclid ...
```
### Break
- The `break` keyword escapes the loop, regardless if the iteration has completed or not. Once broken, the rest of the program code will execute as necessary.
### Continue
- `continue` is used inside a loop to skip the remaining code inside the loop code block and begin the next loop iteration
```Python
big_number_list = [1, 2, -1, 4, -5, 5, 2, -9]

# Print only positive numbers:
for i in big_number_list:
  if i < 0:
    continue
  print(i)

# Output:
# 1
# 2
# 4
# 5
# 2
```
## List Comprehensions
- Allows for list creation from a single line expression
- Follows the following format `[<expression> for <item> in <list> <if or for conditional(s)]`
	- The expression can be anything, any kind of object can go into a list
- List comprehensions always return lists
```Python
# Example list comprehension from codecademy.com
# List comprehension for the squares of all even numbers between 0 and 9

result = [x**2 for x in range(10) if x % 2 == 0]

print(result)

# [0, 4, 16, 36, 64]
```
## Error Handling
- Mistakes in code are referred to as errors and will point to the location where an error occurred with a `^` character.
- Classifying Errors
	- `SyntaxError` - Error caused by not following the proper structure (syntax) of the language
	- `NameError` - Error reported when the interpreter detects a variable that is unknown
	- `TypeError` - Error thrown when an operation is applied to an object of an inappropriate type
## Modules
- Importing modules is one way of utilizing code snippets or previously defined functions in our own code.
- Import a module using `import <mod-name>`
- Common modules:
	- random
## Data Structures
- From Wikipedia, a data structure is a data organization, management, and storage format that is usually chosen for efficient access to data.
- In Python, there are several built-in data structures, one being the list type which allows us to work with data in sequential order.
### Lists
- Lists are contained within brackets `[]`
- Each item is separated by a comma `,` 
- Lists are mutable, meaning changeable
- Lists can contain many data types and can even contain multiple data types at the same time including strings and integers.
- List can also contain other lists called two-dimensional (2D) lists
- We can use the `.append()` method to add singular items or concatenation `+` to add multiple lists together.
- The location of an item is called its *index*. Python lists are zero-indexed though, meaning the index starts at 0 rather than 1.
	- To call the item index, brackets after calling the list name `list_name[3]`
	- Index' can only be called using integers
	- You can also call them starting from the rear if you use a negative integer. For example, -1 will grab the final element in the list
- We can use the `.remove()` method to remove elements from lists using the element name.

### Tuples
- Tuples are similar to lists, but are immutable, meaning once created we can no longer change it dynamically.
- Tuples are contained within parentheses `()`
- Each item is separated by a comma `,`
- `.append()`, `.remove()`, `.insert()`, etc. are not able to used with tuples.
- Trailing commas are required when making a one element tuple, otherwise Python treats the item within the parentheses as its own object and not a tuple, because parentheses are also used in equations.
	- For example, `single_tuple = (2)` evaluates to `2`, whereas, `single_tuple = (2,)` evaluates to `(2)` and is treated as an actual tuple.

### Dictionaries [^1]
- A built-in data structure, used to store key-value pairs for efficient retrieval.
- Dictionaries are contained within curly braces `{}`
- Using a hash function, the keys are turned into an index within an underlying array.
```Python
# Example Dictionary from codecademy.com
states = {
  'TN': "Tennessee",
  'CA': "California",
  'NY': "New York",
  'FL': "Florida"
}

west_coast_state = states['CA']
```
- Dictionaries in Python are implemented in C, which makes them highly efficient in terms of memory and time complexity.
- The keys are hashed and the resulting hash values are used to index the key-value pairs in a hash table.
- Since Python 3.7, dictionaries are also ordered meaning the key-value pairs are stored in a specific order.
- To add a key:value pair or replace the value of a key, use the following format
	- `<dictionary>[<key>] = <value>`
	- If the key doesn't exist, it and the value will be added otherwise the key value will just be updated.
- `.get(<key-to-get>, <optional-default-value-to-return>)` - used to get the value of a specified key.
	- You can also specify an optional second argument that is returned as the default value if a value for the requested key doesn't exist.
- `.items()` - Retrieves a list of the dictionary keys and values
- `.keys()` - Retrieves a list of the dictionary keys
- `.values()` - Retrieves a list of the dictionary values
- `<key> in <dictionary-name>` - Returns `True` if key exists in dictionary, otherwise `False`
- `.pop(<key>, <optional-default-value>)` - removes the key and its value. If the key doesn't exist, an error is raised unless the default return value is included.

### Hashmaps [^1]
- Not a built-in data structure in Python, but can be implemented using a dictionary or list.
- Uses a hash function to map keys to values.
- A hash function `hash()` is a built-in mathematical function that takes an input (or 'message') and returns a fixed-size of string of characters, which is called the 'hash value'.
	- The function always returns an integer which remains constant during the current invocation of Python, but will change during the next to prevent tampering/hacking.
```Python
# Example Hashmap from programsquared.com
my_hashmap = {
			  hash('a'):1,
			  hash('b'):2,
			  hash('c'):3
			  }
print(my_hashmap)
```
- Hashmaps are unordered meaning the key-value pairs are not stored in a specific order.
- Advantaged over dictionaries due to being able to handle more data types as keys.

















# Footnotes

[^1]: https://programsquared.com/python/difference-between-dictionary-and-hashmap-in-python/#:~:text=Dictionaries%20are%20built%2Din%20and,different%20data%20types%20as%20keys.
[^2]: https://www.codecademy.com/resources/docs/python