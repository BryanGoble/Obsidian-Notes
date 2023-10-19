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

### Summation
In simple terms, summation is a mathematical operation that lets you add up a bunch of numbers together. It's like when you have a list of numbers, and you want to find the total or the result of adding all those numbers. 

For example, if you have the numbers 1, 2, 3, 4, and 5, you can use summation to find their sum, which is 1 + 2 + 3 + 4 + 5 = 15. So, in this case, the summation of those numbers is 15.

In mathematical notation, you often see summation represented by the Greek letter sigma (∑). For the example above, it would look like this:

∑ (from 1 to 5) of i

Here, "i" represents each number in the sequence, and the sigma (∑) tells you to add up all the numbers from 1 to 5. So, it's a way of compactly expressing the process of adding a series of numbers.

