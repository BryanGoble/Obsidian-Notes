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