# Courses
1. [Introduction to Computer Science and Programming Specialization](https://www.coursera.org/learn/introduction-to-computer-programming/)
2. [How Computers Work](https://www.coursera.org/learn/how-computers-work)
3. [Mathematics for Computer Science](https://www.coursera.org/learn/mathematics-for-computer-science/)
# Requirements
1. Code Editor
	1. B something
	2. VS Code w/ Live Server extension
2. Libraries
	1. p5.js - Javascript drawing utility for the browser

# Content

## P5.JS
p5.js was made to visually illustrate what your code is doing and does this through drawings on a webpage.

p5.js sketches using a coordinate system on the Cartesian Plane, like we used to see back in High School.

### Required Files
1. index.html
2. sketch.js
3. library folder to host the p5.js locally (Optional)

### Sketch.js
Use functions to establish the setup and drawing functionality
```js
function setup() {
	createCanvas(width, height); // 500, 500
}

function draw() {
	rect(x, y, width, height); // 100, 100, 10, 10 - Creates a 10x10 square starting at 100, 100 on the cartesian plane.
}
```

## Abstraction
Describing the main details without unnecessary information
- Numbers and Pixels are two different ways of thinking about the same representation of an image.
- A Notional Machine is an abstraction, simplification, of the working of a computer or software.

A notional machine, often referred to as an abstract machine or theoretical machine, is a conceptual model used in computer science and theoretical computer science to describe and analyze the behavior of algorithms and computer programs. It is not a physical machine or computer but a mathematical and conceptual representation designed to help understand and analyze computation.

Notional machines provide a high-level and simplified view of how algorithms work without getting into the details of specific hardware or low-level programming languages. They are used to describe the step-by-step execution of algorithms, often in a way that is independent of the underlying computer architecture.

Common examples of notional machines include:

1. Turing Machine: Developed by Alan Turing, the Turing machine is one of the most well-known notional machines. It consists of an infinite tape divided into cells and a read/write head. It can perform basic operations like reading, writing, and moving left or right on the tape. The Turing machine is used to model the fundamental principles of computation and is used to define what is computable.

2. Von Neumann Architecture: This notional machine represents the basic architecture of most modern computers. It consists of a central processing unit (CPU), memory, and an instruction set. It illustrates the fetch-decode-execute cycle and how instructions and data are stored and processed in a computer.

3. Register Machine: A register machine is a notional machine that uses a finite number of registers to perform computations. It is often used in the study of computability and complexity theory.

Notional machines are valuable tools for computer scientists and researchers to analyze and compare algorithms, study computational complexity, and prove theorems about the limits of computation. They help abstract away the complexities of real-world computer systems and allow for a more precise and theoretical understanding of computation.

## Binary (Base 2)
Binary numbers come in two forms, 0 or 1. They can be added, subtracted, multiplied, and divided. They can even be converted into other formats like Decimal.

### Binary to Decimal (Base 10)
Binary to decimal conversion is the process of turning a binary number, which uses only two digits (0 and 1), into a decimal number, which uses ten digits (0 through 9). To do this, you start with the rightmost digit of the binary number and assign it the value of 2^0 (which is 1). Then, for each digit to the left, you double the previous value and assign it to that digit. Finally, you add up all these values to get the decimal equivalent of the binary number.

For example, to convert the binary number 1101 to decimal:

1. Start from the right: 1 (rightmost digit) is 2^0 = 1 in decimal.
2. Move to the left: 0 (next digit) is 2^1 = 2 in decimal.
3. Move to the left: 1 (next digit) is 2^2 = 4 in decimal.
4. Move to the left: 1 (leftmost digit) is 2^3 = 8 in decimal.

Now, add up all these values: 8 + 4 + 0 + 1 = 13

So, the binary number 1101 is equal to the decimal number 13.

### Binary Fraction to Decimal
Converting a binary fraction (a binary number with a fractional part) to decimal is also a straightforward process. You can use the same concept as before but with negative powers of 2 for the fractional part. Here's how you can convert the binary fraction 1.0110 to decimal:

1. The whole number part (before the decimal point) is 1, which is the same in both binary and decimal systems.

2. For the fractional part (after the decimal point), you start from the left of the binary fraction (0.0110) and assign negative powers of 2.

   - The first digit to the right of the decimal point is 0, which represents 0 * 2^(-1) = 0 in decimal.
   - The second digit to the right is 1, representing 1 * 2^(-2) = 0.25 in decimal.
   - The third digit to the right is 1, representing 1 * 2^(-3) = 0.125 in decimal.
   - The fourth digit to the right is 0, representing 0 * 2^(-4) = 0 in decimal.

3. Now, add up all these values:

   1 (whole number part) + 0 + 0.25 + 0.125 + 0 = 1.375 in decimal.

So, the binary fraction 1.0110 is equal to the decimal number 1.375.

### Arithmetic in Binary
Certainly! Here are simple explanations of binary addition, subtraction, multiplication, and division:

1. Binary Addition:
   Binary addition is like adding numbers in decimal (base 10) but in base 2. You add the digits from right to left, just like in decimal, but you carry over when the result is 2 (10 in binary). Here's an example:
   
   ```
    1 1 1 0 1  (Carry)
      1 0 1 0 1
   +    1 1 0 1
   ------------
    1 0 0 0 1 0
   ```

   In this example, you start from the right, add 1+1 (with a carry of 1), which is 0 with a carry. Then you move to the next digit and repeat the process.

2. Binary Subtraction:
   Binary subtraction is similar to binary addition but with borrowing instead of carrying. You start from the right and borrow when necessary. Here's an example:

   ```
      1 0 0 0
   -    1 1 0
   ------------
        0 1 0
   ```

   In this example, you borrow from the left to subtract 1 from 10 (2) and get 1.

3. Binary Multiplication:
   Binary multiplication is similar to decimal multiplication but uses only 0 and 1. You multiply the binary digits like you do in decimal and shift left for each new row. Here's an example:

   ```
      1 0 1
   x      1 1
   ---------
      1 0 1
   + 1 0 1
   ---------
   1 1 1 1
   ```

   You multiply each digit in the second number by each digit in the first, shift left for each new row, and add them up.

4. Binary Division:
   Binary division is like decimal division but in base 2. You divide the binary numbers and find the quotient and remainder. Here's an example:

   ```
      1 0 0 1 1
   /        1 1
   --------------
            1 0 0
          +   1 1
   --------------
          0 0 1
   ```

   In this example, you divide 10011 by 11, getting a quotient of 100 and a remainder of 1.

These operations in binary follow similar principles to their decimal counterparts but use base 2 instead of base 10.

### Binary to Octal (Base 8)
Binary to octal conversion is a process of changing a binary number, which uses only 0s and 1s, into an octal number, which uses digits from 0 to 7. 

Here's how it works:

1. Group the binary digits into sets of three, starting from the right. If there are not enough digits to form a group of three, add leading zeros to complete the group.

2. Write down the corresponding octal digit for each group of three binary digits. Here's a simple reference:
   - Binary 000 corresponds to Octal 0.
   - Binary 001 corresponds to Octal 1.
   - Binary 010 corresponds to Octal 2.
   - Binary 011 corresponds to Octal 3.
   - Binary 100 corresponds to Octal 4.
   - Binary 101 corresponds to Octal 5.
   - Binary 110 corresponds to Octal 6.
   - Binary 111 corresponds to Octal 7.

3. Combine the octal digits you found in step 2 to get the octal representation of the original binary number.

### Binary to Hexadecimal (Base 16)
Binary to hexadecimal conversion is a way to represent binary (base-2) numbers using hexadecimal (base-16) digits. Here's a simple explanation:

1. Start with your binary number, which consists of only 0s and 1s.
2. Group the binary digits into sets of four, starting from the right. If there are not enough digits to make a group of four at the end, pad the left side with zeros.
3. Convert each group of four binary digits into a single hexadecimal digit using the following chart:
   - 0000 in binary is 0 in hexadecimal.
   - 0001 in binary is 1 in hexadecimal.
   - 0010 in binary is 2 in hexadecimal.
   - 0011 in binary is 3 in hexadecimal.
   - 0100 in binary is 4 in hexadecimal.
   - 0101 in binary is 5 in hexadecimal.
   - 0110 in binary is 6 in hexadecimal.
   - 0111 in binary is 7 in hexadecimal.
   - 1000 in binary is 8 in hexadecimal.
   - 1001 in binary is 9 in hexadecimal.
   - 1010 in binary is A in hexadecimal.
   - 1011 in binary is B in hexadecimal.
   - 1100 in binary is C in hexadecimal.
   - 1101 in binary is D in hexadecimal.
   - 1110 in binary is E in hexadecimal.
   - 1111 in binary is F in hexadecimal.
4. Write down the hexadecimal digits obtained from each group, and you'll have your hexadecimal representation of the binary number.

For example, let's convert the binary number 110110101011 to hexadecimal:

1. Group into sets of four: 11 0110 1010 1101.
2. Convert each group: 11 = 3, 0110 = 6, 1010 = A, 1101 = D.
3. Write the hexadecimal digits together: 3 6 A D.
4. The hexadecimal representation of 110110101011 is 36AD.

## Decimal (Base 10) Conversions
### Decimal to Octal
Decimal to octal conversion is a process of changing a number from its usual base-10 representation (decimal) into a base-8 representation (octal). Here's a simple explanation of how it works:

1. Start with your decimal number.
2. Divide the decimal number by 8.
3. Write down the remainder (the leftover value after division) as the rightmost digit in the octal number.
4. Take the result of the division (quotient) and repeat steps 2 and 3 until the quotient becomes 0.
5. Write down the remainders you found in step 3 from right to left. This sequence of remainders will be your octal representation of the original decimal number.

For example, let's convert the decimal number 29 to octal:

1. Start with 29.
2. Divide 29 by 8. Quotient = 3, Remainder = 5.
3. Write down the remainder as the rightmost digit of the octal number.
4. Now, take the quotient, which is 3, and repeat the process.
5. Divide 3 by 8. Quotient = 0, Remainder = 3.
6. Write down the remainder as the next digit in the octal number.
7. Since the quotient is now 0, we stop.

So, the octal representation of 29 in octal is 35.

You can also convert a decimal number to octal by using powers of 8. Here's how you can do it for the decimal number 179:

1. Start with the decimal number (179).
2. Find the largest power of 8 that is less than or equal to the decimal number. In this case, 8^2 (64) is the largest power of 8 that fits.
3. Divide 179 by 64 (8^2):
```
	179
/    64
-------
      2 rem 51
```
4. Write down the quotient (2) as the leftmost digit in the octal representation.
5. Now, take the remainder (51) and repeat the process with the next lower power of 8, which is 8^1 (8):
```
	51
/    8
------
	 6 rem 3
```
1. Write down the new quotient (6) as the next digit in the octal number.
2. Finally, take the remainder (3) and write it as the rightmost digit in the octal representation because 3 * 1 = 3.

So, the octal representation of 179 in octal using powers of 8 is 263.

### Octal to Decimal
Octal to decimal conversion is a process of changing a number from the octal number system (base-8) to the decimal number system (base-10). In octal, we use digits 0 through 7, whereas in decimal, we use digits 0 through 9.

Let's use the example of converting the octal number 157 to decimal:

1. Start from the rightmost digit of the octal number, which is 7 in this case.
2. Assign a positional value of 1 to the rightmost digit.
3. Move one position to the left, which is the digit 5.
4. Assign a positional value of 8 (since it's base-8) to this digit.
5. Move one position to the left, which is the digit 1.
6. Assign a positional value of 64 (8^2) to this digit.
7. Now, calculate the decimal equivalent by multiplying each digit by its positional value and adding them together:
   Decimal Equivalent = (1 * 64) + (5 * 8) + (7 * 1)
   Decimal Equivalent = 64 + 40 + 7
   Decimal Equivalent = 111

So, the octal number 157 is equal to the decimal number 111.
### Decimal to Hexadecimal
Decimal to hexadecimal conversion is the process of converting a number from its usual base 10 (decimal) representation into a base 16 (hexadecimal) representation. In decimal, we use digits from 0 to 9, while in hexadecimal, we use digits from 0 to 9 and letters from A to F to represent values 10 to 15.

Here's a simple step-by-step explanation:

1. Start with your decimal number.
2. Divide the decimal number by 16.
3. Write down the remainder (which will be a digit between 0 and 15) as the least significant digit (rightmost digit) of the hexadecimal number.
4. Divide the quotient (the result of the division in step 2) by 16 again.
5. Repeat steps 3 and 4 until the quotient becomes zero, writing down the remainders as you go from right to left.
6. If you encounter remainders greater than 9, use the letters A for 10, B for 11, C for 12, D for 13, E for 14, and F for 15.
7. The sequence of remainders you wrote down in step 5, from right to left, is your hexadecimal representation of the decimal number.

For example, let's convert the decimal number 245 to hexadecimal:

1. Start with 245.
2. 245 divided by 16 is 15 with a remainder of 5. So, we write down 5 as the least significant digit.
3. Now, divide 15 by 16, which gives you 0. Since the quotient is zero, we stop.

So, the decimal number 245 is equivalent to the hexadecimal number 0xF5.

In summary, decimal to hexadecimal conversion involves repeatedly dividing by 16 and writing down remainders as hexadecimal digits until the quotient becomes zero.

Decimal to hexadecimal conversion using base powers is another method that can be quite useful, especially for larger decimal numbers. Here's how it works:

1. Start with your decimal number.
2. Identify the largest power of 16 (hexadecimal base) that is less than or equal to your decimal number. This power of 16 will be the leftmost digit in the hexadecimal representation.
3. Divide your decimal number by 16 raised to that power and write down the result as the leftmost digit in the hexadecimal representation.
4. Subtract the result from step 3 (the leftmost digit in hexadecimal) multiplied by 16 raised to the power from step 2 from your original decimal number.
5. Repeat steps 2 to 4 for the remainder from step 4 until the remainder becomes zero.
6. If you encounter remainders greater than 9, use the letters A for 10, B for 11, C for 12, D for 13, E for 14, and F for 15 in your hexadecimal representation.

Here's an example, converting the decimal number 3657 to hexadecimal using base powers:

1. Start with 3657.
2. The largest power of 16 less than or equal to 3657 is 256 (16^2). So, our leftmost digit in hexadecimal will be determined by dividing 3657 by 256, which is 14 (since 3657 ÷ 256 = 14 with a remainder).
3. Write down 14 as the leftmost digit.
4. Now, subtract 14 * 256 (leftmost digit times the power of 16) from 3657, which gives us a remainder of 41.
5. The largest power of 16 less than or equal to 41 is 16 (16^1). So, our next digit will be determined by dividing 41 by 16, which is 2 with a remainder of 9.
6. Write down 2 as the next digit, and 9 as the last digit. Since 9 is less than 10, it remains as is.

So, the decimal number 3657 is equivalent to the hexadecimal number 0xE49 in this method.

In summary, this method involves finding the largest power of 16 in your decimal number, determining the leftmost digit in hexadecimal, and then subtracting that value to continue the process with the remainder until it becomes zero.

### Hexadecimal to Decimal
Hexadecimal to decimal conversion is a way to change a number represented in base-16 (hexadecimal) to its equivalent in base-10 (decimal). 

In hexadecimal, there are 16 possible digits: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, and F. 

To convert from hexadecimal to decimal, you can follow these steps:

1. Write down the hexadecimal number you want to convert.
2. Starting from the rightmost digit (the least significant digit), assign a decimal value to each digit based on its position. 
   - Digits 0 to 9 in hexadecimal have the same values as in decimal.
   - A in hexadecimal is 10 in decimal, B is 11, C is 12, D is 13, E is 14, and F is 15 in decimal.
3. Multiply each digit by its corresponding decimal value and add up all the results to get the decimal equivalent.

For example, let's convert the hexadecimal number "1A" to decimal:

1. Start from the right: A represents 10 in decimal, and 1 represents 1 in decimal.
2. Multiply A by 10 and 1 by 1.
3. Add the results: 10 + 1 = 11.

So, the hexadecimal number "1A" is equal to the decimal number 11.

## Fractionals
### Octal Fractionals

| 512 | 64 | 8 | 1 | . | 1/8 | 1/64 | 1/512 |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 8$^3$ | 8$^2$ | 8$^1$ | 8$^0$ | . | 8$^-1$ | 8$^-2$ | 8$^-3$ |

Converting an octal fractional number to decimal is straightforward. Octal is a base-8 numbering system, while decimal is base-10. To convert an octal fractional number like 0.72 to decimal, follow these steps:

1. Write down the octal fractional number, in this case, 0.72.
2. Assign place values to each digit in the octal fraction, starting from the left and moving to the right, using negative powers of 8.
   For 0.72:
   - The first digit '7' is in the "eighth" place (8^-1).
   - The second digit '2' is in the "sixty-fourth" place (8^-2).

3. Multiply each digit by its respective place value and sum up the results.
   Decimal equivalent = (7 * 8^-1) + (2 * 8^-2)

4. Calculate the values of each term:
   - (7 * 1/8) = 7/8
   - (2 * 1/64) = 2/64 = 1/32

5. Add the results together:
   Decimal equivalent = (7/8) + (1/32)

6. Simplify the fraction by finding a common denominator:
   Decimal equivalent = (28/32) + (1/32)

7. Add the fractions:
   Decimal equivalent = 29/32

So, 0.72 in octal is equal to 29/32 in decimal.

Decimal fractionals to octal conversion involves converting a decimal number with a fractional part into its equivalent octal (base-8) representation. Here's a simple explanation using the example of the decimal fractional number 0.515625:

1. **Convert the Whole Part to Octal:**
   - Take the whole part of the decimal number (0 in this case) and convert it to octal. This is straightforward because 0 in decimal is also 0 in octal.
2. **Convert the Fractional Part to Octal:**
   - Take the fractional part of the decimal number (0.515625) and convert it to octal. This is done by multiplying the fractional part by 8 repeatedly, keeping track of the whole number part at each step until the fractional part becomes 0 or until you've obtained the desired number of octal digits.

   - Start by multiplying 0.515625 by 8:
     - 0.515625 * 8 = 4.125
     - So, the first octal digit is 4, and we have 0.125 left.

   - Now, multiply 0.125 by 8:
     - 0.125 * 8 = 1.0
     - The next octal digit is 1, and there's no remainder.

3. **Combine the Whole and Fractional Octal Parts:**
   - Combine the whole part (0) and the fractional part (41) to get the octal representation: 0.415 (in octal).

So, the decimal fractional number 0.515625 is equivalent to 0.415 in octal notation.

### Hexadecimal Fractionals

| 4096 | 256 | 16 | 1 | . | 1/16 | 1/256 | 1/... |
| :-: | :-: | :-: | :-: | :-: | :-: | :-: | :-: |
| 16$^3$ | 16$^2$ | 16$^1$ | 16$^0$ | . | 16$^-1$ | 16$^-2$ | 16$^-3$ |

Hexadecimal numbers use a base-16 system, which means they have 16 different digits: 0-9 and A-F, where A represents 10, B represents 11, and so on up to F, which represents 15.

To convert a hexadecimal fractional number to decimal, follow these steps:

1. Identify the hexadecimal fractional part. In your example, the fractional part is '9B.'
2. Assign decimal values to the hexadecimal digits:
   - 9 in hexadecimal is equivalent to 9 in decimal.
   - B in hexadecimal is equivalent to 11 in decimal.
3. Convert each digit to its decimal equivalent:
   - For '9,' it remains '9' in decimal.
   - For 'B,' it becomes '11' in decimal.
4. Write the hexadecimal fractional number as a sum of its decimal equivalents with negative powers of 16:
   - 9B in hexadecimal becomes (9 * 16^-1) + (11 * 16^-2) in decimal.
5. Calculate the values:
   - (9 * 16^-1) is 9/16 in decimal, which is 0.5625.
   - (11 * 16^-2) is 11/256 in decimal, which is approximately 0.043.
6. Add the calculated values together:
   - 0.5625 + 0.043 = 0.6055 (rounded to four decimal places).

So, 0.9B in hexadecimal is approximately equal to 0.6055 in decimal.

Decimal fractional to hexadecimal conversion involves converting a decimal number with a fractional part (like 1.96875) into its hexadecimal (base-16) equivalent. Here's a simple explanation using your example:

1. Take the decimal fractional part (0.96875) and multiply it by 16.
   - 0.96875 * 16 = 15.5
2. The integer part of this result (15) is the first digit in the hexadecimal representation.
3. Take the fractional part of the result (0.5) and multiply it by 16 again.
   - 0.5 * 16 = 8
4. The integer part of this new result (8) is the second digit in the hexadecimal representation.

So, the hexadecimal representation of the decimal fractional 0.96875 is 0.F in hexadecimal notation.
Therefore, 1.96875 in decimal is equivalent to 1.0F in hexadecimal.

## Steganography using Binary

Steganography is a method of hiding a secret message within another piece of data, such as an image, without it being apparent to anyone who looks at the data. In this case, we'll use binary messages and hexadecimal color values to explain how it works.

1. Binary Messages: Binary is a system of representing information using only two symbols, usually 0 and 1. In the context of steganography, a binary message is a series of these 0s and 1s that you want to hide within another piece of data.
    
2. Hexadecimal Color Values: In digital images, colors are often represented using hexadecimal values. Hexadecimal is a base-16 numbering system that uses the digits 0-9 and the letters A-F to represent values from 0 to 15. Each color in an image is typically described using a combination of red (R), green (G), and blue (B) values, each represented by two hexadecimal digits. For example, the color white is represented as #FFFFFF, where FF stands for the highest intensity of red, green, and blue.
    

Here's a simple way to use steganography with binary messages and hexadecimal color values:
1. Break up your image pixels into rows and columns to divide the colors
2. Convert the colors into their hexadecimal equivalents (eg. 255 192 000)
3. Convert individual hex values to binary then take the last digit (eg. 255 becomes 1111 1111. Keep 1)
4. The 3 values kept become your binary number which can be converted to decimal.

To encode a message, do the opposite
1. Choose your message in decimal format
2. Convert each number to 3 digit binary
3. Take each digit and replace the final hex color value in each pixel.
4. The colors will ever so slightly change, but look almost original.