
#### 🐍 Python Basics – Data Types, Typecasting & Truthy/Falsy Values

This repository contains notes and examples covering fundamental Python concepts, including **data types**, **variable naming rules**, **typecasting**, **comments**, and **truthy vs falsy values**.  
These concepts form the foundation for writing clean, readable, and logical Python programs.

---

## 📌 1. Data Types Review

Python provides several built-in data types to store different kinds of values:

### 🔹 Integer (`int`)
- Used to store whole numbers.
- Example: `10`, `-5`, `0`

### 🔹 Floating Point (`float`)
- Used for decimal numbers.
- Example: `3.14`, `-2.5`

### 🔹 String (`str`)
- A collection of characters.
- Can include letters, numbers, special symbols, and spaces.
- Defined using **single quotes** (`' '`) or **double quotes** (`" "`).

```python
name = "Python"
email = 'user@example.com'
````

### 🔹 Complex (`complex`)

* Numbers with a real and imaginary part.
* Imaginary part is represented using `j`.

```python
num = 1 + 3j
```

### 🔹 Range (`range`)

* Represents a sequence of numbers.
* Commonly used in loops.

```python
r = range(1, 5)
```

### 🔹 Additional Data Types

* `bytes`
* `list`
  (These are advanced concepts and will be explored later.)

---

## 📌 2. Variable Naming Rules

Python variables must follow these rules:

* Cannot start with a number ❌
* Must start with a **letter** or an **underscore (_)** ✅
* Can contain letters, numbers, and underscores
* Case-sensitive (`age` and `Age` are different)

```python
valid_name = 10
_age = 25
# 2name = 5 ❌ Invalid
```

---

## 📌 3. Typecasting

**Typecasting** is the process of converting one data type into another.

### 🔹 Checking the Data Type

Use the built-in `type()` function:

```python
a = 10
print(type(a))
```

### 🔹 Conversion Examples

```python
x = 3.14
print(int(x))   # Output: 3
```

* Decimal part is removed when converting `float` to `int`.

```python
num = "25"
print(int(num))  # Output: 25
```

* Strings can be converted only if they contain valid numeric values.

---

## 📌 4. Comments in Python

Comments help explain code and improve readability.
They are **ignored by the Python interpreter**.

### 🔹 Single-line Comments

```python
# This is a single-line comment
print("Hello, Python!")
```

### 🔹 Multi-line Comments

```python
"""
This is a multi-line comment.
Used to describe large blocks of code.
"""
```

---

## 📌 5. Truthy vs Falsy Values in Python

In Python, every value can be evaluated as either **True** or **False** in a Boolean context.

### 🔹 Example

```python
number = 7
if number:
    print("This will print because 7 is truthy.")

number = 0
if number:
    print("This will NOT print because 0 is falsy.")
```

### 🔹 Output

```
This will print because 7 is truthy.
```

---

## ✅ Truthy Values

These evaluate to `True`:

* Non-empty sequences or collections
  `[1]`, `(0,)`, `"Hello"`, `{1:2}`
* Non-zero numbers
  `1`, `-4`, `3.5`
* Constant
  `True`

```python
if [1, 2]:
    print("Non-empty list is truthy")

if -4:
    print("-4 is truthy")
```

---

## ❌ Falsy Values

These evaluate to `False`:

* Empty sequences or collections
  `[]`, `()`, `{}`, `set()`, `range(0)`
* Zero values
  `0`, `0.0`, `0j`
* Constants
  `None`, `False`

```python
if not 0:
    print("0 is falsy")

if not []:
    print("Empty list is falsy")
```

---

## 📌 6. Practical Example – Odd or Even Check

```python
num1 = 7
num2 = 4

if num1 % 2:
    print(num1, "is odd")
else:
    print(num1, "is even")

if num2 % 2:
    print(num2, "is odd")
else:
    print(num2, "is even")
```

### 🔹 Output

```
7 is odd
4 is even
```

---

## 📌 7. Built-in `bool()` Function

The `bool()` function converts any value into a Boolean (`True` or `False`).

```python
print(bool(7))      
print(bool(0))      
print(bool([1,2,3]))
print(bool([]))      
print(bool(None))
```

### 🔹 Output

```
True
False
True
False
False
```

---

## 🚀 Conclusion

Understanding **data types**, **typecasting**, **comments**, and **truthy/falsy values** helps in writing:

* Cleaner code
* Better conditions
* More Pythonic programs

These basics are essential before moving on to loops, functions, and advanced concepts.


```
