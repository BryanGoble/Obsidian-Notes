
---
share: true  
---

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
- Built-in Methods:
	- In Python, for any specific data type there are built-in functions called *methods* that we can use to create, manipulate, or delete data.
	- Most follow the format of `<variable_name>.method()`. Some methods require an input value between the parentheses.
	- Common Methods:
		- `.append()` - allows us to add an element to the end of a list
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
- Lists can contain many data types and can even contain multiple data types at the same time including strings and integers.
- List can also contain other lists called two-dimensional (2D) lists
- We can use the `.append()` method to add singular items or concatenation `+` to add multiple lists together.
- The location of an item is called its *index*. Python lists are zero-indexed though, meaning the index starts at 0 rather than 1.
	- To call the item index, brackets after calling the list name `list_name[3]`
	- Index' can only be called using integers
	- You can also call them starting from the rear if you use a negative integer. For example, -1 will grab the final element in the list
- We can use the `.remove()` method to remove elements from lists using the element name.