# 🐍 Python Day-2 Notes

## 📌 Topics Covered
- Python Installation & Setup
- Python Basics
- Variables
- Keywords
- Data Types

---

## 📑 Table of Contents
1. Python Installation & Setup  
2. Python Basics  
3. Hello World Program  
4. Indentation in Python  
5. Variables in Python  
6. Rules for Naming Variables  
7. Assigning Values to Variables  
8. Type Casting  
9. Checking Data Types  
10. Object Reference in Python  
11. Deleting a Variable  
12. Python Keywords  
13. Keywords vs Identifiers  
14. Python Data Types  
15. Day-2 Summary  

---

## 1. Python Installation & Setup

### Ways to Run Python

#### Local Installation
- Install Python from the official website
- Use:
  - Terminal / Command Prompt
  - IDLE
  - VS Code
  - PyCharm

#### Online Code Editors
- No installation required
- Search **"online Python compiler"**
- Select Python → Write code → Run

---

## 2. Python Basics

### Key Features of Python
- Created in **1991**
- Easy to read and write
- Requires fewer lines of code
- Dynamically typed
- Supports:
  - Object-Oriented Programming
  - Functional Programming
  - Procedural Programming

---

## 3. Hello World Program

```python
# This is a comment
print("Hello, World!")
````

### Output

```
Hello, World!
```

### Explanation

* `print()` → Displays output
* `"Hello, World!"` → String
* `#` → Single-line comment

### Multi-Line Comment

```python
"""
This is a multi-line comment.
Used to explain large sections of code.
"""
```

---

## 4. Indentation in Python

* Python uses indentation to define code blocks
* Same indentation → same block
* Standard: **4 spaces** or **1 tab**

### Incorrect Example

```python
print("No indentation")
    print("Wrong indentation")
```

### Error

```
IndentationError: unexpected indent
```

---

## 5. Variables in Python

A variable is a name that refers to a value.

```python
x = 5
name = "Samantha"
print(x)
print(name)
```

---

## 6. Rules for Naming Variables

### Valid Rules

* Letters (a–z, A–Z)
* Digits (0–9)
* Underscore (_)
* Cannot start with a digit
* Case-sensitive
* Cannot use keywords

### Valid Examples

```python
age = 21
_colour = "lilac"
total_score = 90
```

### Invalid Examples

```python
1name = "Error"
class = 10
user-name = "Doe"
```

---

## 7. Assigning Values to Variables

### Basic Assignment

```python
x = 5
y = 3.14
z = "Hi"
```

### Dynamic Typing

```python
x = 10
x = "Now a string"
```

### Multiple Assignment

```python
x, y, z = 1, 2.5, "Python"
```

### Same Value Assignment

```python
a = b = c = 100
```

---

## 8. Type Casting

Converting one data type to another.

```python
s = "10"
n = int(s)

cnt = 5
f = float(cnt)

age = 25
s2 = str(age)
```

---

## 9. Checking Data Types

```python
print(type(10))        # int
print(type(3.14))      # float
print(type("Hello"))   # str
print(type([1,2,3]))   # list
print(type({'a':1}))   # dict
print(type(True))      # bool
```

---

## 10. Object Reference in Python

Variables store references, not actual values.

```python
x = 5
y = x
x = "Geeks"
```

* `y` still refers to `5`
* Reassigning one variable does not affect others

---

## 11. Deleting a Variable

```python
x = 10
del x
```

* Removes variable from memory
* Accessing again → `NameError`

---

## 12. Python Keywords

Reserved words with predefined meaning.

### Example (Error)

```python
for = 10
```

### Get All Keywords

```python
import keyword
print(keyword.kwlist)
```

---

## 13. Keywords vs Identifiers

| Keywords          | Identifiers    |
| ----------------- | -------------- |
| Reserved words    | User-defined   |
| Cannot be changed | Can be changed |
| if, for           | x, total       |

---

## 14. Python Data Types

### Built-in Data Types

* Numeric → int, float, complex
* Sequence → string, list, tuple
* Mapping → dict
* Boolean → bool
* Set → set, frozenset

---

### Numeric Data Types

```python
a = 5
b = 5.0
c = 2 + 4j
```

---

### String Data Type

```python
s = "Welcome to Python"
print(s[0])
print(s[-1])
```

---

### List Data Type

```python
a = [1, 2, 3]
b = ["Geeks", 4, True]
```

---

### Tuple Data Type

```python
tup = (1, 2, 3)
t = (5,)
```

---

### Boolean Data Type

```python
if 1:
    print("Truthy")

if not 0:
    print("Falsy")
```

---

### Set Data Type

```python
s = set(["Geeks", "For", "Geeks"])
```

---

### Dictionary Data Type

```python
d = {1: "Geeks", "name": "For"}
print(d["name"])
```

---

## ✅ Day-2 Summary

✔ Python installation
✔ Variables & rules
✔ Keywords
✔ Type casting
✔ Object references
✔ All major data types

## problems
1.Comments are very useful in any language to tell users what is the task of any function or operation. The comments are neglected by the compiler, so whatever you write in the comments won't have any effect on the working of a code.
In Python, comments can be written as mentioned below: This is a comment
""" This is also a comment """
You are given a complete function that outputs a, b, and c. Comment the code that outputs b, so only a and c gets printed.

2.When learning a new language, we first learn to output some message. Here we will start with the famous "Hello World" message.
Complete the python code to print "Hello World".

3.Exercises: Level 1
3.1 Inside 30DaysOfPython create a folder called day_2. Inside this folder create a file named variables.py
3.2 Write a python comment saying 'Day 2: 30 Days of python programming'
3.3 Declare a first name variable and assign a value to it
3.4 Declare a last name variable and assign a value to it
3.5 Declare a full name variable and assign a value to it
3.6 Declare a country variable and assign a value to it
3.7 Declare a city variable and assign a value to it
3.8 Declare an age variable and assign a value to it
3.9 Declare a year variable and assign a value to it
3.10 Declare a variable is_married and assign a value to it
3.11 Declare a variable is_true and assign a value to it
3.12 Declare a variable is_light_on and assign a value to it
3.13 Declare multiple variable on one line

4.Exercises: Level 2
4.1 Check the data type of all your variables using type() built-in function
4.2 Using the len() built-in function, find the length of your first name
4.3 Compare the length of your first name and your last name
4.4 Declare 5 as num_one and 4 as num_two
4.5 Add num_one and num_two and assign the value to a variable total
4.6 Subtract num_two from num_one and assign the value to a variable diff
4.7 Multiply num_two and num_one and assign the value to a variable product
4.8 Divide num_one by num_two and assign the value to a variable division
4.9 Use modulus division to find num_two divided by num_one and assign the value to a variable remainder
4.10 Calculate num_one to the power of num_two and assign the value to a variable exp
4.11 Find floor division of num_one by num_two and assign the value to a variable floor_division
4.12 The radius of a circle is 30 meters.
4.13 Calculate the area of a circle and assign the value to a variable name of area_of_circle
4.14 Calculate the circumference of a circle and assign the value to a variable name of circum_of_circle
4.15 Take radius as user input and calculate the area.
4.16 Use the built-in input function to get first name, last name, country and age from a user and store the value to their corresponding variable names
4.17 Run help('keywords') in Python shell or in your file to check for the Python reserved words or keywords
