---
tags:
  - Python
---
# Courses
1. [IBM Data Science Fundamentals with Python and SQL](https://www.coursera.org/programs/allegiant-giving-corporation-on-demand-learning-program-mjqmr/specializations/data-science-fundamentals-python-sql)
	1. [Python for Data Science, AI & Development](https://www.coursera.org/learn/python-for-applied-data-science-ai)

## Module 1 Cheatsheet: Python Basics

|Package/Method|Description|Code Example|
|---|---|---|
|Comments|Comments are lines of text that are ignored by the Python interpreter when executing the code<./td>|1. 1<br><br>1. `# This is a comment`<br><br> |
|Concatenation|Combines (concatenates) strings.|Syntax:<br><br>1. 1<br><br>1. `concatenated_string = string1 + string2` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `result = "Hello" + " John"</td>`<br><br> |
|Data Types|- Integer - Float - Boolean - String|Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br>8. 8<br>9. 9<br>10. 10<br><br>1. `x=7` <br>2. `# Integer Value` <br>3. `y=12.4` <br>4. `# Float Value` <br>5. `is_valid = True` <br>6. `# Boolean Value` <br>7. `is_valid = False` <br>8. `# Boolean Value` <br>9. `F_Name = "John"` <br>10. `# String Value`<br><br> |
|Indexing|Accesses character at a specific index.|Example:<br><br>1. 1<br>2. 2<br><br>1. `my_string="Hello"` <br>2. `char = my_string[0]`<br><br> |
|len()|Returns the length of a string.|Syntax:<br><br>1. 1<br><br>1. `len(string_name)` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `my_string="Hello"` <br>2. `length = len(my_string)`<br><br> |
|lower()|Converts string to lowercase.|Example:<br><br>1. 1<br>2. 2<br><br>1. `my_string="Hello"` <br>2. `uppercase_text = my_string.lower()`<br><br> |
|print()|Prints the message or variable inside `()`.|Example:<br><br>1. 1<br>2. 2<br><br>1. `print("Hello, world")` <br>2. `print(a+b)`<br><br> |
|Python Operators|- Addition (+): Adds two values together.  <br>- Subtraction (-): Subtracts one value from another.  <br>- Multiplication (*): Multiplies two values.  <br>- Division (/): Divides one value by another, returns a float.  <br>- Floor Division (//): Divides one value by another, returns the quotient as an integer.  <br>- Modulo (%): Returns the remainder after division.|Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br><br>1. `x = 9 y = 4` <br>2. `result_add= x + y # Addition` <br>3. `result_sub= x - y # Subtraction` <br>4. `result_mul= x * y # Multiplication` <br>5. `result_div= x / y # Division` <br>6. `result_fdiv= x // y # Floor Division` <br>7. `result_mod= x % y # Modulo`<br><br>|
| `replace()` | Replaces substrings. | Example:<br><br>1. 1<br>2. 2<br><br>1. `my_string="Hello"` <br>2. `new_text = my_string.replace("Hello", "Hi")`<br><br>|
| Slicing | Extracts a portion of the string. | Syntax:<br><br>1. 1<br><br>1. `substring = string_name[start:end]` <br><br><br><br>Example:<br><br>1. 1<br><br>1. `my_string="Hello" substring = my_string[0:5]`<br><br>|
|split()|Splits string into a list based on a delimiter.|Example:<br><br>1. 1<br>2. 2<br><br>1. `my_string="Hello"` <br>2. `split_text = my_string.split(",")`<br><br> |
|strip()|Removes leading/trailing whitespace.|Example:<br><br>1. 1<br>2. 2<br><br>1. `my_string="Hello"` <br>2. `trimmed = my_string.strip()`<br><br> |
|upper()|Converts string to uppercase.|Example:<br><br>1. 1<br>2. 2<br><br>1. `my_string="Hello"` <br>2. `uppercase_text = my_string.upper()`<br><br> |
|Variable Assignment|Assigns a value to a variable.|Syntax:<br><br>1. 1<br><br>1. `variable_name = value` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `name="John" # assigning John to variable name` <br>2. `x = 5 # assigning 5 to variable x`|

# Python Data Structures Cheat Sheet

## **List**

|Package/Method|Description|Code Example|
|---|---|---|
|append()|The `append()` method is used to add an element to the end of a list.|Syntax:<br><br>1. 1<br><br>1. `list_name.append(element)` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `fruits = ["apple", "banana", "orange"]` <br>2. `fruits.append("mango") print(fruits)`<br><br> |
|copy()|The `copy()` method is used to create a shallow copy of a list.|Example 1:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `my_list = [1, 2, 3, 4, 5]` <br>2. `new_list = my_list.copy() print(new_list)` <br>3. `# Output: [1, 2, 3, 4, 5]`<br><br> |
|count()|The `count()` method is used to count the number of occurrences of a specific element in a list in Python.|Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `my_list = [1, 2, 2, 3, 4, 2, 5, 2]` <br>2. `count = my_list.count(2) print(count)` <br>3. `# Output: 4`<br><br> |
|Creating a list|A list is a built-in data type that represents an ordered and mutable collection of elements. Lists are enclosed in square brackets [] and elements are separated by commas.|Example:<br><br>1. 1<br><br>1. `fruits = ["apple", "banana", "orange", "mango"]`<br><br> |
|del|The `del` statement is used to remove an element from list. `del` statement removes the element at the specified index.|Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `my_list = [10, 20, 30, 40, 50]` <br>2. `del my_list[2] # Removes the element at index 2 print(my_list)` <br>3. `# Output: [10, 20, 40, 50]`<br><br> |
|extend()|The `extend()` method is used to add multiple elements to a list. It takes an iterable (such as another list, tuple, or string) and appends each element of the iterable to the original list.|Syntax:<br><br>1. 1<br><br>1. `list_name.extend(iterable)` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `fruits = ["apple", "banana", "orange"]` <br>2. `more_fruits = ["mango", "grape"]` <br>3. `fruits.extend(more_fruits)` <br>4. `print(fruits)`<br><br> |
|Indexing|Indexing in a list allows you to access individual elements by their position. In Python, indexing starts from 0 for the first element and goes up to `length_of_list - 1`.|Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br><br>1. `my_list = [10, 20, 30, 40, 50]` <br>2. `print(my_list[0])` <br>3. `# Output: 10 (accessing the first element)` <br>4. `print(my_list[-1])` <br>5. `# Output: 50 (accessing the last element using negative indexing)`<br><br> |
|insert()|The `insert()` method is used to insert an element.|Syntax:<br><br>1. 1<br><br>1. `list_name.insert(index, element)` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `my_list = [1, 2, 3, 4, 5]` <br>2. `my_list.insert(2, 6)` <br>3. `print(my_list)`<br><br> |
|Modifying a list|You can use indexing to modify or assign new values to specific elements in the list.|Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `my_list = [10, 20, 30, 40, 50]` <br>2. `my_list[1] = 25 # Modifying the second element` <br>3. `print(my_list)` <br>4. `# Output: [10, 25, 30, 40, 50]`<br><br> |
|pop()|`pop()` method is another way to remove an element from a list in Python. It removes and returns the element at the specified index. If you don't provide an index to the `pop()` method, it will remove and return the last element of the list by default|Example 1:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br><br>1. `my_list = [10, 20, 30, 40, 50]` <br>2. `removed_element = my_list.pop(2) # Removes and returns the element at index 2` <br>3. `print(removed_element)` <br>4. `# Output: 30` <br><br>6. `print(my_list)` <br>7. `# Output: [10, 20, 40, 50]` <br><br> <br><br>Example 2:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br><br>1. `my_list = [10, 20, 30, 40, 50]` <br>2. `removed_element = my_list.pop() # Removes and returns the last element` <br>3. `print(removed_element)` <br>4. `# Output: 50` <br><br>6. `print(my_list)` <br>7. `# Output: [10, 20, 30, 40]`<br><br> |
|remove()|To remove an element from a list. The `remove()` method removes the first occurrence of the specified value.|Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `my_list = [10, 20, 30, 40, 50]` <br>2. `my_list.remove(30) # Removes the element 30` <br>3. `print(my_list)` <br>4. `# Output: [10, 20, 40, 50]`<br><br> |
|reverse()|The `reverse()` method is used to reverse the order of elements in a list|Example 1:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `my_list = [1, 2, 3, 4, 5]` <br>2. `my_list.reverse() print(my_list)` <br>3. `# Output: [5, 4, 3, 2, 1]`<br><br> |
|Slicing|You can use slicing to access a range of elements from a list.|Syntax:<br><br>1. 1<br><br>1. `list_name[start:end:step]` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br>8. 8<br>9. 9<br>10. 10<br>11. 11<br>12. 12<br><br>1. `my_list = [1, 2, 3, 4, 5]` <br>2. `print(my_list[1:4])` <br>3. `# Output: [2, 3, 4] (elements from index 1 to 3)`<br><br>5. `print(my_list[:3])` <br>6. `# Output: [1, 2, 3] (elements from the beginning up to index 2)` <br><br>8. `print(my_list[2:])` <br>9. `# Output: [3, 4, 5] (elements from index 2 to the end)` <br><br>11. `print(my_list[::2])` <br>12. `# Output: [1, 3, 5] (every second element)`<br><br> |
|sort()|The `sort()` method is used to sort the elements of a list in ascending order. If you want to sort the list in descending order, you can pass the `reverse=True` argument to the `sort()` method.|Example 1:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `my_list = [5, 2, 8, 1, 9]` <br>2. `my_list.sort()` <br>3. `print(my_list)` <br>4. `# Output: [1, 2, 5, 8, 9]` <br><br> <br><br>Example 2:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `my_list = [5, 2, 8, 1, 9]` <br>2. `my_list.sort(reverse=True)` <br>3. `print(my_list)` <br>4. `# Output: [9, 8, 5, 2, 1]`<br><br> |

## **Dictionary**

|Package/Method|Description|Code Example|
|---|---|---|
|Accessing Values|You can access the values in a dictionary using their corresponding `keys`.|Syntax:<br><br>1. 1<br><br>1. `Value = dict_name["key_name"]` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `name = person["name"]` <br>2. `age = person["age"]`<br><br> |
|Add or modify|Inserts a new key-value pair into the dictionary. If the key already exists, the value will be updated; otherwise, a new entry is created.|Syntax:<br><br>1. 1<br><br>1. `dict_name[key] = value` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `person["Country"] = "USA" # A new entry will be created.` <br>2. `person["city"] = "Chicago" # Update the existing value for the same key`<br><br> |
|clear()|The `clear()` method empties the dictionary, removing all key-value pairs within it. After this operation, the dictionary is still accessible and can be used further.|Syntax:<br><br>1. 1<br><br>1. `dict_name.clear()` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `grades.clear()`<br><br> |
|copy()|Creates a shallow copy of the dictionary. The new dictionary contains the same key-value pairs as the original, but they remain distinct objects in memory.|Syntax:<br><br>1. 1<br><br>1. `new_dict = dict_name.copy()` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `new_person = person.copy()` <br>2. `new_person = dict(person) # another way to create a copy of dictionary`<br><br> |
|Creating a Dictionary|A dictionary is a built-in data type that represents a collection of key-value pairs. Dictionaries are enclosed in curly braces `{}`.|Example:<br><br>1. 1<br>2. 2<br><br>1. `dict_name = {} #Creates an empty dictionary` <br>2. `person = { "name": "John", "age": 30, "city": "New York"}`<br><br> |
|del|Removes the specified key-value pair from the dictionary. Raises a `KeyError` if the key does not exist.|Syntax:<br><br>1. 1<br><br>1. `del dict_name[key]` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `del person["Country"]`<br><br> |
|items()|Retrieves all key-value pairs as tuples and converts them into a list of tuples. Each tuple consists of a key and its corresponding value.|Syntax:<br><br>1. 1<br><br>1. `items_list = list(dict_name.items())` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `info = list(person.items())`<br><br> |
|key existence|You can check for the existence of a key in a dictionary using the `in` keyword|Example:<br><br>1. 1<br>2. 2<br><br>1. `if "name" in person:` <br>2.     `print("Name exists in the dictionary.")`<br><br> |
|keys()|Retrieves all keys from the dictionary and converts them into a list. Useful for iterating or processing keys using list methods.|Syntax:<br><br>1. 1<br><br>1. `keys_list = list(dict_name.keys())` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `person_keys = list(person.keys())`<br><br> |
|update()|The `update()` method merges the provided dictionary into the existing dictionary, adding or updating key-value pairs.|Syntax:<br><br>1. 1<br><br>1. `dict_name.update({key: value})` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `person.update({"Profession": "Doctor"})`<br><br> |
|values()|Extracts all values from the dictionary and converts them into a list. This list can be used for further processing or analysis.|Syntax:<br><br>1. 1<br><br>1. `values_list = list(dict_name.values())` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `person_values = list(person.values())`<br><br> |

## **Sets**

|Package/Method|Description|Code Example|
|---|---|---|
|add()|Elements can be added to a set using the `add()` method. Duplicates are automatically removed, as sets only store unique values.|Syntax:<br><br>1. 1<br><br>1. `set_name.add(element)` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `fruits.add("mango")`<br><br> |
|clear()|The `clear()` method removes all elements from the set, resulting in an empty set. It updates the set in-place.|Syntax:<br><br>1. 1<br><br>1. `set_name.clear()` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `fruits.clear()`<br><br> |
|copy()|The `copy()` method creates a shallow copy of the set. Any modifications to the copy won't affect the original set.|Syntax:<br><br>1. 1<br><br>1. `new_set = set_name.copy()` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `new_fruits = fruits.copy()`<br><br> |
|Defining Sets|A set is an unordered collection of unique elements. Sets are enclosed in curly braces `{}`. They are useful for storing distinct values and performing set operations.|Example:<br><br>1. 1<br>2. 2<br><br>1. `empty_set = set() #Creating an Empty Set` <br>2. `fruits = {"apple", "banana", "orange"}`<br><br> |
|discard()|Use the `discard()` method to remove a specific element from the set. Ignores if the element is not found.|Syntax:<br><br>1. 1<br><br>1. `set_name.discard(element)` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `fruits.discard("apple")`<br><br> |
|issubset()|The `issubset()` method checks if the current set is a subset of another set. It returns True if all elements of the current set are present in the other set, otherwise False.|Syntax:<br><br>1. 1<br><br>1. `is_subset = set1.issubset(set2)` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `is_subset = fruits.issubset(colors)`<br><br> |
|issuperset()|The `issuperset()` method checks if the current set is a superset of another set. It returns True if all elements of the other set are present in the current set, otherwise False.|Syntax:<br><br>1. 1<br><br>1. `is_superset = set1.issuperset(set2)` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `is_superset = colors.issuperset(fruits)`<br><br> |
|pop()|The `pop()` method removes and returns an arbitrary element from the set. It raises a `KeyError` if the set is empty. Use this method to remove elements when the order doesn't matter.|Syntax:<br><br>1. 1<br><br>1. `removed_element = set_name.pop()` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `removed_fruit = fruits.pop()`<br><br> |
|remove()|Use the `remove()` method to remove a specific element from the set. Raises a `KeyError` if the element is not found.|Syntax:<br><br>1. 1<br><br>1. `set_name.remove(element)` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `fruits.remove("banana")`<br><br> |
|Set Operations|Perform various operations on sets: `union`, `intersection`, `difference`, `symmetric difference`.|Syntax:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `union_set = set1.union(set2)`<br>2. `intersection_set = set1.intersection(set2)` <br>3. `difference_set = set1.difference(set2)` <br>4. `sym_diff_set = set1.symmetric_difference(set2)`<br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `combined = fruits.union(colors)` <br>2. `common = fruits.intersection(colors)` <br>3. `unique_to_fruits = fruits.difference(colors)` <br>4. `sym_diff = fruits.symmetric_difference(colors)`<br><br> |
|update()|The `update()` method adds elements from another iterable into the set. It maintains the uniqueness of elements.|Syntax:<br><br>1. 1<br><br>1. `set_name.update(iterable)` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `fruits.update(["kiwi", "grape"]`|

## 1. Comparison Operations

Comparison operations are essential in programming. They help us compare values and make decisions based on the results.

### Equality Operator

The equality operator `==` checks if two values are equal. For example, in Python:

``` Python
age = 25

if age == 25:
	print("You are 25 years old.")
```

Here, the code checks if the variable age is equal to 25 and prints a message if it is.

### inequality

The inequality operator (!=) checks if two values are not equal:

```Python
if age != 30:
	print("You are not 30 years old.")
```

Here, the code checks if the variable age is not equal to 30 and prints a message if it is.

### Greater Than and Less Than

You can also compare if one value is greater than another.

```Python
if age>= 20:
	print("Yes, the Age is greater than 20")
```

Here, the code checks if the variable age is greater than equal to 30 and prints a message if it is.

### 2. Branching

Branching is like making decisions in your program based on conditions. Think of it as real-life choices.

#### The IF Statement

Consider a real-life scenario: entering a bar. If you’re above a certain age, you can enter; otherwise, you cannot.

```Python
age = 20
if age >= 21:
	print("You can enter the bar.")
else:
	print("Sorry, you cannot enter.")
```

Here, we use the if statement to make a decision based on the age variable.

#### The ELIF Statement

Sometimes, there are multiple conditions to check. For example, if you’re not old enough for the bar, you can go to a movie instead.

```Python
if age >= 21:
	print("You can enter the bar.")
elif age >= 18:
	print("You can watch a movie.")
else:
	print("Sorry, you cannot do either.")
```
 
##### Real-life example: Automated Teller Machine (ATM)

When a user interacts with an ATM, the software in the ATM can use branching to make decisions based on the user’s input. For example, if the user selects “Withdraw Cash,” the ATM can branch into different denominations of bills to dispense based on the amount requested.

```Python
user_choice = "Withdraw Cash"

if user_choice == "Withdraw Cash":
	amount = input("Enter the amount to withdraw: ")
	if amount % 10 == 0:
		dispense_cash(amount)
	else:
		print("Please enter a multiple of 10.")
else:
print("Thank you for using the ATM.")
```
 
### 3. Logical Operators

Logical operators help us combine and manipulate conditions.
#### The NOT Operator

##### Real-life example: Notification Settings

In a smartphone’s notification settings, you can use the NOT operator to control when to send notifications. For example, you might only want to receive notifications when your phone is not in “Do Not Disturb” mode.

The not operator negates a condition.

```Python
is_do_not_disturb = True

if not is_do_not_disturb:
	send_notification("New message received")
```
 
#### The AND Operator

##### Real-life example: Access Control

In a secure facility, you can use the AND operator to check multiple conditions for access. To open a high-security door, a person might need both a valid ID card and a matching fingerprint.  
The and operator checks if multiple conditions are all true. Like needing both keys to open a safe.

```Python
has_valid_id_card = True
has_matching_fingerprint = True

if has_valid_id_card and has_matching_fingerprint:
	open_high_security_door()
```
 
#### The OR Operator

##### Real-life example: Movie Night Decision

When planning a movie night with friends, you can use the OR operator to decide on a movie genre. You’ll choose a movie if at least one person is interested.

The or operator checks if at least one condition is true. It’s like choosing between different movies to watch.

```Python
friend1_likes_comedy = True
friend2_likes_action = False
friend3_likes_drama = False

if friend1_likes_comedy or friend2_likes_action or friend3_likes_drama:
	choose a movie()
```

# What is a Loop?

In programming, a loop is like a magic trick that allows a computer to do something over and over again. Imagine you are a magician's assistant, and your magician friend asks you to pull a rabbit out of a hat, but not just once - they want you to keep doing it until they tell you to stop. That is what loops do for computers - they repeat a set of instructions as many times as needed.

# How Loop works?

Here's how it works in Python:

![For loop flowchart](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%203/images/forloop.png)

- **Start:** The for loop begins with the keyword for, followed by a variable that will take on each value in a sequence.
    
- **Condition:** After the variable, you specify the keyword in and a sequence, such as a list or a range, that the loop will iterate through.
    
- If **Condition True**:
    

1. The loop takes the first value from the sequence and assigns it to the variable.
2. The indented block of code following the loop header is executed using this value.
3. The loop then moves to the next value in the sequence and repeats the process until all values have been used.

- **Statement:** Inside the indented block of the loop, you write the statements that you want to repeat for each value in the sequence.
    
- **Repeat:** The loop continues to repeat the block of code for each value in the sequence until there are no more values left.
    
- If **Condition False**:
    

1. Once all values in the sequence have been processed, the loop terminates automatically.
2. The loop completes its execution, and the program continues to the next statement after the loop.

---

### The Need for Loops

Think about when you need to count from 1 to 10. Doing it manually is easy, but what if you had to count to a **million**? Typing all those numbers one by one would be a nightmare! This is where loops come in handy. They help computers repeat tasks quickly and accurately without getting tired.

## Main Types of Loops

### For Loops

For loops are like a superhero's checklist. A for loop in programming is a control structure that allows the repeated execution of a set of statements for each item in a sequence, such as elements in a list or numbers in a range, enabling efficient iteration and automation of tasks

##### Syntax of for loop

1. 1
2. 2

1. `for val in sequence:`
2.       `# statement(s) to be executed in sequence as a part of the loop.`

 

Here is an example of For loop.

Imagine you're a painter, and you want to paint a beautiful rainbow with seven colors. Instead of picking up each color one by one and painting the rainbow, you could tell a magical painter's assistant to do it for you. This is what a basic for loop does in programming.

##### We have a list of colours.

1. 1

1. `colors = ["red", "orange", "yellow", "green", "blue", "indigo", "violet"]`

 

##### Let's print the colour name in the new line using for loop.

1. 1
2. 2

1. `for color in colors:`
2.     `print(color)`

 

In this example, the for loop picks each color from the colors list and prints it on the screen. You don't have to write the same code for each color - the loop does it automatically!

---

Sometimes you do not want to paint a rainbow, but _you want to count the number of steps to reach your goal._ A range-based for loop is like having a friendly step counter that helps you reach your target.  
Here is how you might use a for loop to count from 1 to 10:

1. 1
2. 2

1. `for number in range(1, 11):`
2.     `print(number)`

 

Here, the **range(1, 11)** generates a sequence from 1 to 10, and the for loop goes through each number in that sequence, printing it out. It's like taking 10 steps, and you're guided by the loop!

#### Range Function

The range function in Python generates an ordered sequence that can be used in loops. It takes one or two arguments:

- If given one argument (e.g., range(11)), it generates a sequence starting from 0 up to (but not including) the given number.

1. 1
2. 2

1. `for number in range(11):`
2.     `print(number)`

 

- If given two arguments (e.g., range(1, 11)), it generates a sequence starting from the first argument up to (but not including) the second argument.

1. 1
2. 2

1. `for number in range(1, 11):`
2.     `print(number)`

 

#### The Enumerated For Loop

Have you ever needed to keep track of both the item and its position in a list? An enumerated for loop comes to your rescue. It's like having a personal assistant who not only hands you the item but also tells you where to find it.

Consider this example:

1. 1
2. 2
3. 3

1. `fruits = ["apple", "banana", "orange"]`
2. `for index, fruit in enumerate(fruits):`
3.     `print(f"At position {index}, I found a {fruit}")`

 

With this loop, you not only get the fruit but also its position in the list. It's as if you have a magical guide pointing out each fruit's location!

### While Loops

While loops are like a sleepless night at a friend's sleepover. Imagine you and your friends keep telling ghost stories until someone decides it's time to sleep. As long as no one says, "Let's sleep" you keep telling stories.  
A while loop works similarly - it repeats a task as long as a certain condition is true. It's like saying, "Hey computer, keep doing this until I say stop!"

##### Basic syntax of While Loop.

1. 1
2. 2
3. 3

1. `while condition:`
2.     `# Code to be executed while the condition is true`
3.     `# Indentation is crucial to indicate the scope of the loop`

 

For example, here's how you might use a while loop to count from 1 to 10:

1. 1
2. 2
3. 3
4. 4

1. `count = 1`
2. `while count <= 10:`
3.     `print(count)`
4.     `count += 1`

 

here's a breakdown of the above code.

1. There is a variable named **count** initialized with the value 1.
    
2. The while loop is used to repeatedly execute a block of code as long as a given condition is True. In this case, the condition is **count <= 10**, meaning the loop will continue as long as count is less than or equal to 10.
    
3. Inside the loop:
    
    - The **print(count)** statement outputs the current value of the count variable.
        
    - The **count += 1** statement increments the value of count by 1. This step ensures that the loop will eventually terminate when count becomes greater than 10.
        
4. The loop will continue executing as long as the condition count <= 10 is satisfied.
    
5. The loop will print the numbers 1 to 10 in consecutive order since the print statement is inside the loop block and executed during each iteration.
    
6. Once count reaches 11, the condition count <= 10 will evaluate to False, and the loop will terminate.
    
7. The output of the code will be the numbers 1 to 10, each printed on a separate line.
    

### The Loop Flow

Both for and while loops have their special moves, but they follow a pattern:

- **Initialization:** You set up things like a starting point or conditions.
    
- **Condition:** You decide when the loop should keep going and when it should stop.
    
- **Execution:** You do the task inside the loop.
    
- **Update:** You make changes to your starting point or conditions to move forward.
    
- **Repeat:** The loop goes back to step 2 until the condition is no longer true.
### When to Use Each

**For Loops:** Use for loops when you know the number of iterations in advance and want to process each element in a sequence. They are best suited for iterating over collections and sequences where the length is known.

**While Loops:** Use while loops when you need to perform a task repeatedly as long as a certain condition holds true. While loops are particularly useful for situations where the number of iterations is uncertain or where you're waiting for a specific condition to be met.

# Introduction to functions

A function is a fundamental building block that encapsulates specific actions or computations. As in mathematics, where functions take inputs and produce outputs, programming functions perform similarly. They take inputs, execute predefined actions or calculations, and then return an output.

## Purpose of functions

Functions promote code modularity and reusability. Imagine you have a task that needs to be performed multiple times within a program. Instead of duplicating the same code at various places, you can define a function once and call it whenever you need that task. This reduces redundancy and makes the code easier to manage and maintain.

## Benefits of using functions

**Modularity:** Functions break down complex tasks into manageable components  
**Reusability:** Functions can be used multiple times without rewriting code  
**Readability:** Functions with meaningful names enhance code understanding  
**Debugging:** Isolating functions eases troubleshooting and issue fixing  
**Abstraction:** Functions simplify complex processes behind a user-friendly interface  
**Collaboration:** Team members can work on different functions concurrently  
**Maintenance:** Changes made in a function automatically apply wherever it's used

## How functions take inputs, perform tasks, and produce outputs

### Inputs (Parameters)

Functions operate on data, and they can receive data as input. These inputs are known as _parameters_ or _arguments_. Parameters provide functions with the necessary information they need to perform their tasks. Consider parameters as values you pass to a function, allowing it to work with specific data.

### Performing tasks

Once a function receives its input (parameters), it executes predefined actions or computations. These actions can include calculations, operations on data, or even more complex tasks. The purpose of a function determines the tasks it performs. For instance, a function could calculate the sum of numbers, sort a list, format text, or fetch data from a database.

### Producing outputs

After performing its tasks, a function can produce an output. This output is the result of the operations carried out within the function. It's the value that the function “returns” to the code that called it. Think of the output as the end product of the function's work. You can use this output in your code, assign it to variables, pass it to other functions, or even print it out for display.

Example:

Consider a function named `calculate_total` that takes two numbers as input (parameters), adds them together, and then produces the sum as the output. Here's how it works:


1. `def calculate_total(a, b):  # Parameters: a and b`
2.     `total = a + b           # Task: Addition`
3.     `return total            # Output: Sum of a and b`

5. `result = calculate_total(5, 7)  # Calling the function with inputs 5 and 7`
6. `print(result)  # Output: 12`

## Python's built-in functions

Python has a rich set of built-in functions that provide a wide range of functionalities. These functions are readily available for you to use, and you don't need to be concerned about how they are implemented internally. Instead, you can focus on understanding what each function does and how to use it effectively.

### Using built-in functions or Pre-defined functions

To use a built-in function, you simply call the function's name followed by parentheses. Any required arguments or parameters are passed into the function within these parentheses. The function then performs its predefined task and may return an output you can use in your code.

Here are a few examples of commonly used built-in functions:

**len():** Calculates the length of a sequence or collection

1. `string_length = len("Hello, World!")  # Output: 13`
2. `list_length = len([1, 2, 3, 4, 5])   # Output: 5`


**sum():** Adds up the elements in an iterable (list, tuple, and so on)

1. `total = sum([10, 20, 30, 40, 50])  # Output: 150`

**max():** Returns the maximum value in an iterable

1. `highest = max([5, 12, 8, 23, 16])  # Output: 23`

**min():** Returns the minimum value in an iterable

1. `lowest = min([5, 12, 8, 23, 16])  # Output: 5`

Python's built-in functions offer a wide array of functionalities, from basic operations like len() and sum() to more specialized tasks.

## Defining your functions

Defining a function is like creating your mini-program:

1. Use `def` followed by the function name and parentheses

Here is the syntax to define a function:

1. 1
2. 2

1. `def function_name():`
2.     `pass`

A `"pass"` statement in a programming function is a placeholder or a no-op (no operation) statement. Use it when you want to define a function or a code block syntactically but do not want to specify any functionality or implementation at that moment.

- **Placeholder:** `"pass"` acts as a temporary placeholder for future code that you intend to write within a function or a code block.
    
- **Syntax Requirement:** In many programming languages like Python, using `"pass"` is necessary when you define a function or a conditional block. It ensures that the code remains syntactically correct, even if it doesn't do anything yet.
    
- **No Operation:** `"pass"` itself doesn't perform any meaningful action. When the interpreter encounters “pass”, it simply moves on to the next statement without executing any code.

### Function Parameters:

- Parameters are like inputs for functions
- They go inside parentheses when defining the function
- Functions can have multiple parameters

Example:

1. `def greet(name):`
2.     `print("Hello, " + name)`

4. `result = greet("Alice")`
5. `print(result)  # Output: Hello, Alice`

### Docstrings (Documentation Strings)

- Docstrings explain what a function does
- Placed inside triple quotes under the function definition
- Helps other developers understand your function

Example:

1. `def multiply(a, b):`
2.     `"""`
3.     `This function multiplies two numbers.`
4.     `Input: a (number), b (number)`
5.     `Output: Product of a and b`
6.     `"""`
7.     `print(a * b)`
8. `multiply(2,6)`

### Return statement

- Return gives back a value from a function
- Ends the function's execution and sends the result
- A function can return various types of data

Example:

1. `def add(a, b):`
2.     `return a + b`

4. `sum_result = add(3, 5)  # sum_result gets the value 8`

### Understanding scopes and variables

Scope is where a variable can be seen and used:

- **Global Scope:** Variables defined outside functions; accessible everywhere
- **Local Scope:** Variables inside functions; only usable within that function

### Part 1: Global variable declaration

1. `global_variable = "I'm global"`

This line initializes a global variable called `global_variable` and assigns it the value "I'm global".

> Global variables are accessible throughout the entire program, both inside and outside functions.

### Part 2: Function definition

1. `def example_function():`
2.     `local_variable = "I'm local"`
3.     `print(global_variable)  # Accessing global variable`
4.     `print(local_variable)   # Accessing local variable`

Here, you define a function called `example_function()`.

Within this function:

- A local variable named local_variable is declared and initialized with the string value "I'm local." This variable is local to the function and can only be accessed within the function's scope.
    
- The function then prints the values of both the **global variable (global_variable) and the local variable (local_variable)**. It demonstrates that you can access global and local variables within a function.
### Part 3: Function call

1. `example_function()`

In this part, you call the `example_function()` by invoking it. This results in the function's code being executed.  
As a result of this function call, it will print the values of the global and local variables within the function.

### Part 4: Accessing global variable outside the function

1. `print(global_variable)  # Accessible outside the function`

After calling the function, you print the value of the global variable `global_variable` outside the function. **This demonstrates that global variables are accessible inside and outside of functions.**

### Part 5: Attempting to access local variable outside the function

1. `# print(local_variable)  # Error, local variable not visible here`

In this part, you are attempting to print the value of the local variable `local_variable` outside of the function. However, this line would result in an error.

> Local variables are only visible and accessible within the scope of the function where they are defined.

Attempting to access them outside of that scope would raise a `"NameError"`.

## Using functions with loops

### Functions and loops together

1. Functions can contain code with loops
2. This makes complex tasks more organized
3. The loop code becomes a repeatable function

Example:

1. `def print_numbers(limit):`
2.     `for i in range(1, limit+1):`
3.         `print(i)`

5. `print_numbers(5)  # Output: 1 2 3 4 5`

### Enhancing code organization and reusability

1. Functions group similar actions for easy understanding
2. Looping within functions keeps code clean
3. You can reuse a function to repeat actions

Example

1. `def greet(name):`
2.     `return "Hello, " + name`

4. `for _ in range(3):`
5.     `print(greet("Alice"))`

## Modifying data structure using functions

You'll use Python and a list as the data structure for this illustration. In this example, you will create functions to add and remove elements from a list.

### Part 1: Initialize an empty list

1. `# Define an empty list as the initial data structure`
2. `my_list = []`

In this part, you start by creating an empty list named `my_list`. This empty list serves as the data structure that you will modify throughout the code.

### Part 2: Define a function to add elements

1. `# Function to add an element to the list`
2. `def add_element(data_structure, element):`
3.     `data_structure.append(element)`

Here, you define a function called `add_element`. This function takes two parameters:

- `data_structure`: This parameter represents the list to which you want to add an element
- `element`: This parameter represents the element you want to add to the list

Inside the function, you use the `append` method to add the provided element to the data_structure, which is assumed to be a list.

### Part 3: Define a function to remove elements

1. `# Function to remove an element from the list`
2. `def remove_element(data_structure, element):`
3.     `if element in data_structure:`
4.         `data_structure.remove(element)`
5.     `else:`
6.         `print(f"{element} not found in the list.")`

In this part, you define another function called `remove_element`. It also takes two parameters:

- `data_structure`: The list from which we want to remove an element
- `element`: The element we want to remove from the list

Inside the function, you use conditional statements to check if the element is present in the data_structure. If it is, you use the `remove` method to remove the first occurrence of the element. If it's not found, you print a message indicating that the element was not found in the list.

### Part 4: Add elements to the list

1. `# Add elements to the list using the add_element function`
2. `add_element(my_list, 42)`
3. `add_element(my_list, 17)`
4. `add_element(my_list, 99)`

Here, you use the `add_element` function to add three elements (42, 17, and 99) to the `my_list`. These are added one at a time using function calls.

### Part 5: Print the current list

1. `# Print the current list`
2. `print("Current list:", my_list)`

This part simply prints the current state of the `my_list` to the console, allowing us to see the elements that have been added so far.

### Part 6: Remove elements from the list

1. `# Remove an element from the list using the remove_element function`
2. `remove_element(my_list, 17)`
3. `remove_element(my_list, 55)  # This will print a message since 55 is not in the list`

In this part, you use the `remove_element` function to remove elements from the my_list. First, you attempt to remove 17 (which is in the list), and then you try to remove 55 (which is not in the list). **The second call to `remove_element` will print a message indicating that 55 was not found.**

### Part 7: Print the updated list

1. `# Print the updated list`
2. `print("Updated list:", my_list)`

Finally, you print the updated `my_list` to the console. This allows us to observe the modifications made to the list by adding and removing elements using the defined functions.

## What are exceptions?

**Exceptions** are alerts when something unexpected happens while running a program. It could be a mistake in the code or a situation that was not planned for. Python can raise these alerts automatically, but we can also trigger them on purpose using the raise command. The cool part is that we can prevent our program from crashing by handling exceptions.

## Errors vs. Exceptions

Hold on, what is the difference between errors and exceptions? Well, `errors` are usually big problems that come from the computer or the system. They often make the program stop working completely. On the other hand, `exceptions` are more like issues we can control. They happen because of something we did in our code and can usually be fixed, so the program keeps going.

---

Here is the difference between `Errors and exceptions`:-

|Aspect|Errors|Exceptions|
|---|---|---|
|**Origin**|Errors are typically caused by the environment, hardware, or operating system. | Exceptions are usually a result of problematic code execution within the program.|
|**Nature**|Errors are often severe and can lead to program crashes or abnormal termination. | Exceptions are generally less severe and can be caught and handled to prevent program termination.|
|**Handling**|Errors are not usually caught or handled by the program itself. | Exceptions can be caught using try-except blocks and dealt with gracefully, allowing the program to continue execution.|
|**Examples**|Examples include “SyntaxError” due to incorrect syntax or “NameError” when a variable is not defined.|Examples include “ZeroDivisionError” when dividing by zero, or “FileNotFoundError” when attempting to open a non-existent file.|
|**Categorization**|Errors are not classified into categories.|Exceptions are categorized into various classes, such as “ArithmeticError”, “IOError”, "ValueError”, etc., based on their nature.|

## Common Exceptions in Python

Here are a few examples of exceptions we often run into and can handle using this tool:

- **ZeroDivisionError:** This error arises when an attempt is made to divide a number by zero. Division by zero is undefined in mathematics, causing an arithmetic error. For instance:  
    For example:

1. `result = 10 / 0` 
2. `print(result)`
3. `# Raises ZeroDivisionError`

- **ValueError:** This error occurs when an inappropriate value is used within the code. An example of this is when trying to convert a non-numeric string to an integer:  
    For example:

1. `num = int("abc")`
2. `# Raises ValueError`

- **FileNotFoundError:** This exception is encountered when an attempt is made to access a file that does not exist.  
    For example:

1. `with open("nonexistent_file.txt", "r") as file:`
2.         `content = file.read()   # Raises FileNotFoundError`

- **IndexError:** An IndexError occurs when an index is used to access an element in a list that is outside the valid index range.  
    For example:

1. `my_list = [1, 2, 3]`
2. `value = my_list[1]  # No IndexError, within range`
3. `missing = my_list[5]  # Raises IndexError`

- **KeyError:** The KeyError arises when an attempt is made to access a non-existent key in a dictionary.  
    For example:

1. `my_dict = {"name": "Alice", "age": 30}`
2. `value = my_dict.get("city")  # No KeyError, using .get() method`
3. `missing = my_dict["city"]  # Raises KeyError`

- **TypeError:** The TypeError occurs when an object is used in an incompatible manner. An example includes trying to concatenate a string and an integer:  
    For example:

1. `result = "hello" + 5`   
2. `# Raises TypeError`

- **AttributeError:** An AttributeError occurs when an attribute or method is accessed on an object that doesn't possess that specific attribute or method. For instance:  
    For example:

1. `text = "example"`
2. `length = len(text)  # No AttributeError, correct method usage`
3. `missing = text.some_method()  # Raises AttributeError`

- **ImportError:** This error is encountered when an attempt is made to import a module that is unavailable. For example: `import non_existent_module`

---

> Note: **Please remember, the exceptions you will encounter are not limited to just these. There are many more in Python. However, there is no need to worry. By using the technique provided below and following the correct syntax, you will be able to handle any exceptions that come your way.**

---

## Handling Exceptions:

Python has a handy tool called `try and except` that helps us manage exceptions.

**Try and Except** : You can use the try and except blocks to prevent your program from crashing due to exceptions.

Here's how they work:

1. The code that may result in an exception is contained in the try block.
2. If an exception occurs, the code directly jumps to except block.
3. In the except block, you can define how to handle the exception gracefully, like displaying an error message or taking alternative actions.
4. After the except block, the program continues executing the remaining code.

### Example: Attempting to divide by zero

1. `# using Try- except` 
2. `try:`
3.     `# Attempting to divide 10 by 0`
4.     `result = 10 / 0`
5. `except ZeroDivisionError:`
6.     `# Handling the ZeroDivisionError and printing an error message`
7.     `print("Error: Cannot divide by zero")`
8. `# This line will be executed regardless of whether an exception occurred`
9. `print("outside of try and except block")`

# Introduction to Classes and object

Python is an object-oriented programming (OOP) language, which means it uses a paradigm centered around objects and classes. Here's an explanation of these fundamental concepts:

## Classes:

A class is a blueprint or template for creating objects. It defines the structure and behavior that its objects will have.

Think of a class as a cookie cutter, and objects as the cookies cut from that template.

In Python, classes are created using the `class` keyword.

### Creating Classes:

When you create a class, you specify the `attributes`(data) and `methods` (functions) that objects of that class will have.  
`Attributes` are defined as variables within the class, and `methods` are defined as functions.  
For example,you can design a "Car" class with attributes such as "color" and "speed," along with methods like "accelerate."

## Objects:

An _object_ is a fundamental unit in Python that represents a real-world entity or concept.  
Objects can be tangible (like a car) or abstract (like a student's grade).

_Every object has two main characteristics:_

### State:

The _attributes or data_ that describe the object. For our "Car" object, this might include attributes like "color", "speed", and "fuel level".

### Behavior:

The _actions or methods_ that the object can perform. In Python, methods are functions that belong to objects and can change the object's state or perform specific operations.

### Instantiating Objects:

- Once you've defined a class, you can create individual objects (instances) based on that class.
- Each object is independent and has its own set of attributes and methods.
- To create an object, you use the class name followed by parentheses, so: "my_car = Car()"

### Interacting with Objects:

You interact with objects by calling their methods or accessing their attributes using dot notation.

For example, if you have a Car object named **my_car**, you can set its color with **my_car.color = "blue"** and accelerate it with **my_car.accelerate()** if there's an accelerate method defined in the class.

## Structure of classes and object code

> Please don't directly copy and use this code as it's meant as a template for explanation and isn't tailored for specific results.

### Class Declaration (class ClassName):

- The class keyword is used to declare a class in Python.
- ClassName is the name of the class, typically following CamelCase naming conventions.

1. `class ClassName:`

### Class Attributes (class_attribute = value):

- Class attributes are variables that are shared among all instances (objects) of the class.
- They are defined within the class but outside of any methods.

1. `class ClassName:`
2.     `# Class attributes (shared by all instances)`
3.     `class_attribute = value`

### Constructor Method (def **init**(self, attribute1, attribute2, …):):

- The `__init__` method is a special method known as the constructor.
- It initializes the **instance attributes** (also called instance variables) when an object is created.
- The `self` parameter is the first parameter of the constructor, referring to the instance being created.
- **attribute1**, **attribute2**, and so on are parameters passed to the constructor when creating an object.
- Inside the constructor, `self.attribute1`, `self.attribute2`, and so on are used to assign values to instance attributes.

1. `class ClassName:`
2.     `# Class attributes (shared by all instances)`
3.     `class_attribute = value`

5.     `# Constructor method (initialize instance attributes)`
6.     `def __init__(self, attribute1, attribute2, ...):`
7.         `pass`
8.         `# ...`

### Instance Attributes (self.attribute1 = attribute1):

- Instance attributes are variables that store data specific to each instance of the class.
- They are initialized within the **init** method using the self keyword followed by the attribute name.
- These attributes hold unique data for each object created from the class.

1. `class ClassName:`
2.     `# Class attributes (shared by all instances)`
3.     `class_attribute = value`

5.     `# Constructor method (initialize instance attributes)`
6.     `def __init__(self, attribute1, attribute2, ...):`
7.         `self.attribute1 = attribute1`
8.         `self.attribute2 = attribute2`
9.         `# ...`

### Instance Methods (def method1(self, parameter1, parameter2, …):):

- Instance methods are functions defined within the class.
- They operate on the instance's data (instance attributes) and can perform actions specific to instances.
- The **self** parameter is required in instance methods, allowing them to access instance attributes and call other methods within the class.

1. `class ClassName:`
2.     `# Class attributes (shared by all instances)`
3.     `class_attribute = value`

5.     `# Constructor method (initialize instance attributes)`
6.     `def __init__(self, attribute1, attribute2, ...):`
7.         `self.attribute1 = attribute1`
8.         `self.attribute2 = attribute2`
9.         `# ...`

11.     `# Instance methods (functions)`
12.     `def method1(self, parameter1, parameter2, ...):`
13.         `# Method logic`
14.         `pass`

> Using same steps you can define multiple instance methods.

1. `class ClassName:`
2.     `# Class attributes (shared by all instances)`
3.     `class_attribute = value`

5.     `# Constructor method (initialize instance attributes)`
6.     `def __init__(self, attribute1, attribute2, ...):`
7.         `self.attribute1 = attribute1`
8.         `self.attribute2 = attribute2`
9.         `# ...`

11.     `# Instance methods (functions)`
12.     `def method1(self, parameter1, parameter2, ...):`
13.         `# Method logic`
14.         `pass`

16.     `def method2(self, parameter1, parameter2, ...):`
17.         `# Method logic`
18.         `pass`

 

> Note:- Now, we have successfully created a dummy class.

#### Creating Objects (Instances):

- To create objects (instances) of the class, you call the class like a function and provide arguments required by the constructor.
- Each object is a distinct instance of the class, with its own set of instance attributes and the ability to call methods defined in the class.

1. 1
2. 2
3. 3

1. `# Create objects (instances) of the class`
2. `object1 = ClassName(arg1, arg2, ...)`
3. `object2 = ClassName(arg1, arg2, ...)`

 

#### Calling methods on objects:

- In this section we will call methods on objects, specifically `object1` and `object2`.
- The methods **method1** and **method2** are defined in the ClassName **class**, and you're calling them on **object1** and **object2** respectively.
- You pass values **param1_value** and **param2_value** as arguments to these methods. These arguments are used within the method's logic.

#### Method 1: Using dot notation:

- This is the most straightforward way to call an object's method. In this we use the dot notation **(object.method())** to directly invoke the method on the object.
- For example, `result1 = object1.method1(param1_value, param2_value, ...)` calls method1 on object1.

1. 1
2. 2
3. 3
4. 4

1. `# Calling methods on objects`
2. `# Method 1: Using dot notation`
3. `result1 = object1.method1(param1_value, param2_value, ...)`
4. `result2 = object2.method2(param1_value, param2_value, ...)`

 

#### Method 2: Assigning object methods to variables:

- Here's an alternative way to call an object's method by assigning the method reference to a variable.
- `method_reference = object1.method1` assigns the method **method1** of **object1** to the variable **method_reference**.
- Later, we call the method using the variable like this: **result3 = method_reference(param1_value, param2_value, …)**.

1. 1
2. 2
3. 3

1. `# Method 2: Assigning object methods to variables`
2. `method_reference = object1.method1  # Assign the method to a variable`
3. `result3 = method_reference(param1_value, param2_value, ...)`

 

#### Accessing object attributes:

- Here, we are accessing an object's attribute using dot notation.
- `attribute_value = object1.attribute1` retrieves the value of the attribute **attribute1** from **object1** and assigns it to the variable **attribute_value**.

1. 1
2. 2

1. `# Accessing object attributes`
2. `attribute_value = object1.attribute1  # Access the attribute using dot notation`

 

#### Modifying object attributes:

- We are modifying an object's attribute using dot notation.
- `object1.attribute2 = new_value` sets the attribute **attribute2** of **object1** to the new value **new_value**.

1. 1
2. 2

1. `# Modifying object attributes`
2. `object1.attribute2 = new_value  # Change the value of an attribute using dot notation`

 

#### Accessing class attributes (shared by all instances):

- Finally,we access a class attribute, which is shared by all instances of the class.
- `class_attr_value = ClassName.class_attribute` accesses the class attribute `class_attribute` from the ClassName `class` and assigns its value to the variable  
    `class_attr_value`.

1. 1
2. 2

1. `# Accessing class attributes (shared by all instances)`
2. `class_attr_value = ClassName.class_attribute`

 

#### Real-world example

Let's write a python program that simulates a simple car class, allowing you to create car instances, accelerate them, and display their current speeds.

1. Let's start by defining a Car class that includes the following attributes and methods:

- Class attribute `max_speed`, which is set to **120 km/h**.
    
- Constructor method `__init__` that takes parameters for the **car's make, model, color, and an optional speed (defaulting to 0)**. This method initializes instance attributes for make, model, color, and speed.
    
- Method `accelerate(self, acceleration)` that allows the car to accelerate. If the acceleration does not exceed the `max_speed`, update the **car's speed** attribute. Otherwise, set the speed to the **max_speed**.
    
- Method `get_speed(self)` that returns the current speed of the car.
    

1. 1
2. 2
3. 3
4. 4
5. 5
6. 6
7. 7
8. 8
9. 9
10. 10
11. 11
12. 12
13. 13
14. 14
15. 15
16. 16
17. 17
18. 18
19. 19
20. 20
21. 21

1. `class Car:`
2.     `# Class attribute (shared by all instances)`
3.     `max_speed = 120  # Maximum speed in km/h`

5.     `# Constructor method (initialize instance attributes)`
6.     `def __init__(self, make, model, color, speed=0):`
7.         `self.make = make`
8.         `self.model = model`
9.         `self.color = color`
10.         `self.speed = speed  # Initial speed is set to 0`

12.     `# Method for accelerating the car`
13.     `def accelerate(self, acceleration):`
14.         `if self.speed + acceleration <= Car.max_speed:`
15.             `self.speed += acceleration`
16.         `else:`
17.             `self.speed = Car.max_speed`

19.     `# Method to get the current speed of the car`
20.     `def get_speed(self):`
21.         `return self.speed`

 

2. Now, we will instantiate two objects of the Car class, each with the following characteristics:

- car1: **Make = "Toyota", Model = "Camry", Color = "Blue"**
    
- car2: **Make = "Honda", Model = "Civic", Color = "Red"**
    

1. 1
2. 2
3. 3

1. `# Create objects (instances) of the Car class`
2. `car1 = Car("Toyota", "Camry", "Blue")`
3. `car2 = Car("Honda", "Civic", "Red")`

 

3. Using the `accelerate` method, we will increase the speed of car1 by 30 km/h and car2 by 20 km/h.

1. 1
2. 2
3. 3
4. 4

2. `# Accelerate the cars`
3. `car1.accelerate(30)`
4. `car2.accelerate(20)`

 

4. Lastly, we will display the current speed of each car by utilizing the `get_speed method.

1. 1
2. 2
3. 3
4. 4

2. `# Print the current speeds of the cars`
3. `print(f"{car1.make} {car1.model} is currently at {car1.get_speed()} km/h.")`
4. `print(f"{car2.make} {car2.model} is currently at {car2.get_speed()} km/h.")`

## Python Programming Fundamentals Cheat Sheet

|Package/Method|Description|Syntax and Code Example|
|---|---|---|
|AND|Returns `True` if both statement1 and statement2 are `True`. Otherwise, returns `False`.|Syntax:<br><br><br><br>1. `statement1 and statement2` <br><br> <br><br>Example:<br><br>1. `marks = 90`<br>2. `attendance_percentage = 87`<br><br>4. `if marks >= 80 and attendance_percentage >= 85:`<br>5.     `print("qualify for honors")`<br>6. `else:`<br>7.     `print("Not qualified for honors")`<br><br>9. `# Output = qualify for honors`<br><br> |
|Class Definition|Defines a blueprint for creating objects and defining their attributes and behaviors.|Syntax:<br><br>1. 1<br><br>1. `class ClassName: # Class attributes and methods` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `class Person:` <br>2.     `def __init__(self, name, age):` <br>3.         `self.name = name` <br>4.         `self.age = age`<br><br> |
|Define Function|A `function` is a reusable block of code that performs a specific task or set of tasks when called.|Syntax:<br><br>1. 1<br><br>1. `def function_name(parameters): # Function body` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `def greet(name): print("Hello,", name)`<br><br> |
|Equal(`==`)|Checks if two values are equal.|Syntax:<br><br>1. `variable1 == variable2` <br><br> <br><br>Example 1:<br><br>1. `5 == 5` <br><br>returns True<br><br>Example 2:<br><br>1. `age = 25 age == 30` <br><br> <br><br>returns False|
|For Loop|A `for` loop repeatedly executes a block of code for a specified number of iterations or over a sequence of elements (list, range, string, etc.).|Syntax:<br><br>1. `for variable in sequence: # Code to repeat` <br><br> <br><br>Example 1:<br><br>1. `for num in range(1, 10):` <br>2.     `print(num)` <br><br> <br><br>Example 2:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `fruits = ["apple", "banana", "orange", "grape", "kiwi"]` <br>2. `for fruit in fruits:`<br>3.     `print(fruit)`<br><br> |
|Function Call|A function call is the act of executing the code within the function using the provided arguments.|Syntax:<br><br>1. 1<br><br>1. `function_name(arguments)` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `greet("Alice")`<br><br> |
|Greater Than or Equal To(>=)|Checks if the value of variable1 is greater than or equal to variable2.|Syntax:<br><br>1. 1<br><br>1. `variable1 >= variable2` <br><br> <br><br>Example 1:<br><br>1. 1<br><br>1. `5 >= 5 and 9 >= 5` <br><br> <br><br>returns True<br><br>Example 2:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `quantity = 105` <br>2. `minimum = 100` <br>3. `quantity >= minimum` <br><br> <br><br>returns True|
|Greater Than(>)|Checks if the value of variable1 is greater than variable2.|Syntax:<br><br>1. 1<br><br>1. `variable1 > variable2` <br><br> <br><br>Example 1: 9 > 6<br><br>returns True<br><br>Example 2:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `age = 20` <br>2. `max_age = 25` <br>3. `age > max_age` <br><br> <br><br>returns False|
|If Statement|Executes code block `if` the condition is `True`.|Syntax:<br><br>1. 1<br><br>1. `if condition: #code block for if statement` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `if temperature > 30:` <br>2. `print("It's a hot day!")`<br><br> |
|If-Elif-Else|Executes the first code block if condition1 is `True`, otherwise checks condition2, and so on. If no condition is `True`, the else block is executed.|Syntax:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br>8. 8<br><br>1. `if condition1:`<br>2. `# Code if condition1 is True`<br><br>4. `elif condition2:`<br>5. `# Code if condition2 is True`<br><br>7. `else:`<br>8. `# Code if no condition is True`<br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br>8. 8<br>9. 9<br><br>1. `score = 85  # Example score`<br>2. `if score >= 90:`<br>3.     `print("You got an A!")`<br>4. `elif score >= 80:`<br>5.     `print("You got a B.")`<br>6. `else:`<br>7.     `print("You need to work harder.")`<br><br>9. `# Output = You got a B.`<br><br> |
|If-Else Statement|Executes the first code block if the condition is `True`, otherwise the second block.|Syntax:<br><br>1. 1<br>2. 2<br><br>1. `if condition: # Code, if condition is True` <br>2. `else: # Code, if condition is False` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `if age >= 18:`<br>2.     `print("You're an adult.")`<br>3. `else:`<br>4.     `print("You're not an adult yet.")`<br><br> |
|Less Than or Equal To(<=)|Checks if the value of variable1 is less than or equal to variable2.|Syntax:<br><br>1. 1<br><br>1. `variable1 <= variable2` 			 <br><br> <br><br>Example 1:<br><br>1. 1<br><br>1. `5 <= 5 and 3 <= 5` <br><br> <br><br>returns True<br><br>Example 2:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `size = 38` <br>2. `max_size = 40` <br>3. `size <= max_size` <br><br> <br><br>returns True|
|Less Than(<)|Checks if the value of variable1 is less than variable2.|Syntax:<br><br>1. 1<br><br>1. `variable1 < variable2` <br><br> <br><br>Example 1:<br><br>1. 1<br><br>1. `4 < 6` <br><br> <br><br>returns True<br><br>Example 2:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `score = 60` <br>2. `passing_score = 65` <br>3. `score < passing_score` <br><br> <br><br>returns True|
|Loop Controls|`break` exits the loop prematurely. `continue` skips the rest of the current iteration and moves to the next iteration.|Syntax:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br><br>1. `for: # Code to repeat` <br>2.     `if # boolean statement`<br>3.         `break` <br><br>5. `for: # Code to repeat`  <br>6.     `if # boolean statement`<br>7.         `continue`<br><br> <br><br>Example 1:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `for num in range(1, 6):`<br>2.     `if num == 3:`<br>3.         `break`<br>4.     `print(num)`<br><br> <br><br>Example 2:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `for num in range(1, 6):`<br>2.     `if num == 3:`<br>3.         `continue`<br>4.     `print(num)`<br><br> |
|NOT|Returns `True` if variable is `False`, and vice versa.|Syntax:<br><br>1. 1<br><br>1. `!variable` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `!isLocked` <br><br> <br><br>returns True if the variable is False (i.e., unlocked).|
|Not Equal(!=)|Checks if two values are not equal.|Syntax:<br><br>1. 1<br><br>1. `variable1 != variable2` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `a = 10` <br>2. `b = 20` <br>3. `a != b` <br><br> <br><br>returns True<br><br>Example 2:<br><br>1. 1<br>2. 2<br><br>1. `count=0` <br>2. `count != 0` <br><br> <br><br>returns False|
|Object Creation|Creates an instance of a class (object) using the class constructor.|Syntax:<br><br>1. 1<br><br>1. `object_name = ClassName(arguments)` <br><br> <br><br>Example:<br><br>1. 1<br><br>1. `person1 = Person("Alice", 25)`<br><br> |
|OR|Returns `True` if either statement1 or statement2 (or both) are `True`. Otherwise, returns `False`.|Syntax:<br><br>1. 1<br><br>1. `statement1 \| statement2` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `"Farewell Party Invitation"` <br>2. `Grade = 12 grade == 11 or grade == 12` <br><br> <br><br>returns True|
|range()|Generates a sequence of numbers within a specified range.|Syntax:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `range(stop)` <br>2. `range(start, stop)` <br>3. `range(start, stop, step)` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `range(5) #generates a sequence of integers from 0 to 4.` <br>2. `range(2, 10) #generates a sequence of integers from 2 to 9.` <br>3. `range(1, 11, 2) #generates odd integers from 1 to 9.`<br><br> |
|Return Statement|`Return` is a keyword used to send a value back from a function to its caller.|Syntax:<br><br>1. 1<br><br>1. `return value` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `def add(a, b): return a + b` <br>2. `result = add(3, 5)`<br><br> |
|Try-Except Block|Tries to execute the code in the try block. If an exception of the specified type occurs, the code in the except block is executed.|Syntax:<br><br>1. 1<br>2. 2<br><br>1. `try: # Code that might raise an exception except` <br>2. `ExceptionType: # Code to handle the exception` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `try:` <br>2.     `num = int(input("Enter a number: "))` <br>3. `except ValueError:` <br>4.     `print("Invalid input. Please enter a valid number.")`<br><br> |
|Try-Except with Else Block|Code in the `else` block is executed if no exception occurs in the try block.|Syntax:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `try: # Code that might raise an exception except` <br>2. `ExceptionType: # Code to handle the exception` <br>3. `else: # Code to execute if no exception occurs` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br><br>1. `try:` <br>2.     `num = int(input("Enter a number: "))` <br>3. `except ValueError:` <br>4.     `print("Invalid input. Please enter a valid number")` <br>5. `else:` <br>6.     `print("You entered:", num)`<br><br> |
|Try-Except with Finally Block|Code in the `finally` block always executes, regardless of whether an exception occurred.|Syntax:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `try: # Code that might raise an exception except` <br>2. `ExceptionType: # Code to handle the exception` <br>3. `finally: # Code that always executes` <br><br> <br><br>Example:<br><br>1. `try:` <br>2.     `file = open("data.txt", "r")` <br>3.     `data = file.read()` <br>4. `except FileNotFoundError:` <br>5.     `print("File not found.")` <br>6. `finally:` <br>7.     `file.close()`<br><br> |
|While Loop|A `while` loop repeatedly executes a block of code as long as a specified condition remains `True`.|Syntax:<br><br>1. 1<br><br>1. `while condition: # Code to repeat` <br><br> <br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `count = 0 while count < 5:` <br>2.     `print(count) count += 1`<br><br> |

## Reading Text Files

Reading text files involves extracting and processing the data stored within them. Text files can have various structures, and how you read them depends on their format. Here's a general guide on reading text files with different structures:

### Plain Text Files:

- Plain text files contain unformatted text without any specific structure.
- You can read plain text files line by line or load the entire content into memory.

## Using Python's Open Function

Python's `open` function is used to create a file object and access the data within a text file. It takes two primary parameters:

1. **File Path**: The file path consists of the filename and directory where the file is located.
    
2. **Mode**: The mode parameter specifies the purpose of opening the file, such as 'r' for reading, 'w' for writing, or 'a' for appending.

```Python
# Step 1: Open the file in read ('r') mode
file = open('file.txt', 'r')

# Step 2: Read the file content
content = file.read()

# Step 3: Process the content (e.g., print it)
print(content)

# Step 4: Close the file explicitly when done
file.close()
```

#### Step 1: Open the file in read ('r') mode

**open('file.txt', 'r'):** This line opens a file named 'file.txt' in read mode ('r'). It returns a file object, which is stored in the variable file. The 'r' mode indicates that the file will be opened for reading.

#### Step 2: Read the file content

**content = file.read():** Here, the read() method is called on the file object, which reads the entire content of the file and stores it in the variable content. This step effectively loads the entire content of 'file.txt' into memory.

#### Step 3: Process the content (e.g., print it)

**print(content):** This line prints the content of the file to the standard output (usually the console). You can perform any desired processing on the content variable at this point, such as parsing, searching, or analyzing the text.

#### Step 4: Close the file explicitly when done

**file.close():** Finally, this line explicitly closes the file using the close() method. Closing the file is important to release system resources and ensure that the file is properly closed after reading. Failing to close the file can lead to resource leaks.

## The "with" Statement

To simplify file handling and ensure proper closure of files, Python provides the "with" statement. It automatically closes the file when operations within the indented block are completed. This is considered best practice when working with files.

1. `# Step 1: Open the file using 'with' in read ('r') mode`
2. `with open('file.txt', 'r') as file:`
3.     `# Step 2: Read the file content within the 'with' block`
4.     `content = file.read()`

6.     `# Step 3: Process the content (e.g., print it)`
7.     `print(content)`

9. `# Step 4: The file is automatically closed when the 'with' block exits`

Copied!

#### Step 1: Open the file using 'with' in read ('r') mode

**with open('file.txt', 'r') as file:**: This line opens a file named 'file.txt' in read mode ('r') using the with statement, which is a context manager. The file is automatically closed when the code block inside the with statement exits.

#### Step 2: Read the file content within the 'with' block

**content = file.read():** Inside the with block, the read() method is called on the file object. This reads the entire content of the file and stores it in the variable content. Reading the file content occurs within the protected context, ensuring proper resource management.

#### Step 3: Process the content (e.g., print it)

print(content): After reading the file's content, this line prints the content to the standard output (usually the console). You can perform any processing on the content variable at this point, such as text analysis, searching, or manipulation.

#### Step 4: The file is automatically closed when the 'with' block exits

After the code block inside the with statement finishes executing (including any processing or printing), the file is automatically closed. You don't need to explicitly call file.close() because the with statement ensures that the file is properly closed, even if an exception occurs during the execution of the code block.

### Advantages of using `With` Method:

The key advantages of using the with method are:

- **Automatic resource management:** The file is guaranteed to be closed when you exit the with block, even if an exception occurs during processing.
- **Cleaner and more concise code:** You don't need to explicitly call **close()**, making your code more readable and less error-prone.

For most file reading and writing operations in Python, the with method is recommended.

## read method in Python:

You can read the entire content of a file using the read method, which stores the data as a string in a variable. This content can be printed or further manipulated as needed.

```Python
# Reading and Storing the Entire Content of a File

# Using the read method, you can retrieve the complete content of a file
# and store it as a string in a variable for further processing or display.

# Step 1: Open the file you want to read
with open('File1.txt', 'r') as file:

	# Step 2: Use the read method to read the entire content of the file
	file_stuff = file.read()

	# Step 3: Now that the file content is stored in the variable 'file_stuff',
	# you can manipulate or display it as needed.

	# For example, let's print the content to the console:
	print(file_stuff)

# Step 4: The 'with' block automatically closes the file when it's done,
# ensuring proper resource management and preventing resource leaks.
```


**Step 1** involves opening the file, specifying 'File1.txt' as the file to be opened for reading ('r') mode using the with context manager.

**Step 2** utilizes the `read()` method on the file object (file) to read the entire content of the file. This content is then stored in the file_stuff variable.

**Step 3** explains that with the content now stored in file_stuff, you have the flexibility to perform various operations on it. In the example provided, the code prints the content to the console, but you can manipulate, analyze, search, or process the text data in file_stuff based on your specific needs.

**Step 4** emphasizes that the with block automatically closes the file when it's done, ensuring proper resource management and preventing resource leaks. This is a crucial aspect of using the with statement when working with files.

## Reading Lines

Python provides methods to read files line by line:

- The readlines method reads the file line by line and stores each line as an element in a list. The order of lines in the list corresponds to their order in the file.
    
- The readline method reads individual lines from the file. It can be called multiple times to read subsequent lines.
    

In Python, the readline() method is like a detective that reads a book one line at a time. Imagine you have a big book, and you want to read it page by page. readline() helps you do just that, but with lines of text instead of pages.

Here's how it works:

**Opening a File:** First, you need to open the file you want to read using the open() function.

1. `file = open('my_file.txt', 'r')`

**Reading Line by Line:** Now, you can use readline() to read one line from the file at a time. It's like turning the pages of the book, but here, you're getting one sentence (or line) at each turn.

1. `line1 = file.readline()  # Reads the first line`
2. `line2 = file.readline()  # Reads the second line`

**Using the Lines:** You can do things with each line you read. For example, you can print it, check if it contains specific words, or save it somewhere else.

1. `print(line1)  # Print the first line`
2. `if 'important' in line2:`
3.     `print('This line is important!')`


**Looping Through Lines:** Typically, you use a loop to read lines until there are no more lines left. It's like reading the entire book, line by line.

1. `while True:`
2.     `line = file.readline()`
3.     `if not line:`
4.         `break  # Stop when there are no more lines to read`
5.     `print(line)`

**Closing the Book:** When you're done reading, it's essential to close the file using file.close() to make sure you're not wasting resources.

1. `file.close()`

So, in simple terms, **readline()** helps you read a text file line by line, allowing you to work with each line of text as you go. It's like taking one sentence at a time from a book and doing something with it before moving on to the next sentence. Don't forget to close the book when you're done!

## Reading Specific Characters

You can specify the number of characters to read using the readlines method. For example, reading the first four characters, then the next five, and so on.

Reading specific characters from a text file in Python involves opening the file, navigating to the desired position, and then reading the characters you need. Here's a detailed explanation of how to read specific characters from a file:

### Open the File:

First, you need to open the file you want to read. Use the open() function with the appropriate file path and mode. For reading, use 'r' mode.

1. `file = open('my_file.txt', 'r')`

### Navigate to the Desired Position (Optional):

If you want to read characters from a specific position in the file, you can use the seek() method. This method moves the file pointer (like a cursor) to a particular position. The position is specified in bytes, so you'll need to know the byte offset of the characters you want to read.

1. `file.seek(10)  # Move to the 11th byte (0-based index)`

### Read Specific Characters:

To read specific characters, you can use the read() method with an argument that specifies the number of characters to read. It reads characters starting from the current position of the file pointer.

1. `characters = file.read(5)  # Read the next 5 characters`

In this example, it reads the next 5 characters from the current position of the file pointer.

### Use the Read Characters:

You can now use the characters variable to work with the specific characters you've read. You can print them, save them, manipulate them, or perform any other actions.

1. `print(characters)`

### Close the File:

It's essential to close the file when you're done to free up system resources and ensure proper handling of the file.

1. `file.close()`

### Writing to a file

You can create a new text file and write data to it using Python's `open()` function. The `open()` function takes two main arguments: the file path (including the file name) and the mode parameter, which specifies the operation you want to perform on the file. For writing, you should use the mode 'w' Here's an example:

1. `# Create a new file Example2.txt for writing`
2. `with open('Example2.txt', 'w') as File1:`
3.     `File1.write("This is line A\n")`
4.     `File1.write("This is line B\n")`
5.     `# File1 is automatically closed when the 'with' block exits`

#### Line 2 explanation:** `with open('Example2.txt', 'w') as File1:`

- We start by using the open function to open or create a file named `Example2.txt` for writing ('w' mode).
- The `'w'` mode specifies that we intend to write data to the file.
- We use the `with` statement to ensure that the file is automatically closed when the code block exits. This helps manage resources efficiently.

#### Line 3 explanation: `File1.write("This is line A\n")`

- Here, we use the `write()` method on the file object, `File1`, to add the text `This is line A` to the file.
- The `\n` at the end represents a newline character, which starts a new line in the file.

#### Line 4 explanation `File1.write("This is line" B\n")`

- Similarly, we use the `write()` method again to add the text `This is line B` to the file on a new line.

### Writing multiple lines to a file using a list and loop

In Python, you can use a list to store multiple lines of text and then write these lines to a file using a loop. Here's an example code snippet that demonstrates this:

1. `# List of lines to write to the file`
2. `Lines = ["This is line 1", "This is line 2", "This is line 3"]`

4. `# Create a new file Example3.txt for writing`
5. `with open('Example3.txt', 'w') as File2:`
6.     `for line in Lines:`
7.         `File2.write(line + "\n")`
8.     `# File2 is automatically closed when the 'with' block exits`

Here's an explanation of the code:

- Line 2: We start by defining a list called `Lines`, which contains multiple lines of text that we want to write to the file. Each line is a string.
    
- Line 5: Next, we use the `open()` function to create a new text file named `Example3.txt` for writing, `'w'` mode. The `'w'` mode indicates that we intend to write data to the file.
    
- Line 6: We then enter a for loop to iterate through each element (line) in the `Lines` list.
    
- Line 7: Inside the loop, we use the `write()` method on the file object `File2` to write the current line of text (line) to the file. We add `\n` at the end of each line to ensure that each line is followed by a newline character, which separates them in the file.
    
- Line 8: Finally, we add a comment indicating that the file `File2` will be automatically closed when the code block within the with statement exits. Properly closing the file is essential for good resource management.
## Appending data to an existing file

In Python, you can use the `'a'` mode when opening a file to append new data to an existing file without overwriting its contents. Here's an example code snippet that demonstrates this:

1. `# Data to append to the existing file`
2. `new_data = "This is line C"`

4. `# Open an existing file Example2.txt for appending`
5. `with open('Example2.txt', 'a') as File1:`
6.     `File1.write(new_data + "\n")`
7.     `# File1 is automatically closed when the 'with' block exits`

Here's an explanation of the code:

- Line 2: We start by defining a variable `new_data` that contains the text we want to append to the existing file. In this case, it's the string `This is line C.``
    
- Line 5: Next, we use the `open()` function to open an existing file named `Example2.txt` for appending, `'a'` mode. The `'a'` mode indicates that we intend to append data to the file, and if the file doesn't exist, it will be created.
    
- Line 6: Within the with block, we use the `write()` method on the file object `File1` to append the `new_data` to the file. We add `"\n"` at the end to ensure that the appended data starts on a new line, maintaining the file's readability.
    
- Finally, we add a comment indicating that the file `File1` will automatically close when the code block within the `with` statement exits. Properly closing the file is essential for good resource management.

## Copying contents from one file to another

In Python, you can copy the contents of one file to another by reading from the source file and writing to the destination file. Here's an example code snippet that demonstrates this:

1. `# Open the source file for reading`
2. `with open('source.txt', 'r') as source_file:`
3.     `# Open the destination file for writing`
4.     `with open('destination.txt', 'w') as destination_file:`
5.         `# Read lines from the source file and copy them to the destination file`
6.         `for line in source_file:`
7.             `destination_file.write(line)`
8.     `# Destination file is automatically closed when the 'with' block exits`
9. `# Source file is automatically closed when the 'with' block exits`

Here's an explanation of the code:

- Line 2: We start by opening the source file, `source.txt` for reading, `r` mode, using the `with` statement and the `open()` function. This allows us to read data from the source file.
    
- Line 4: Inside the first with block, we open the destination file, `destination.txt` for writing, `w` mode, using another `with` statement and the `open()` function. This prepares the destination file for writing.
    
- Line 6: We use a `for` loop to iterate through each line in the source file `source_file`. This loop reads each line from the source file one by one.
    
- Line 7: Within the loop, we use the `write()` method to write each line from the source file to the destination file `destination_file`. This effectively copies the content of the source file to the destination file.
    
- Lines 8 and 9: After copying all the lines, both the source and destination files are automatically closed when their respective with blocks exit. Proper file closure is crucial for managing resources efficiently.
    
## File modes in Python (syntax and use cases)

The following table provides an overview of different file modes, their syntax, and common use cases. Understanding these modes is essential when working with files in Python for various data manipulation tasks.

|Mode|Syntax|Description|
|:-:|:-:|:--|
|‘r’|`'r'`|Read mode. Opens an existing file for reading. Raises an error if the file doesn't exist.|
|‘w’|`'w'`|Write mode. Creates a new file for writing. Overwrites the file if it already exists.|
|‘a’|`'a'`|Append mode. Opens a file for appending data. Creates the file if it doesn't exist.|
|‘x’|`'x'`|Exclusive creation mode. Creates a new file for writing but raises an error if the file already exists.|
|‘rb’|`'rb'`|Read binary mode. Opens an existing binary file for reading.|
|‘wb’|`'wb'`|Write binary mode. Creates a new binary file for writing.|
|‘ab’|`'ab'`|Append binary mode. Opens a binary file for appending data.|
|‘xb’|`'xb'`|Exclusive binary creation mode. Creates a new binary file for writing but raises an error if it already exists.|
|‘rt’|`'rt'`|Read text mode. Opens an existing text file for reading. (Default for text files)|
|‘wt’|`'wt'`|Write text mode. Creates a new text file for writing. (Default for text files)|
|‘at’|`'at'`|Append text mode. Opens a text file for appending data. (Default for text files)|
|‘xt’|`'xt'`|Exclusive text creation mode. Creates a new text file for writing but raises an error if it already exists.|
|‘r+’|`'r+'`|Read and write mode. Opens an existing file for both reading and writing.|
|‘w+’|`'w+'`|Write and read mode. Creates a new file for reading and writing. Overwrites the file if it already exists.|
|‘a+’|`'a+'`|Append and read mode. Opens a file for both appending and reading. Creates the file if it doesn't exist.|
|‘x+’|`'x+'`|Exclusive creation and read/write mode. Creates a new file for reading and writing but raises an error if it already exists.|

## What is Pandas?

Pandas is a popular open-source data manipulation and analysis library for the Python programming language. It provides a powerful and flexible set of tools for working with structured data, making it a fundamental tool for data scientists, analysts, and engineers.  
Pandas is designed to handle data in various formats, such as tabular data, time series data, and more, making it an essential part of the data processing workflow in many industries.

Here are some **key features and functionalities of Pandas**:

**Data Structures**: Pandas offers two primary data structures - DataFrame and Series.

1. A DataFrame is a two-dimensional, size-mutable, and potentially heterogeneous tabular data structure with labeled axes (rows and columns).
2. A Series is a one-dimensional labeled array, essentially a single column or row of data.

**Data Import and Export**: Pandas makes it easy to read data from various sources, including CSV files, Excel spreadsheets, SQL databases, and more. It can also export data to these formats, enabling seamless data exchange.

**Data Merging and Joining**: You can combine multiple DataFrames using methods like merge and join, similar to SQL operations, to create more complex datasets from different sources.

**Efficient Indexing**: Pandas provides efficient indexing and selection methods, allowing you to access specific rows and columns of data quickly.

**Custom Data Structures**: You can create custom data structures and manipulate data in ways that suit your specific needs, extending Pandas' capabilities.

## Importing Pandas:

Import Pandas using the import command, followed by the library's name.  
Commonly, Pandas is imported as pd for brevity in code.

```Python
import pandas as pd
```

## Data Loading:

- Pandas can be used to load data from various sources, such as CSV and Excel files.
- The read_csv function is used to load data from a CSV file into a Pandas DataFrame.

To read a CSV (Comma-Separated Values) file in Python using the Pandas library, you can use the `pd.read_csv()` function. Here's the syntax to read a CSV file:

```Python
import pandas as pd

# Read the CSV file into a DataFrame
df = pd.read_csv('your_file.csv')
```

Replace 'your_file.csv' with the actual file path of your CSV file. Make sure that the file is located in the same directory as your Python script, or you provide the correct file path.

## What is a Series?

A Series is a one-dimensional labeled array in Pandas. It can be thought of as a single column of data with labels or indices for each element. You can create a Series from various data sources, such as lists, NumPy arrays, or dictionaries  
Here's a basic example of creating a Series in Pandas:

```Python
import pandas as pd

# Create a Series from a list
data = [10, 20, 30, 40, 50]
s = pd.Series(data)

print(s)
```

In this example, we've created a Series named **s** with numeric data. Notice that Pandas automatically assigned numerical indices (0, 1, 2, 3, 4) to each element, but you can also specify custom labels if needed.

## Accessing Elements in a Series

You can access elements in a Series using the index labels or integer positions. Here are a few common methods for accessing Series data:

#### Accessing by label

```Python
print(s[2])     # Access the element with label 2 (value 30)
```


#### Accessing by position

```Python
print(s.iloc[3]) # Access the element at position 3 (value 40)
```

#### Accessing multiple elements

```Python
print(s[1:4])   # Access a range of elements by label
```

## Series Attributes and Methods

Pandas Series come with various attributes and methods to help you manipulate and analyze data effectively. Here are a few essential ones:

- **values**: Returns the Series data as a NumPy array.
- **index**: Returns the index (labels) of the Series.
- **shape**: Returns a tuple representing the dimensions of the Series.
- **size**: Returns the number of elements in the Series.
- **mean(), sum(), min(), max()**: Calculate summary statistics of the data.
- **unique(), nunique()**: Get unique values or the number of unique values.
- **sort_values(), sort_index()**: Sort the Series by values or index labels.
- **isnull(), notnull()**: Check for missing (NaN) or non-missing values.
- **apply()**: Apply a custom function to each element of the Series.

## What is a DataFrames?

A DataFrame is a two-dimensional labeled data structure with columns of potentially different data types. Think of it as a table where each column represents a variable, and each row represents an observation or data point. DataFrames are suitable for a wide range of data, including structured data from CSV files, Excel spreadsheets, SQL databases, and more.

## Creating DataFrames from Dictionaries:

DataFrames can be created from dictionaries, with keys as column labels and values as lists representing rows.

1. `import pandas as pd`

3. `# Creating a DataFrame from a dictionary`
4. `data = {'Name': ['Alice', 'Bob', 'Charlie', 'David'],`
5.         `'Age': [25, 30, 35, 28],`
6.         `'City': ['New York', 'San Francisco', 'Los Angeles', 'Chicago']}`

8. `df = pd.DataFrame(data)`

10. `print(df)`


## Column Selection:

You can select a single column from a DataFrame by specifying the column name within double brackets.  
Multiple columns can be selected in a similar manner, creating a new DataFrame.

```Python
print(df['Name'])  # Access the 'Name' column
```
#### Accessing Rows:

You can access rows by their index using .iloc[] or by label using .loc[].

1. `print(df.iloc[2])   # Access the third row by position`
2. `print(df.loc[1])    # Access the second row by label`

#### Slicing:

You can slice DataFrames to select specific rows and columns.

1. `print(df[['Name', 'Age']])  # Select specific columns`
2. `print(df[1:3])             # Select specific rows`


## Finding Unique Elements:

Use the unique method to determine the unique elements in a column of a DataFrame.

1. `unique_dates = df['Age'].unique()`

## Conditional Filtering:

You can filter data in a DataFrame based on conditions using inequality operators.  
For instance, you can filter albums released after a certain year.

1. `high_above_102 = df[df['Age'] > 25]`

## Saving DataFrames:

To save a DataFrame to a CSV file, use the to_csv method and specify the filename with a “.csv” extension.Pandas provides other functions for saving DataFrames in different formats.

1. `df.to_csv('trading_data.csv', index=False)`

## DataFrame Attributes and Methods

DataFrames provide numerous attributes and methods for data manipulation and analysis, including:

- **shape**: Returns the dimensions (number of rows and columns) of the DataFrame.
- **info()**: Provides a summary of the DataFrame, including data types and non-null counts.
- **describe()**: Generates summary statistics for numerical columns.
- **head(), tail()**: Displays the first or last n rows of the DataFrame.
- **mean(), sum(), min(), max()**: Calculate summary statistics for columns.
- **sort_values()**: Sort the DataFrame by one or more columns.
- **groupby()**: Group data based on specific columns for aggregation.
- **fillna(), drop(), rename()**: Handle missing values, drop columns, or rename columns.
- **apply()**: Apply a function to each element, row, or column of the DataFrame.

> Pandas offers a wide range of methods beyond these examples. For more detailed information, please refer to the official documentation available on the [Pandas official website](https://pandas.pydata.org/docs/ "Pandas official website").

### What is Numpy?

NumPy, short for Numerical Python, is a fundamental library for numerical and scientific computing in Python. It provides support for large, multi-dimensional arrays and matrices, along with a collection of high-level mathematical functions to operate on these arrays. NumPy serves as the foundation for many data science and machine learning libraries, making it an essential tool for data analysis and scientific research in Python.

#### Key aspects of NumPy in Python:

- **Efficient Data Structures**: NumPy introduces efficient array structures, which are faster and more memory-efficient than Python lists. This is crucial for handling large datasets.
    
- **Multi-Dimensional Arrays**: NumPy allows you to work with multi-dimensional arrays, enabling the representation of matrices and tensors. This is particularly useful in scientific computing.
    
- **Element-Wise Operations**: NumPy simplifies element-wise mathematical operations on arrays, making it easy to perform calculations on entire datasets in one go.
    
- **Random Number Generation**: It provides a wide range of functions for generating random numbers and random data, which is useful for simulations and statistical analysis.
    
- **Integration with Other Libraries**: NumPy seamlessly integrates with other data science libraries like SciPy, Pandas, and Matplotlib, enhancing its utility in various domains.
    
- **Performance Optimization**: NumPy functions are implemented in low-level languages like C and Fortran, which significantly boosts their performance. It's a go-to choice when speed is essential.

## Installation

If you haven't already installed NumPy, you can do so using pip:

```Python
pip install numpy
```

## Creating NumPy Arrays

You can create NumPy arrays from Python lists. These arrays can be one-dimensional or multi-dimensional.

### Creating 1D Array

```Python
import numpy as np
```

**import numpy as np**: In this line we imported the NumPy library and assigned it an alias “np” to make it easier to reference in the code.

```Python
# Creating a 1D array
arr_1d = np.array([1, 2, 3, 4, 5]) # **np.array()** is used to create NumPy arrays.
```

**arr_1d = np.array([1, 2, 3, 4, 5])**: In this line, we are creating a one-dimensional NumPy array named arr_1d. It uses the np.array() function to convert a Python list [1, 2, 3, 4, 5] into a NumPy array. This array contains five elements, which are 1, 2, 3, 4, and 5. arr_1d is a 1D array because it has a single row of elements.

### Creating 2D Array

1. `import numpy as np`


**import numpy as np**: In this line we imported the NumPy library and assigned it an alias “np” to make it easier to reference in the code.


1. `# Creating a 2D array`
2. `arr_2d = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])`


**arr_2d = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])**: In this line, we are creating a two-dimensional NumPy array named arr_2d. It uses the np.array() function to convert a list of lists into a 2D NumPy array.  
The outer list contains three inner lists, each of which represents a row of elements. So, arr_2d is a 2D array with three rows and three columns. The elements in this array form a matrix with values from 1 to 9, organized in a 3x3 grid.

### Array Attributes

NumPy arrays have several useful attributes:


1. `# Array attributes`
2. `print(arr_2d.ndim)  # ndim : Represents the number of dimensions or "rank" of the array.`
3. `# output : 2`
4. `print(arr_2d.shape)  # shape : Returns a tuple indicating the number of rows and columns in the array.`
5. `# Output : (3, 3)`
6. `print(arr_2d.size) # size: Provides the total number of elements in the array.`  
7. `# Output : 9`


### Indexing and Slicing

You can access elements of a NumPy array using indexing and slicing:

In this line, we are accessing the 3rd element (index 2) of the 1D array 'arr_1d'.

1. `# Indexing and slicing`
2. `print(arr_1d[2])          # Accessing an element (3rd element)`

In this line, we are accessing the element in the 2nd row (index 1) and 3rd column (index 2) of the 2D array 'arr_2d'.

1. `print(arr_2d[1, 2])       # Accessing an element (2nd row, 3rd column)`

In this line, we are accessing the 2nd row (index 1) of the 2D array 'arr_2d'.

1. `print(arr_2d[1])          # Accessing a row (2nd row)`

In this line, we are accessing the 2nd column (index 1) of the 2D array 'arr_2d'.

1. `print(arr_2d[:, 1])       # Accessing a column (2nd column)`

## Basic Operations

NumPy simplifies basic operations on arrays:

### Element-Wise Arithmetic Operations:

Addition, subtraction, multiplication, and division of arrays with scalars or other arrays.

#### Array Addition

1. `# Array addition`
2. `array1 = np.array([1, 2, 3])`
3. `array2 = np.array([4, 5, 6])`
4. `result = array1 + array2`
5. `print(result)  # [5 7 9`

#### Scalar Multiplication

1. `# Scalar multiplication`
2. `array = np.array([1, 2, 3])`
3. `result = array * 2 # each element of an array is multiplied by 2`
4. `print(result)  # [2 4 6]`

#### Element-wise Multiplication (Hadamard Product)

1. `# Element-wise multiplication (Hadamard product)`
2. `array1 = np.array([1, 2, 3])`
3. `array2 = np.array([4, 5, 6])`
4. `result = array1 * array2`
5. `print(result)  # [4 10 18]`

### Matrix Multiplication

1. `# Matrix multiplication`
2. `matrix1 = np.array([[1, 2], [3, 4]])`
3. `matrix2 = np.array([[5, 6], [7, 8]])`
4. `result = np.dot(matrix1, matrix2)`
5. `print(result)`
6. `# [[19 22]`
7. `#  [43 50]]`

NumPy simplifies these operations, making it easier and more efficient than traditional Python lists.

## Operation with Numpy

Here's the list of operation which can be performed using Numpy

|Operation|Description|Example|
|---|---|---|
|Array Creation|Creating a NumPy array.|arr = np.array([1, 2, 3, 4, 5])|
|Element-Wise Arithmetic|Element-wise addition, subtraction, etc.|result = arr1 + arr2|
|Scalar Arithmetic|Scalar addition, subtraction, etc.|result = arr * 2|
|Element-Wise Functions|Applying functions to each element.|result = np.sqrt(arr)|
|Sum and Mean|Calculating the sum and mean of an array.Calculating the sum and mean of an array.|total = np.sum(arr)  <br>average = np.mean(arr)|
|Maximum and Minimum Values|Finding the maximum and minimum values.|max_val = np.max(arr)  <br>min_val = np.min(arr)|
|Reshaping|Changing the shape of an array.|reshaped_arr = arr.reshape(2, 3)|
|Transposition|Transposing a multi-dimensional array.|transposed_arr = arr.T|
|Matrix Multiplication|Performing matrix multiplication.|result = np.dot(matrix1, matrix2)|

## Working with Data in Python Cheat Sheet

### **Reading and writing files**

|Package/Method|Description|Syntax and Code Example|
|---|---|---|
|File opening modes|Different modes to open files for specific operations.|Syntax: r (reading) w (writing) a (appending) + (updating: read/write) b (binary, otherwise text)<br><br>1. 1<br><br>1. `Examples: with open("data.txt", "r") as file: content = file.read() print(content) with open("output.txt", "w") as file: file.write("Hello, world!") with open("log.txt", "a") as file: file.write("Log entry: Something happened.") with open("data.txt", "r+") as file: content = file.read() file.write("Updated content: " + content)</td>`<br><br>Copied!|
|File reading methods|Different methods to read file content in various ways.|Syntax:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `file.readlines() # reads all lines as a list`<br>2. `readline() # reads the next line as a string`<br>3. `file.read() # reads the entire file content as a string`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br><br>1. `with open("data.txt", "r") as file:`<br>2.     `lines = file.readlines()`<br>3.     `next_line = file.readline()`<br>4.     `content = file.read()`<br><br>Copied!|
|File writing methods|Different write methods to write content to a file.|Syntax:<br><br>1. 1<br>2. 2<br><br>1. `file.write(content) # writes a string to the file`<br>2. `file.writelines(lines) # writes a list of strings to the file`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `lines = ["Hello\n", "World\n"]`<br>2. `with open("output.txt", "w") as file:`<br>3.     `file.writelines(lines)`<br><br>Copied!|
|Iterating over lines|Iterates through each line in the file using a `loop`.|Syntax:<br><br>1. 1<br><br>1. `for line in file: # Code to process each line`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `with open("data.txt", "r") as file:`<br>2. `for line in file: print(line)`<br><br>Copied!|
|Open() and close()|Opens a file, performs operations, and explicitly closes the file using the close() method.|Syntax:<br><br>1. 1<br>2. 2<br><br>1. `file = open(filename, mode) # Code that uses the file`<br>2. `file.close()`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `file = open("data.txt", "r")`<br>2. `content = file.read()`<br>3. `file.close()`<br><br>Copied!|
|with open()|Opens a file using a with block, ensuring automatic file closure after usage.|Syntax:<br><br>1. 1<br><br>1. `with open(filename, mode) as file: # Code that uses the file`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `with open("data.txt", "r") as file:`<br>2. `content = file.read()`<br><br>Copied!|

### **Pandas**

|Package/Method|Description|Syntax and Code Example|
|---|---|---|
|.read_csv()|Reads data from a `.CSV` file and creates a DataFrame.|Syntax: dataframe_name = pd.read_csv("filename.csv") Example: df = pd.read_csv("data.csv")|
|.read_excel()|Reads data from an Excel file and creates a DataFrame.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name = pd.read_excel("filename.xlsx")`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `df = pd.read_excel("data.xlsx")`<br><br>Copied!|
|.to_csv()|Writes DataFrame to a CSV file.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name.to_csv("output.csv", index=False)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `df.to_csv("output.csv", index=False)`<br><br>Copied!|
|Access Columns|Accesses a specific column using [] in the DataFrame.|Syntax:<br><br>1. 1<br>2. 2<br><br>1. `dataframe_name["column_name"] # Accesses single column`<br>2. `dataframe_name[["column1", "column2"]] # Accesses multiple columns`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `df["age"]`<br>2. `df[["name", "age"]]`<br><br>Copied!|
|describe()|Generates statistics summary of numeric columns in the DataFrame.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name.describe()`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `df.describe()`<br><br>Copied!|
|drop()|Removes specified rows or columns from the DataFrame. axis=1 indicates columns. axis=0 indicates rows.|Syntax:<br><br>1. 1<br>2. 2<br><br>1. `dataframe_name.drop(["column1", "column2"], axis=1, inplace=True)`<br>2. `dataframe_name.drop(index=[row1, row2], axis=0, inplace=True)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `df.drop(["age", "salary"], axis=1, inplace=True) # Will drop columns`<br>2. `df.drop(index=[5, 10], axis=0, inplace=True) # Will drop rows`<br><br>Copied!|
|dropna()|Removes rows with missing NaN values from the DataFrame. axis=0 indicates rows.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name.dropna(axis=0, inplace=True)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `df.dropna(axis=0, inplace=True)`<br><br>Copied!|
|duplicated()|Duplicate or repetitive values or records within a data set.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name.duplicated()`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `duplicate_rows = df[df.duplicated()]`<br><br>Copied!|
|Filter Rows|Creates a new DataFrame with rows that meet specified conditions.|Syntax:<br><br>1. 1<br><br>1. `filtered_df = dataframe_name[(Conditional_statements)]`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `filtered_df = df[(df["age"] > 30) & (df["salary"] < 50000)`<br><br>Copied!|
|groupby()|Splits a DataFrame into groups based on specified criteria, enabling subsequent aggregation, transformation, or analysis within each group.|Syntax:<br><br>1. 1<br>2. 2<br><br>1. `grouped = dataframe_name.groupby(by, axis=0, level=None, as_index=True,`<br>2. `sort=True, group_keys=True, squeeze=False, observed=False, dropna=True)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `grouped = df.groupby(["category", "region"]).agg({"sales": "sum"})`<br><br>Copied!|
|head()|Displays the first n rows of the DataFrame.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name.head(n)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `df.head(5)`<br><br>Copied!|
|Import pandas|Imports the Pandas library with the alias pd.|Syntax:<br><br>1. 1<br><br>1. `import pandas as pd`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `import pandas as pd`<br><br>Copied!|
|info()|Provides information about the DataFrame, including data types and memory usage.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name.info()`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `df.info()`<br><br>Copied!|
|merge()|Merges two DataFrames based on multiple common columns.|Syntax:<br><br>1. 1<br><br>1. `merged_df = pd.merge(df1, df2, on=["column1", "column2"])`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `merged_df = pd.merge(sales, products, on=["product_id", "category_id"])`<br><br>Copied!|
|print DataFrame|Displays the content of the DataFrame.|Syntax:<br><br>1. 1<br><br>1. `print(df) # or just type df`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `print(df)`<br>2. `df`<br><br>Copied!|
|replace()|Replaces specific values in a column with new values.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name["column_name"].replace(old_value, new_value, inplace=True)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `df["status"].replace("In Progress", "Active", inplace=True)`<br><br>Copied!|
|tail()|Displays the last n rows of the DataFrame.|Syntax:<br><br>1. 1<br><br>1. `dataframe_name.tail(n)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `df.tail(5)`<br><br>Copied!|

### **Numpy**

|Package/Method|Description|Syntax and Code Example|
|---|---|---|
|Importing NumPy|Imports the NumPy library.|Syntax:<br><br>1. 1<br><br>1. `import numpy as np`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `import numpy as np`<br><br>Copied!|
|np.array()|Creates a one or multi-dimensional array,|Syntax:<br><br>1. 1<br>2. 2<br><br>1. `array_1d = np.array([list1 values]) # 1D Array`<br>2. `array_2d = np.array([[list1 values], [list2 values]]) # 2D Array`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `array_1d = np.array([1, 2, 3]) # 1D Array`<br>2. `array_2d = np.array([[1, 2], [3, 4]]) # 2D Array`<br><br>Copied!|
|Numpy Array Attributes|- Calculates the mean of array elements  <br>- Calculates the sum of array elements  <br>- Finds the minimum value in the array  <br>- Finds the maximum value in the array  <br>- Computes dot product of two arrays|Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br><br>1. `np.mean(array)`<br>2. `np.sum(array)`<br>3. `np.min(array`<br>4. `np.max(array)`<br>5. `np.dot(array_1, array_2)`<br>|

# Introduction to APIs

An API acts as a bridge that allows one software application to interact with another, making it possible for them to share data, functionalities, or services without the need for the user to understand the internal workings of each application. APIs can be used to enable the integration of different systems, allowing them to work together seamlessly.

![What is API](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/WhatisAPI.png "What is API")

# How APIs work?

The operation of an **API (Application Programming Interface)** involves various components that define interactions between software systems or applications. Here's a breakdown of the typical structure and functionality of an API::

### Endpoint:

- An endpoint is a specific URL or URI (Uniform Resource Identifier) that represents a specific function or resource in the API. Each endpoint corresponds to a particular operation that the API can perform.

### Request Methods (HTTP Methods):

- APIs use HTTP methods to specify the type of action the client wants to perform on a given resource. Common HTTP methods include:
    - **GET**: Retrieve data from the server.
    - **POST**: Send data to the server to create a new resource.
    - **PUT or PATCH**: Update an existing resource on the server.
    - **DELETE**: Remove a resource on the server.

### Request Headers:

Headers contain additional information about the request, such as the content type, authentication tokens, or other metadata.

### Request Body:

In some cases, a request may include a body that contains data to be sent to the server. This is common in POST or PUT requests, where the client is sending data to create or update a resource.

![Body_content](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/body_Content.png "Body_content")

### Response Status Code:

The server responds to a client request with an HTTP status code, indicating the success or failure of the operation.

These are typical status codes that you may encounter when interacting with a website:

![Status_part2](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/Statuscode_1.png "Status_part1")  
![Statuscode_Part_2](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/Statuscode_2.png "Statuscode_Part_2")

### Authentication:

Many APIs require authentication to ensure that only authorized users or applications can access certain resources. This can be done using API keys, OAuth tokens, or other authentication mechanisms.

### Documentation:

Good API design includes comprehensive documentation that explains how to use the API, the available endpoints, request and response formats, and any authentication requirements. This documentation helps developers understand and integrate with the API effectively.

# Structure of API URL

Here's what the API structure consist of:-

![API_URL](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/API_URL.png "API_URL")

### - URI (Uniform Resource Identifier):

The entire string [https://api.example.com/v1/get/json.xml?parameter1=value1&parameter2=value2](https://api.example.com/v1/get/json.xml?parameter1=value1&parameter2=value2) is a URI.  
A URI is a string of characters that identifies a name or a resource on the internet.

### - URL (Uniform Resource Locator):

The URL is a specific type of URI that provides the means to access a resource on the web.  
In this case, [https://api.example.com](https://api.example.com/) is a URL.

### - Scheme:

The protocol is specified at the beginning of the URL as **https://**, indicating that the communication should be secured using the HTTPS protocol.

### - Route:

This is the location on the web server; for example: /v1/get/json.xml

# What is NBA_API?

This API provides access to various statistics and data related to the National Basketball Association (NBA). The "nba_api" allows developers to programmatically retrieve information such as player statistics, team information, game results, and more.

# API vs RESTAPI

API (Application Programming Interface) and REST API (Representational State Transfer API) are related terms, but there are distinctions between them.

|Feature|API|Rest API|
|---|---|---|
|Full form|Application Programming Interface|Representational State Transfer API|
|Definition|An API is a set of protocols and tools for building software applications. It defines how different software components should interact.|REST API is a specific type of web API that follows the principles of Representational State Transfer (REST). It is an architectural style for designing networked applications.|
|Scope|API is a broader term encompassing various types of interfaces.|REST API specifically refers to APIs following the principles of REST architecture.|
|Communication|API communication methods can vary.(e.g., RPC, SOAP, etc.)|REST API uses standard HTTP methods (GET, POST, PUT, DELETE) for communication.|
|Architectural Style|Does not necessarily adhere to a specific architectural style|Follows the REST architectural style|
|Data Format|Can use different data formats (e.g., JSON, XML, etc.)|Typically uses lightweight data formats, commonly JSON, for data exchange|
|URI|Resource identification methods may vary|Resources identified by URIs, each with multiple representations|
|Usage|Used in various contexts (web development, libraries, operating systems, etc.)|Primarily used for web services and web-based applications|

# How to access Free Public APIs

To use a public API in your Python code, you need to know the URL of the API endpoint that you want to access. Here's how you can find the URL for a public API from the list provided in the GitHub repository:

- Go to the GitHub repository:
	- [https://github.com/public-apis/public-apis](https://github.com/public-apis/public-apis)

- Scroll down to the table of APIs and find the one that you're interested in using.   
- Look for the "API" column in the table, which will give you the base URL for the API. This is the main URL that you will use to access the API endpoints.
- If the API requires authentication or has additional instructions, look for the "Auth" or "HTTPS" columns for more information.

Once you have the URL for the API, you can use it in your Python code with the requests library to make HTTP requests and retrieve data from the API.  

For example, to retrieve data from the FishWatch API, you can use the following code:

```Python
# Import the requests and json modules for making HTTP requests and handling JSON data, respectively.
import requests
import json

# Specify the URL of the API endpoint for retrieving information about fish species.
url = "https://www.fishwatch.gov/api/species"

# Make an HTTP GET request to the specified URL and store the response in the data variable.
data = requests.get(url)

# Parse the JSON data received from the API response using json.loads() and store it in the results variable.
results = json.loads(data.text)
```

> Note that the specific endpoint you want to access may differ for each API, so you should refer to the API documentation for more information on how to use it.

# Introduction to Web scraping

Web scraping, also known as web harvesting or web data extraction, is the process of extracting information from websites or web pages. It involves automated retrieval of data from web sources and is commonly used for a wide range of applications such as data analysis, data mining, price comparison, content aggregation, and more.

## How web scraping works:

### HTTP Request:

The process typically begins with an HTTP request. A web scraper sends an HTTP request to a specific URL, similar to how a web browser would when you visit a website. The request is usually an HTTP GET request, which retrieves the content of the web page.

### Web Page Retrieval:

The web server hosting the website responds to the request by sending back the requested web page's HTML content. This content includes not only the visible text and media elements but also the underlying HTML structure that defines the page's layout.

### HTML Parsing:

Once the HTML content is received, it needs to be parsed. Parsing involves breaking down the HTML structure into its individual components, such as tags, attributes, and text content. This is where a library like BeautifulSoup in Python is commonly used. It creates a structured representation of the HTML content that can be easily navigated and manipulated.

### Data Extraction:

With the HTML content parsed, web scrapers can now identify and extract the specific data they need. This data can include text, links, images, tables, product prices, news articles, and more. Scrapers locate the data by searching for relevant HTML tags, attributes, and patterns in the HTML structure.

### Data Transformation:

Extracted data may need further processing and transformation. For instance, removing HTML tags from text, converting data formats, or cleaning up messy data. This step ensures that the data is ready for analysis or other use cases.

### Storage:

After extraction and transformation, the scraped data can be stored in various formats, such as databases, spreadsheets, or even JSON or CSV files. The choice of storage format depends on the specific project's requirements.

### Automation:

In many cases, web scraping is automated using scripts or programs. These automation tools allow for recurring data extraction from multiple web pages or websites. Automated scraping is especially useful for collecting data from dynamic websites that regularly update their content.

![Document Tree](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/Webpage.png)

# HTML Structure

HTML (Hypertext Markup Language) serves as the foundation of web pages. Understanding its structure is crucial for web scraping.

- `<html>` is the root element of an HTML page.
- `<head>` contains meta-information about the HTML page.
- `<body>` displays the content on the web page, often the data of interest.
- `<h3>` tags are type 3 headings, making text larger and bold, typically used for player names.
- `<p>` tags represent paragraphs and contain player salary information.

# Composition of an HTML Tag

HTML tags define the structure of web content and can contain attributes.

- An HTML tag consists of an opening (start) tag and a closing (end) tag.
- Tags have names (e.g., `<a>` for an anchor tag).
- Tags may contain attributes with an attribute name and value, providing additional information to the tag.

# HTML Document Tree

HTML documents can be visualized as trees with tags as nodes.

- Tags can contain strings and other tags, making them the tag's children.
- Tags within the same parent tag are considered siblings.
- For example, the `<html>` tag contains both `<head>` and `<body>` tags, making them descendants of `<html` but children of `<html>`. `<head>` and `<body>` are siblings.

![Document Tree](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/DOM_structure.png)

# HTML Tables

HTML tables are essential for presenting structured data.

- Define an HTML table using the `<table>` tag.
- Each table row is defined with a `<tr>` tag.
- The first row often uses the table header tag, typically `<th>`.
- The table cell is represented by `<td>` tags, defining individual cells in a row.

![HTML Table](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-PY0101EN-SkillsNetwork/labs/Module%205/images/table.png)

# Web Scraping

Web scraping involves extracting information from web pages using Python. It can save time and automate data collection.

### Required Tools:

Web scraping requires Python code and two essential modules: Requests and Beautiful Soup. Ensure you have both modules installed in your Python environment.

1. `# Import Beautiful Soup to parse web page content`
2. `from bs4 import BeautifulSoup`

### Fetching and Parsing HTML:

To start web scraping, you need to fetch the HTML content of a webpage and parse it using Beautiful Soup. Here's a step-by-step example:

1. `import requests`
2. `from bs4 import BeautifulSoup`

4. `# Specify the URL of the webpage you want to scrape`
5. `url = 'https://en.wikipedia.org/wiki/IBM'`

7. `# Send an HTTP GET request to the webpage`
8. `response = requests.get(url)`

10. `# Store the HTML content in a variable`
11. `html_content = response.text`

13. `# Create a BeautifulSoup object to parse the HTML`
14. `soup = BeautifulSoup(html_content, 'html.parser')`

16. `# Display a snippet of the HTML content`
17. `print(html_content[:500])`

### Navigating the HTML Structure:

BeautifulSoup represents HTML content as a tree-like structure, allowing for easy navigation. You can use methods like find_all to filter and extract specific HTML elements. For example, to find all anchor tags () and print their text:

1. `# Find all <a> tags (anchor tags) in the HTML`
2. `links = soup.find_all('a')`

4. `# Iterate through the list of links and print their text`
5. `for link in links:`
6.     `print(link.text)`

### Custom Data Extraction:

Web scraping allows you to navigate the HTML structure and extract specific information based on your requirements. This may involve finding specific tags, attributes, or text content within the HTML document.

### Using BeautifulSoup for HTML Parsing

Beautiful Soup is a powerful tool for navigating and extracting specific parts of a web page. It allows you to find elements based on their tags, attributes, or text, making it easier to extract the information you're interested in.

### Using pandas read_html for Table Extraction

On many websites, data is neatly organized in tables. Pandas, a Python library, provides a function called read_html, which can automatically extract data from these tables and present it in a format suitable for analysis. It's similar to taking a table from a webpage and importing it into a spreadsheet for further analysis.

# Cheat Sheet : API's and Data Collection

|Package/Method|Description|Code Example|
|---|---|---|
|Accessing element attribute|Access the value of a specific attribute of an HTML element.|Syntax:<br><br>1. 1<br><br>1. `attribute = element[(attribute)]`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `href = link_element[(href)]`<br><br>Copied!|
|BeautifulSoup()|Parse the HTML content of a web page using BeautifulSoup. The parser type can vary based on the project.|Syntax:<br><br>1. 1<br><br>1. `soup = BeautifulSoup(html, (html.parser))`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `html = (https://api.example.com/data) soup = BeautifulSoup(html, (html.parser))`<br><br>Copied!|
|delete()|Send a DELETE request to remove data or a resource from the server. DELETE requests delete a specified resource on the server.|Syntax:<br><br>1. 1<br><br>1. `response = requests.delete(url)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `response = requests.delete((https://api.example.com/delete))`<br><br>Copied!|
|find()|Find the first HTML element that matches the specified tag and attributes.|Syntax:<br><br>1. 1<br><br>1. `element = soup.find(tag, attrs)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `first_link = soup.find((a), {(class): (link)})`<br><br>Copied!|
|find_all()|Find all HTML elements that match the specified tag and attributes.|Syntax:<br><br>1. 1<br><br>1. `elements = soup.find_all(tag, attrs)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `all_links = soup.find_all((a), {(class): (link)})</td>`<br><br>Copied!|
|findChildren()|Find all child elements of an HTML element.|Syntax:<br><br>1. 1<br><br>1. `children = element.findChildren()`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `child_elements = parent_div.findChildren()`<br><br>Copied!|
|get()|Perform a GET request to retrieve data from a specified URL. GET requests are typically used for reading data from an API. The response variable will contain the server's response, which you can process further.|Syntax:<br><br>1. 1<br><br>1. `response = requests.get(url)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `response = requests.get((https://api.example.com/data))`<br><br>Copied!|
|Headers|Include custom headers in the request. Headers can provide additional information to the server, such as authentication tokens or content types.|Syntax:<br><br>1. 1<br><br>1. `headers = {(HeaderName): (Value)}`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `base_url = (https://api.example.com/data) headers = {(Authorization): (Bearer YOUR_TOKEN)} response = requests.get(base_url, headers=headers)`<br><br>Copied!|
|Import Libraries|Import the necessary Python libraries for web scraping.|Syntax:<br><br>1. 1<br><br>1. `from bs4 import BeautifulSoup`<br><br>Copied!|
|json()|Parse JSON data from the response. This extracts and works with the data returned by the API. The response.json() method converts the JSON response into a Python data structure (usually a dictionary or list).|Syntax:<br><br>1. 1<br><br>1. `data = response.json()`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br><br>1. `response = requests.get((https://api.example.com/data))` <br>2. `data = response.json()`<br><br>Copied!|
|next_sibling()|Find the next sibling element in the DOM.|Syntax:<br><br>1. 1<br><br>1. `sibling = element.find_next_sibling()`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `next_sibling = current_element.find_next_sibling()`<br><br>Copied!|
|parent|Access the parent element in the Document Object Model (DOM).|Syntax:<br><br>1. 1<br><br>1. `parent = element.parent`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `parent_div = paragraph.parent`<br><br>Copied!|
|post()|Send a POST request to a specified URL with data. Create or update POST requests using resources on the server. The data parameter contains the data to send to the server, often in JSON format.|Syntax:<br><br>1. 1<br><br>1. `response = requests.post(url, data)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `response = requests.post((https://api.example.com/submit), data={(key): (value)})`<br><br>Copied!|
|put()|Send a PUT request to update data on the server. PUT requests are used to update an existing resource on the server with the data provided in the data parameter, typically in JSON format.|Syntax:<br><br>1. 1<br><br>1. `response = requests.put(url, data)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `response = requests.put((https://api.example.com/update), data={(key): (value)})`<br><br>Copied!|
|Query parameters|Pass query parameters in the URL to filter or customize the request. Query parameters specify conditions or limits for the requested data.|Syntax:<br><br>1. 1<br><br>1. `params = {(param_name): (value)}`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `base_url = "https://api.example.com/data"`<br>2. `params = {"page": 1, "per_page": 10}`<br>3. `response = requests.get(base_url, params=params)`<br><br>Copied!|
|select()|Select HTML elements from the parsed HTML using a CSS selector.|Syntax:<br><br>1. 1<br><br>1. `element = soup.select(selector)`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `titles = soup.select((h1))`<br><br>Copied!|
|status_code|Check the HTTP status code of the response. The HTTP status code indicates the result of the request (success, error, redirection). Use the HTTP status codeIt can be used for error handling and decision-making in your code.|Syntax:<br><br>1. 1<br><br>1. `response.status_code`<br><br>Copied!<br><br>Example:<br><br>1. 1<br>2. 2<br>3. 3<br><br>1. `url = "https://api.example.com/data"`<br>2. `response = requests.get(url)`<br>3. `status_code = response.status_code`<br><br>Copied!|
|tags for find() and find_all()|Specify any valid HTML tag as the tag parameter to search for elements of that type. Here are some common HTML tags that you can use with the tag parameter.|Tag Example:<br><br>1. 1<br>2. 2<br>3. 3<br>4. 4<br>5. 5<br>6. 6<br>7. 7<br>8. 8<br>9. 9<br>10. 10<br><br>1. `- (a): Find anchor () tags.`<br>2. `- (p): Find paragraph ((p)) tags.`<br>3. `- (h1), (h2), (h3), (h4), (h5), (h6): Find heading tags from level 1 to 6 ( (h1),n (h2)).`<br>4. `- (table): Find table () tags.`<br>5. `- (tr): Find table row () tags.`<br>6. `- (td): Find table cell ((td)) tags.`<br>7. `- (th): Find table header cell ((td))tags.`<br>8. `- (img): Find image ((img)) tags.`<br>9. `- (form): Find form ((form)) tags.`<br>10. `- (button): Find button ((button)) tags.`<br><br>Copied!|
|text|Retrieve the text content of an HTML element.|Syntax:<br><br>1. 1<br><br>1. `text = element.text`<br><br>Copied!<br><br>Example:<br><br>1. 1<br><br>1. `title_text = title_element.text`<br><br>Copied!|

