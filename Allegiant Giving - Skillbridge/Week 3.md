# Courses
1. [Programming For Everybody (Getting Started With Python)](https://www.coursera.org/learn/python/)

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
   ```

In this structure:

- You specify the type of error you want to handle (e.g., `SomeErrorType`), or you can use a more general `except` without specifying an error type to catch any exception.
- If the error of the specified type occurs in the `try` block, Python will execute the code inside the corresponding `except` block.

Using try/except blocks helps prevent your program from crashing due to unexpected errors, making your code more robust and user-friendly.