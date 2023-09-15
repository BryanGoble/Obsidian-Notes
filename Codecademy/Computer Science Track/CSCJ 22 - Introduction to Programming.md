
# Python Syntax

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