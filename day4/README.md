
# 🐍 Python Input & Output – `print()` and `input()` Functions

This repository documents today’s learning on **Input and Output operations in Python**.  
Understanding how to display output and take user input is a fundamental skill required for writing interactive Python programs.

---

## 📌 1. Output Functionality: `print()` Function

The `print()` function is used to display output on the console.

### 🔹 Basic Usage

```python
print("Hello, World!")
````

**Output**

```
Hello, World!
```

---

### 🔹 Printing Multiple Values

You can print multiple values by separating them with commas.

```python
a = 10
b = 20
print(a, b)
```

**Output**

```
10 20
```

---

### 🔹 Operations Inside `print()`

Mathematical operations can be performed directly inside the `print()` function.

```python
print(3 + 8)
```

**Output**

```
11
```

---

### 🔹 `end` Parameter

By default, `print()` moves to a new line after execution.
This behavior can be changed using the `end` parameter.

```python
print("Hello", end=" ")
print("World")
```

**Output**

```
Hello World
```

---

### 🔹 `sep` Parameter

The `sep` parameter defines how multiple values are separated.

```python
print("2025", "09", "22", sep="-")
```

**Output**

```
2025-09-22
```

---

### 🔹 Escape Sequences

Escape sequences are special characters used inside strings.

| Escape Sequence | Meaning   |
| --------------- | --------- |
| `\n`            | New Line  |
| `\t`            | Tab Space |

```python
print("Python\nProgramming")
print("Python\tProgramming")
```

---

## 📌 2. Input Functionality: `input()` Function

The `input()` function is used to take input from the user.

### 🔹 Basic Input Example

```python
name = input("Enter your name: ")
print("Hello,", name, "! Welcome!")
```

**Sample Output**

```
Enter your name: GeeksforGeeks
Hello, GeeksforGeeks ! Welcome!
```

---

### 🔹 Important Rule of `input()`

* `input()` **always returns data as a string (`str`)**
* Even numeric inputs are treated as strings

```python
x = input("Enter a number: ")
print(type(x))
```

**Output**

```
<class 'str'>
```

---

### 🔹 Typecasting Input

To perform mathematical operations, input must be typecast.

```python
a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
print(a + b)
```

---

## 📌 3. Printing Variables

You can print single or multiple variables using `print()`.

```python
s = "Brad"
print(s)

s = "Anjelina"
age = 25
city = "New York"
print(s, age, city)
```

**Output**

```
Brad
Anjelina 25 New York
```

---

## 📌 4. Taking Multiple Inputs in One Line

Using `split()` method to take multiple values at once.

```python
x, y = input("Enter two values: ").split()
print("Number of boys:", x)
print("Number of girls:", y)
```

```python
x, y, z = input("Enter three values: ").split()
print("Total number of students:", x)
print("Number of boys is:", y)
print("Number of girls is:", z)
```

**Sample Output**

```
Enter two values: 5 10
Number of boys: 5
Number of girls: 10
```

---

## 📌 5. Changing Input Data Type

### 🔹 String Input

```python
color = input("What color is rose?: ")
print(color)
```

---

### 🔹 Integer Input

```python
n = int(input("How many roses?: "))
print(n)
```

---

### 🔹 Float Input

```python
price = float(input("Price of each rose?: "))
print(price)
```

---

## 📌 6. Finding Data Type Using `type()`

The `type()` function is used to identify the data type of a variable.

```python
a = "Hello World"
b = 10
c = 11.22
d = ("Geeks", "for", "Geeks")
e = ["Geeks", "for", "Geeks"]
f = {"Geeks": 1, "for": 2, "Geeks": 3}

print(type(a))
print(type(b))
print(type(c))
print(type(d))
print(type(e))
print(type(f))
```

**Output**

```
<class 'str'>
<class 'int'>
<class 'float'>
<class 'tuple'>
<class 'list'>
<class 'dict'>
```

---

## 🚀 Conclusion

* `print()` helps display output in flexible formats
* `input()` enables interaction with users
* Typecasting is mandatory for numeric calculations
* Understanding input and output is essential for building real-world Python applications

---

