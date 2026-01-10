# 🐍 Python Recursion & Decorators – Complete Notes

---

## 📌 1. Recursion in Python

**Recursion** is a programming technique where a function calls itself to solve a problem by breaking it into smaller subproblems.

### ✅ When to Use Recursion

* Mathematical problems (factorial, Fibonacci)
* Tree & graph traversal
* Divide-and-conquer algorithms

---

## 📌 2. Structure of a Recursive Function

```python
def recursive_function(parameters):
    if base_condition:
        return result
    else:
        return recursive_function(modified_parameters)
```

### 🔑 Key Parts

* **Base Case** → Stops recursion
* **Recursive Case** → Calls itself with smaller input

---

## 📌 3. Example: Factorial Using Recursion

```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))
```

**Output**

```
120
```

### Explanation

* Base case: `n == 0`
* Recursive case: `n * factorial(n-1)`

---

## 📌 4. Example: Fibonacci Using Recursion

```python
def fibonacci(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci(n-1) + fibonacci(n-2)

print(fibonacci(10))
```

**Output**

```
55
```

---

## 📌 5. Types of Recursion

### 🔹 Tail Recursion

Recursive call is the **last operation**.

```python
def tail_fact(n, acc=1):
    if n == 0:
        return acc
    return tail_fact(n-1, acc * n)
```

---

### 🔹 Non-Tail Recursion

Some work is done **after recursive call**.

```python
def nontail_fact(n):
    if n == 1:
        return 1
    return n * nontail_fact(n-1)
```

---

## 📌 6. Recursion vs Iteration

| Feature     | Recursion       | Iteration |
| ----------- | --------------- | --------- |
| Readability | High            | Medium    |
| Memory      | Uses call stack | Efficient |
| Risk        | Stack overflow  | Low       |
| Speed       | Slower          | Faster    |

---

## 📌 7. When to Avoid Recursion

* Large recursion depth
* Performance-critical code
* Problems easily solved with loops

---

# 🎯 Python Decorators

## 📌 8. What is a Decorator?

A **decorator** is a function that modifies another function **without changing its code**.

### Uses

* Logging
* Authentication
* Caching
* Rate limiting

---

## 📌 9. Basic Decorator Example

```python
def decorator(func):
    def wrapper():
        print("Before calling the function.")
        func()
        print("After calling the function.")
    return wrapper

@decorator
def greet():
    print("Hello, World!")

greet()
```

**Output**

```
Before calling the function.
Hello, World!
After calling the function.
```

---

## 📌 10. Decorator with Parameters

```python
def decorator_name(func):
    def wrapper(*args, **kwargs):
        print("Before execution")
        result = func(*args, **kwargs)
        print("After execution")
        return result
    return wrapper

@decorator_name
def add(a, b):
    return a + b

print(add(5, 3))
```

**Output**

```
Before execution
After execution
8
```

---

## 📌 11. Functions as First-Class Objects

Python functions can be:

* Assigned to variables
* Passed as arguments
* Returned from functions

```python
def greet(name):
    return f"Hello, {name}"

say_hi = greet
print(say_hi("Alice"))
```

**Output**

```
Hello, Alice
```

---

## 📌 12. Higher-Order Functions

A function that **takes another function as argument or returns one**.

```python
def apply(f, x):
    return f(x)

def square(n):
    return n * n

print(apply(square, 5))
```

**Output**

```
25
```

---

## 📌 13. Decorators as Higher-Order Functions

Decorators:

* Take a function
* Return a modified function
* Replace original function name

---

## 📌 14. Types of Decorators

### 🔹 Function Decorator

```python
def simple_decorator(func):
    def wrapper():
        print(">>> Starting")
        func()
        print(">>> Finished")
    return wrapper
```

---

### 🔹 Method Decorator

```python
def method_decorator(func):
    def wrapper(self):
        print("Before method")
        func(self)
        print("After method")
    return wrapper
```

---

### 🔹 Class Decorator

```python
def add_class_name(cls):
    cls.class_name = cls.__name__
    return cls

@add_class_name
class Person:
    pass

print(Person.class_name)
```

**Output**

```
Person
```

---

## 📌 15. Built-in Decorators

### 🔹 @staticmethod

```python
class Math:
    @staticmethod
    def add(a, b):
        return a + b

print(Math.add(3, 5))
```

---

### 🔹 @classmethod

```python
class Employee:
    raise_amount = 1.05

    @classmethod
    def set_raise(cls, amt):
        cls.raise_amount = amt
```

---

### 🔹 @property

```python
class Circle:
    def __init__(self, r):
        self._r = r

    @property
    def area(self):
        return 3.14 * self._r ** 2
```

---

## 📌 16. Chaining Decorators

```python
@decor1
@decor2
def num():
    return 10
```

➡ Order matters!



# Exercise:

---

## 1️⃣ Factorial of a Number

Given a **non-negative integer `n`**, find the **factorial of `n`**.

The factorial of a number is defined as the product of all positive integers less than or equal to `n`.

### Examples

* Input: `n = 5`
  Explanation: `1 × 2 × 3 × 4 × 5`
* Input: `n = 4`
  Explanation: `1 × 2 × 3 × 4`

### Constraints

* `0 ≤ n ≤ 12`

---

## 2️⃣ Print Numbers from 1 to N (Without Using Loops)

Given a **positive integer `n`**, print numbers from **1 to `n`** **without using loops**.

Implement a function `printTillN()` to print numbers from `1` to `n` as **space-separated integers**.

### Examples

* Input: `n = 5`
  Explanation: Print numbers from 1 to 5
* Input: `n = 10`
  Explanation: Print numbers from 1 to 10

### Constraints

* `1 ≤ n ≤ 1000`

---

## 3️⃣ Nth Fibonacci Number

Given a **non-negative integer `n`**, find the **nth Fibonacci number**.

The Fibonacci sequence is defined as:

* `F(0) = 0`
* `F(1) = 1`
* `F(n) = F(n − 1) + F(n − 2)` for `n > 1`

Sequence example:
`0, 1, 1, 2, 3, 5, 8, 13, 21, ...`

### Examples

* Input: `n = 5`
  Explanation: The 5th Fibonacci number
* Input: `n = 0`
  Explanation: The 0th Fibonacci number
* Input: `n = 1`
  Explanation: The 1st Fibonacci number

### Constraints

* `0 ≤ n ≤ 30`

---

## 4️⃣ Majority Element in an Array

Given an array `arr[]`, find the **majority element**.

A **majority element** is an element that appears **strictly more than `arr.size() / 2` times**.

If no such element exists, return `-1`.

### Examples

* Input: `arr[] = [1, 1, 2, 1, 3, 5, 1]`
  Explanation: `1` appears more than `7/2` times
* Input: `arr[] = [7]`
  Explanation: Single element is majority
* Input: `arr[] = [2, 13]`
  Explanation: No majority element exists

### Constraints

* `1 ≤ arr.size() ≤ 10⁵`
* `1 ≤ arr[i] ≤ 10⁵`

