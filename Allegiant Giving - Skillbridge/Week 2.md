# Courses
1. [Mathematics for Computer Science](https://www.coursera.org/learn/mathematics-for-computer-science/) (Cont'd)

## Modular Arithmetic
Modular arithmetic is a way of doing arithmetic with a fixed, finite set of numbers. In simple terms, it's like doing regular addition, subtraction, multiplication, and division, but instead of working with all the numbers, you work within a specific "modulus" or "clock."

Here's how it works:

1. **Modulus:** You choose a modulus, which is a positive whole number, often denoted as "m." This modulus determines the size of your number set. For example, if you choose a modulus of 12, you're working with numbers 0 to 11 (12 numbers in total).

2. **Operations:** In modular arithmetic, when you perform operations like addition, subtraction, multiplication, or division, you stay within the set of numbers from 0 to m-1. If the result goes beyond this range, you wrap around or "wrap" back to the beginning. 

   - **Addition:** If you add two numbers and the result is greater than or equal to the modulus, you subtract the modulus from the result until it falls within the 0 to m-1 range.
   
   - **Subtraction:** If you subtract two numbers, and the result is negative, you add the modulus to the result until it's within the 0 to m-1 range.

   - **Multiplication and Division:** For multiplication and division, you use modular arithmetic similarly to addition and subtraction, ensuring the result stays within the 0 to m-1 range.

Here's an example using modulus 12:

- 8 + 6 = 14 in regular arithmetic, but in modular arithmetic (mod 12), it's 2 because you wrap around after reaching 11.
- 9 - 5 = 4 in regular arithmetic, and in modular arithmetic (mod 12), it's still 4 because the result is within the 0 to 11 range.
- 3 * 7 = 21 in regular arithmetic, but in modular arithmetic (mod 12), it's 9 because you wrap around after reaching 11.
- 10 / 2 = 5 in regular arithmetic, and in modular arithmetic (mod 12), it's still 5 because the result is within the 0 to 11 range.

In essence, modular arithmetic is like doing arithmetic in a loop, where you keep cycling through a set of numbers and stay within that fixed range. It's commonly used in various fields, including computer science, cryptography, and number theory.

## Sequences and Series
In computer science mathematics, sequences and series are fundamental concepts that involve lists or sequences of numbers and the sum of those numbers. Let me explain them in simple terms:

1. **Sequence:**
   - A sequence is like a list of numbers that follow a specific pattern or order.
   - Each number in the sequence is called a term.
   - For example, 1, 2, 3, 4, 5 is a sequence of natural numbers.

2. **Series:**
   - A series is the sum of the terms in a sequence.
   - It's like adding up all the numbers in the sequence.
   - For example, if we have the sequence 1, 2, 3, 4, 5, the series would be 1 + 2 + 3 + 4 + 5 = 15.

In computer science and mathematics, sequences and series are often used to model and solve various problems, especially in areas like algorithms, data analysis, and numerical computations. Understanding these concepts helps in designing efficient algorithms and solving mathematical problems involving patterns and sums of numbers.

### Arithmetic Sequence:

- An arithmetic sequence is like a list of numbers where each term is obtained by adding the same fixed number (called the common difference) to the previous term.
- In simpler words, you keep adding or subtracting the same amount to get to the next number.
- For example, if you start with 2 and add 3 each time, you get the sequence: 2, 5, 8, 11, 14...

### Geometric Sequence:

- A geometric sequence is like a list of numbers where each term is obtained by multiplying the previous term by the same fixed number (called the common ratio).
- In simpler words, you keep multiplying by the same amount to get to the next number.
- For example, if you start with 2 and multiply by 3 each time, you get the sequence: 2, 6, 18, 54, 162...

In both arithmetic and geometric sequences, the key is that there's a consistent rule for getting from one term to the next. These sequences are commonly used in various mathematical and scientific contexts, such as calculating interest in finance (geometric) or modeling the growth of data (arithmetic or geometric).

### Sigma Notation, Summation
In simple terms, sigma notation, also known as summation notation, is a way to represent the sum of a series of numbers or terms in a concise and organized manner. It uses the Greek letter sigma (Σ) to denote the summation operation. Here's a simple explanation:

1. **Sigma Symbol (Σ):** The sigma symbol Σ is used to indicate that you're going to add up a bunch of things.

2. **Index:** You typically see a variable below the sigma symbol, like "i" or "k." This variable is called the index, and it represents the position of the term you're adding.

3. **Limits:** There are numbers above and below the sigma symbol that show the starting and ending points for the summation. The lower limit (often denoted as "n =") tells you where to begin adding, and the upper limit (often denoted as "m =") tells you where to stop.

4. **Expression:** To the right of the sigma symbol, you have an expression that describes what you're adding at each position, based on the index variable.

Here's an example to illustrate sigma notation:

Σ(i) from i = 1 to 4

This means you're going to add up a series of numbers where "i" starts at 1 and goes up to 4. At each step, you take the current value of "i" and add it to the sum:

Sum = 1 + 2 + 3 + 4 = 10

So, in simple terms, sigma notation helps you represent and easily compute the sum of a sequence of numbers by specifying the pattern for adding them together.

## Graphs of functions and kinematics

### Graphs of Functions:
   - Think of a graph of a function as a way to show how one thing (like time, temperature, or distance) changes in relation to another thing (like speed, age, or height).
   - Imagine a piece of paper with a horizontal line (the x-axis) and a vertical line (the y-axis) intersecting at a point called the origin (usually at the center of the graph).
   - Now, let's say you have a function, which is like a rule that tells you how to calculate the y-coordinate (vertical position) for any given x-coordinate (horizontal position).
   - When you plot points on the graph using the x and y-coordinates from the function, you create a curve or a line that shows how one thing depends on the other.
   - For example, if you have a function that describes how the temperature changes with time, you can create a graph where time is on the x-axis, and temperature is on the y-axis. The curve or line on the graph will show you how the temperature changes over time.

### Kinematics:
   - Kinematics is like a set of rules that helps you describe and understand the motion of objects, like how a car moves, how a ball is thrown, or how a person walks.
   - It's all about studying how things move, so you can predict where they will be at different times.
   - In kinematics, you look at factors like speed, distance, time, and direction to figure out how an object is moving.
   - Imagine watching a car driving down the road. You can use kinematics to answer questions like, "How fast is it going?" or "How long will it take to reach a certain point?"
   - Kinematics equations and graphs help you make sense of these questions by showing how different variables are related to each other as an object moves. For example, a graph might show how an object's position changes with time, so you can see if it's speeding up, slowing down, or staying constant.

In essence, graphs of functions and kinematics are tools that help us visualize and understand how things change and move in the world around us.

### Interval Notation
Interval notation is a way to express and describe sets of real numbers or intervals on the number line in a simple and compact form. It uses brackets and parentheses to show which values are included or excluded within a range. Here's a simple explanation:

1. Square Brackets [ ]:
   - If you see square brackets, like [a, b], it means that both 'a' and 'b' are included in the interval. In other words, the interval contains all the numbers from 'a' to 'b,' including 'a' and 'b' themselves.
   - For example, [2, 5] represents the interval from 2 to 5, including both 2 and 5: {2, 3, 4, 5}.

2. Round Parentheses ( ):
   - If you see round parentheses, like (a, b), it means that 'a' and 'b' are excluded from the interval. In other words, the interval contains all the numbers between 'a' and 'b,' but 'a' and 'b' themselves are not part of it.
   - For example, (1, 4) represents the interval from 1 to 4, but it does not include 1 or 4: {2, 3}.

3. A Combination of Brackets and Parentheses:
   - Sometimes, you might see a combination of brackets and parentheses in an interval. For instance, [a, b) means that 'a' is included, but 'b' is not.
   - Similarly, (a, b] means that 'b' is included, but 'a' is not.
   - For example, [1, 5) includes 1 but not 5, while (2, 6] includes 6 but not 2.

Interval notation is a concise way to represent a range of values on the number line, making it easier to communicate and work with intervals in mathematics and various fields like algebra, calculus, and set theory.

