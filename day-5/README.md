# 🐍 Python Day 3 – Data Types & Operators

This README covers Boolean values, Python operators, examples, and practice exercises.
It is designed for beginners to understand how Python evaluates expressions and conditions.

## 📌 Boolean Data Type

A Boolean represents one of two values:

True

False

⚠️ Note:

True and False must start with capital letters in Python.

0, empty string "", and None are treated as False

All other values are True

### Example
print(True)
print(False)

## 📌 Operators in Python

Operators are special symbols used to perform operations on values and variables.

Operands

Values on which operators act.

## ➕ Arithmetic Operators
Operator	Description
+	Addition
-	Subtraction
*	Multiplication
/	Division
%	Modulus
//	Floor Division
**	Exponentiation
### Example (Integers)
print('Addition:', 1 + 2)
print('Subtraction:', 2 - 1)
print('Multiplication:', 2 * 3)
print('Division:', 7 / 2)
print('Floor Division:', 7 // 2)
print('Modulus:', 3 % 2)
print('Exponentiation:', 2 ** 3)

🔢 Floating Numbers
print(3.14)
print(9.81)

🔢 Complex Numbers
print(1 + 1j)
print((1 + 1j) * (1 - 1j))

## 📌 Variables & Assignment
a = 3
b = 2

total = a + b
diff = a - b
product = a * b
division = a / b
remainder = a % b
floor_div = a // b
power = a ** b

📐 Practical Calculations
Area of a Circle
radius = 10
area = 3.14 * radius ** 2
print(area)

Area of a Rectangle
length = 10
width = 20
area = length * width
print(area)

Weight Calculation
mass = 75
gravity = 9.81
weight = mass * gravity
print(weight, "N")

## 📌 Comparison Operators
Operator	Meaning
>	Greater than
<	Less than
==	Equal to
!=	Not equal
>=	Greater or equal
<=	Less or equal
### Example
print(3 > 2)
print(3 == 2)
print(len("python") > len("dragon"))

## 📌 Identity Operators
Operator	Description
is	Same object
is not	Different object
a = 10
b = 10
print(a is b)

## 📌 Membership Operators
Operator	Description
in	Exists in sequence
not in	Not exists
print("on" in "python")
print("z" not in "dragon")

## 📌 Logical Operators

Python uses keywords instead of symbols:

Operator	Meaning
and	Logical AND
or	Logical OR
not	Logical NOT
### Example
print(3 > 2 and 4 > 3)
print(3 > 2 or 4 < 3)
print(not True)

## 📌 Bitwise Operators
a = 10
b = 4

print(a & b)
print(a | b)
print(~a)
print(a ^ b)
print(a >> 2)
print(a << 2)

## 📌 Assignment Operators
a = 10
b = a
b += a
b -= a
b *= a

## 📌 Ternary Operator

Single-line conditional expression:

a, b = 10, 20
min_val = a if a < b else b
print(min_val)

## 📌 Operator Precedence

Order of execution:

not

and

or

print(10 + 20 * 30)

# Exercise
1. Declare your age as integer variable
2. Declare your height as a float variable
3. Declare a variable that store a complex number
4. Write a script that prompts the user to enter base and height of the triangle and calculate an area of this triangle (area = 0.5 x b x h).

```py
    Enter base: 20
    Enter height: 10
    The area of the triangle is 100
```

5. Write a script that prompts the user to enter side a, side b, and side c of the triangle. Calculate the perimeter of the triangle (perimeter = a + b + c).

```py
Enter side a: 5
Enter side b: 4
Enter side c: 3
The perimeter of the triangle is 12
```

6. Get length and width of a rectangle using prompt. Calculate its area (area = length x width) and perimeter (perimeter = 2 x (length + width))
7. Get radius of a circle using prompt. Calculate the area (area = pi x r x r) and circumference (c = 2 x pi x r) where pi = 3.14.
8. Calculate the slope, x-intercept and y-intercept of y = 2x -2
9. Slope is (m = y2-y1/x2-x1). Find the slope and [Euclidean distance](https://en.wikipedia.org/wiki/Euclidean_distance#:~:text=In%20mathematics%2C%20the%20Euclidean%20distance,being%20called%20the%20Pythagorean%20distance.) between point (2, 2) and point (6,10) 
10. Compare the slopes in tasks 8 and 9.
11. Calculate the value of y (y = x^2 + 6x + 9). Try to use different x values and figure out at what x value y is going to be 0.
12. Find the length of 'python' and 'dragon' and make a falsy comparison statement.
13. Use _and_ operator to check if 'on' is found in both 'python' and 'dragon'
14. _I hope this course is not full of jargon_. Use _in_ operator to check if _jargon_ is in the sentence.
15. There is no 'on' in both dragon and python
16. Find the length of the text _python_ and convert the value to float and convert it to string
17. Even numbers are divisible by 2 and the remainder is zero. How do you check if a number is even or not using python?
18. Check if the floor division of 7 by 3 is equal to the int converted value of 2.7.
19. Check if type of '10' is equal to type of 10
20. Check if int('9.8') is equal to 10
21. Writ a script that prompts the user to enter hours and rate per hour. Calculate pay of the person?

```py
Enter hours: 40
Enter rate per hour: 28
Your weekly earning is 1120
```

22. Write a script that prompts the user to enter number of years. Calculate the number of seconds a person can live. Assume a person can live hundred years

```py
Enter number of years you have lived: 100
You have lived for 3153600000 seconds.
```

23. Write a Python script that displays the following table

```py
1 1 1 1 1
2 1 2 4 8
3 1 3 9 27
4 1 4 16 64
5 1 5 25 125
```

24. You are given two integer variables x and y. You need to perform the following operations:

```py
p = x + y : Addition
q = x - y : Subtraction
r = x * y :Multiplication
s = x / y : Division
t = x % y : Modulo
Examples:

Input: x = 1, y = 2
Output: 3 -1 2 0 1 
Explanation: The given operations are performed.
Input: x = 3, y = 4 
Output: 7 -1 12 0 3 
Explanation: The given operations are performed
Constraints:
-100 ≤ x ≤ 100
-100 ≤ y ≤ 100
```

25. 🧠 Logical Operators in Python

Logical operators `and`, `or`, and `not` are used in Python for condition checking.

- `a and b` checks if both `a` and `b` are True  
- `a or b` checks if either `a` or `b` is True  
- `not a` complements the boolean value of `a`
```py
⚠️ **Note:**  
- `0` and empty string `""` are treated as **False**  
- All other values are treated as **True**

---
📌 Problem Statement

Given two variables `a` and `b`, perform the following logical operations:

1. `a and b`
2. `a or b`
3. `not a`

Print the results in a **single line**, separated by spaces.
📥 Example 1

**Input**
```text
a = 0, b = 2

Output

0 2 True 
```
