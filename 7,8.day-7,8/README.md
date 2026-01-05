
# 🐍 Python Loops – For, While & Nested Loops

## 📌 Introduction
Loops in Python are used to **repeat a block of code multiple times efficiently**.  
Instead of writing the same code again and again, loops help us automate repetitive tasks.

Python mainly provides:
- **For Loop** – used to iterate over sequences
- **While Loop** – runs based on a condition
- **Nested Loops** – one loop inside another
- **Loop Control Statements** – break, continue, pass

---

## 🔁 For Loop
A **for loop** is used to iterate over a sequence such as a **list, tuple, string, set, dictionary, or range**.

### Example: Printing Numbers Using `range()`
```python
n = 4
for i in range(0, n):
    print(i)
````

### Output

```
0
1
2
3
```

### Explanation

* `range(0, n)` generates numbers from `0` to `n-1`
* The loop runs once for each value

---

## 🔄 Iterating Over Different Data Types

### List, Tuple, String, Dictionary, and Set

```python
li = ["geeks", "for", "geeks"]
for x in li:
    print(x)

tup = ("geeks", "for", "geeks")
for x in tup:
    print(x)

s = "abc"
for x in s:
    print(x)

d = {'x': 123, 'y': 354}
for x in d:
    print("%s  %d" % (x, d[x]))

set1 = {10, 30, 20}
for x in set1:
    print(x)
```

### Output

```
geeks
for
geeks
geeks
for
geeks
a
b
c
x  123
y  354
10
20
30
```

---

## 🔢 Iterating Using Index

We can also iterate using the **index position**.

```python
li = ["geeks", "for", "geeks"]
for index in range(len(li)):
    print(li[index])
```

### Output

```
geeks
for
geeks
```

---

## 🔁 While Loop

A **while loop** executes as long as the given condition is `True`.

### Example

```python
cnt = 0
while cnt < 3:
    cnt = cnt + 1
    print("Hello Geek")
```

### Output

```
Hello Geek
Hello Geek
Hello Geek
```

### Explanation

* The loop runs until `cnt < 3` becomes false
* Counter increases in each iteration

---

## ♾ Infinite While Loop

```python
while True:
    print("Hello Geek")
```

⚠️ **Note:**
This loop runs forever unless interrupted using `break`.
Avoid using infinite loops without a proper exit condition.

---

## 🔂 Nested Loops

A **nested loop** means a loop inside another loop.

### Example

```python
for i in range(1, 5):
    for j in range(i):
        print(i, end=' ')
    print()
```

### Output

```
1
2 2
3 3 3
4 4 4 4
```

### Explanation

* Outer loop controls rows
* Inner loop controls columns
* Each row prints the value of `i` multiple times

---

## 🧭 Loop Control Statements

Loop control statements change the normal flow of loops.

---

### 🔹 Continue Statement

Skips the current iteration and continues with the next one.

```python
for letter in 'geeksforgeeks':
    if letter == 'e' or letter == 's':
        continue
    print('Current Letter :', letter)
```

### Output

```
Current Letter : g
Current Letter : k
Current Letter : f
Current Letter : o
Current Letter : r
Current Letter : g
Current Letter : k
```

---

### 🔹 Break Statement

Terminates the loop completely.

```python
for letter in 'geeksforgeeks':
    if letter == 'e' or letter == 's':
        break
print('Current Letter :', letter)
```

### Output

```
Current Letter : e
```

---

### 🔹 Pass Statement

Used when a statement is syntactically required but no action is needed.

```python
for letter in 'geeksforgeeks':
    pass
print('Last Letter :', letter)
```

### Output

```
Last Letter : s
```

# 🐍 Using `else` with Loops in Python

## 📌 Introduction
In most programming languages like **C, C++ or Java**, the `else` statement is used only with `if`.  
However, **Python allows `else` to be used with loops (`for` and `while`)**.

👉 The `else` block associated with a loop is executed **only when the loop finishes normally**,  
that is, **without encountering a `break` statement**.

---

## 🔁 `else` with `for` Loop

### Example 1: `else` block EXECUTED
```python
for i in range(1, 4):
    print(i)
else:  # Executed because no break is used
    print("No Break")
````

### Output

```
1
2
3
No Break
```

### Explanation

* The loop completes all iterations
* No `break` is encountered
* Hence, the `else` block is executed

---

### Example 2: `else` block NOT executed

```python
for i in range(1, 4):
    print(i)
    break
else:  # Not executed because break is used
    print("No Break")
```

### Output

```
1
```

### Explanation

* The loop stops due to `break`
* The `else` block is skipped

---

## 🎯 When is `else` with Loop Useful?

Using `else` with loops is useful when:

* There is an `if` condition inside the loop
* We want to perform an action **only if the condition never becomes true**
* In other words, **when `break` is never executed**

---

## 🧮 Example: Check if a List Contains an Even Number

```python
# Python program to check if a list contains an even number
def contains_even_number(l):
    for ele in l:
        if ele % 2 == 0:
            print("list contains an even number")
            break
    else:
        # Executed only if break is NEVER reached
        print("list does not contain an even number")

# Driver code
print("For List 1:")
contains_even_number([1, 9, 8])

print("\nFor List 2:")
contains_even_number([1, 3, 5])
```

### Output

```
For List 1:
list contains an even number

For List 2:
list does not contain an even number
```

### Explanation

* In List 1 `[1, 9, 8]`, an even number is found → `break` executes → `else` skipped
* In List 2 `[1, 3, 5]`, no even number → loop completes → `else` executes

---

## 🔁 `else` with `while` Loop

### Example

```python
count = 0
while count < 1:
    count = count + 1
    print(count)
    break
else:
    print("No Break")
```

### Output

```
1
```

### Explanation

* The loop is terminated using `break`
* Hence, the `else` block is NOT executed


# 🐍 Practice Problems of Loops in Python

## 📌 Introduction
Loops in Python are used to **repeat a block of code multiple times**, making programs efficient and readable.  
In real life, we repeat actions like checking emails, counting items, or waiting for a timer — loops bring this repetition into programming.

This repository focuses on **real-world practice problems** using:
- `for` loops
- `while` loops
- Nested loops
- Loop control statements (`break`, `continue`, `pass`)

---

## 🔁 For Loops
A **for loop** is used to iterate over sequences such as **lists, strings, and ranges**.  
It is best used when the number of iterations is known in advance.

---

### 🛒 Problem 1: Print Each Item in a Shopping List
```python
items = input("Enter shopping items separated by commas: ").split(',')

for item in items:
    print("Buy:", item.strip())
````

#### Output

```
Enter shopping items separated by commas: milk, bread, eggs, avacado, oats
Buy: milk
Buy: bread
Buy: eggs
Buy: avacado
Buy: oats
```

---

### 🔢 Problem 2: Print Squares of Numbers from 1 to n

```python
n = int(input("Enter a number: "))

for i in range(1, n + 1):
    print("Square of", i, "is", i**2)
```

#### Output

```
Enter a number: 4
Square of 1 is 1
Square of 2 is 4
Square of 3 is 9
Square of 4 is 16
```

---

## 🔁 While Loop

A **while loop** runs as long as a given condition is `True`.
It is useful when the number of iterations is **not known in advance**.

---

### ⏳ Problem 1: Countdown Timer

```python
seconds = int(input("Enter countdown time in seconds: "))

while seconds > 0:
    print("Time left:", seconds)
    seconds -= 1
```

#### Output

```
Enter countdown time in seconds: 5
Time left: 5
Time left: 4
Time left: 3
Time left: 2
Time left: 1
```

---

### ➕ Problem 2: Sum Until User Enters 0

```python
total = 0
num = int(input("Enter number (0 to stop): "))

while num != 0:
    total += num
    num = int(input("Enter number (0 to stop): "))

print("Total sum:", total)
```

#### Output

```
Enter number (0 to stop): 22
Enter number (0 to stop): 44
Enter number (0 to stop): 0
Total sum: 66
```

---

## 🔂 Nested For Loops

A **nested loop** is a loop inside another loop.
It is useful for **tables, matrices, and patterns**.

---

### ✖️ Problem 1: Multiplication Table

```python
n = 3

for i in range(1, n + 1):
    for j in range(1, 11):
        print(i * j, end=' ')
    print()
```

#### Output

```
1 2 3 4 5 6 7 8 9 10
2 4 6 8 10 12 14 16 18 20
3 6 9 12 15 18 21 24 27 30
```

---

### 🧮 Problem 2: Identity Matrix Pattern

```python
n = 4

for i in range(n):
    for j in range(n):
        if i == j:
            print("1", end=" ")
        else:
            print("0", end=" ")
    print()
```

#### Output

```
1 0 0 0
0 1 0 0
0 0 1 0
0 0 0 1
```

---

## 🎯 Control Flow Statements in Loops

Control flow statements change the normal execution of loops.

---

## 🔴 `break` Statement

The `break` statement exits the loop immediately.

### Problem 1: Stop Printing at a Target Item

```python
items = ["apple", "banana", "cherry", "stop", "mango"]

for item in items:
    if item == "stop":
        break
    print("Item:", item)
```

#### Output

```
Item: apple
Item: banana
Item: cherry
```

---

### Problem 2: Find First Even Number

```python
while True:
    num = int(input("Enter a number: "))
    if num % 2 == 0:
        print("First even number found:", num)
        break
```

#### Output

```
Enter a number: 3
Enter a number: 5
Enter a number: 6
First even number found: 6
```

---

## 🟡 `continue` Statement

The `continue` statement skips the current iteration.

### Problem 1: Skip Out-of-Stock Items

```python
items = ["milk", "bread", "out of stock", "eggs"]

for item in items:
    if item == "out of stock":
        continue
    print("Buy:", item)
```

#### Output

```
Buy: milk
Buy: bread
Buy: eggs
```

---

### Problem 2: Skip Even Numbers

```python
n = 10

for i in range(1, n + 1):
    if i % 2 == 0:
        continue
    print("Odd number:", i)
```

#### Output

```
Odd number: 1
Odd number: 3
Odd number: 5
Odd number: 7
Odd number: 9
```

---

## ⚪ `pass` Statement

The `pass` statement does nothing.
It is used as a **placeholder** where code will be added later.

---

### Problem 1: Pass for Future Implementation

```python
tasks = ["email", "meeting", "call"]

for task in tasks:
    if task == "call":
        pass
    print("Do:", task)
```

#### Output

```
Do: email
Do: meeting
Do: call
```

---

### Problem 2: Empty Loop Using `pass`

```python
for i in range(5):
    pass  # Placeholder for future logic
```

### Exercises: Level 1

1. Iterate 0 to 10 using for loop, do the same using while loop.
2. Iterate 10 to 0 using for loop, do the same using while loop.
3. Write a loop that makes seven calls to print(), so we get on the output the following triangle:

   ```py
     #
     ##
     ###
     ####
     #####
     ######
     #######
   ```

4. Use nested loops to create the following:

   ```sh
   # # # # # # # #
   # # # # # # # #
   # # # # # # # #
   # # # # # # # #
   # # # # # # # #
   # # # # # # # #
   # # # # # # # #
   # # # # # # # #
   ```

5. Print the following pattern:

   ```sh
   0 x 0 = 0
   1 x 1 = 1
   2 x 2 = 4
   3 x 3 = 9
   4 x 4 = 16
   5 x 5 = 25
   6 x 6 = 36
   7 x 7 = 49
   8 x 8 = 64
   9 x 9 = 81
   10 x 10 = 100
   ```

6. Iterate through the list, ['Python', 'Numpy','Pandas','Django', 'Flask'] using a for loop and print out the items.
7. Use for loop to iterate from 0 to 100 and print only even numbers
8. Use for loop to iterate from 0 to 100 and print only odd numbers
   
### Exercises: Level 2
    
1.  Use for loop to iterate from 0 to 100 and print the sum of all numbers.

   ```sh
   The sum of all numbers is 5050.
   ```

2. Use for loop to iterate from 0 to 100 and print the sum of all evens and the sum of all odds.

    ```sh
    The sum of all evens is 2550. And the sum of all odds is 2500.
    ```


# 🐍 Exercises: Level 3 – Python Practice Questions

This section contains **Level 3 practice questions** designed to strengthen your understanding of **loops, strings, numbers, and pattern logic** in Python.
Attempt all questions **without looking at solutions first**.

---

## 🔢 1: Jumping Through While Loop

**Problem Statement:**
Given a positive integer **x**, print the numbers from `1` to `x` in the order of squares:
1², 2², 3², 4², … (in increasing order), such that the square value is **less than or equal to x**.

**Example:**
Input: `x = 10`
Output: `1 4 9`

**Explanation:**
From 1 to 10, numbers that are perfect squares are 1², 2², and 3².

**Constraints:**

* 2 ≤ x ≤ 10³

---

## ✖️ 2: Multiplication Table in a Single Line

**Problem Statement:**
You are given a number **n**. Take input of `n` and print its multiplication table **up to n × 10** in a **single line** using a `for` loop.

**Examples:**
Input: `n = 5`
Output: `5 10 15 20 25 30 35 40 45 50`

Input: `n = 6`
Output: `6 12 18 24 30 36 42 48 54 60`

**Constraints:**

* 1 ≤ n ≤ 10

---

## 🔤 3: Characters at Even Indices

**Problem Statement:**
You are given a string **s**. Print the characters that are present at **even indices** (index starts from 0).

**Note:**
Use the `range()` function to jump indices by 2.

**Examples:**
Input: `s = "DoctorPhenomenal"`
Output: `DcoPeoea`

Input: `s = "Geeks"`
Output: `Ges`

---

## 🔽 4: Print Numbers in Decreasing Order

**Problem Statement:**
Given a number **x**, print the numbers from `x` to `0` in **decreasing order** in a single line.

**Example:**
Input: `x = 3`
Output: `3 2 1 0`

**Explanation:**
Numbers printed are from `x` down to `0`.

---

## 🧮 5: Factorial of a Number

**Problem Statement:**
Given a positive integer **n**, find and print the **factorial** of `n`.

**Examples:**
Input: `n = 5`
Output: `120`

Input: `n = 4`
Output: `24`

**Constraints:**

* 0 ≤ n ≤ 12

---

## ⭐ 6: Square Pattern Using `*`

**Problem Statement:**
Given an integer **n**, print a **square pattern of size n** using the `*` character.

**Examples:**

Input: `n = 4`
Output:

```
* * * *
*     *
*     *
* * * *
```

Input: `n = 3`
Output:

```
* * *
*   *
* * *
```

**Constraints:**

* 1 ≤ n ≤ 10

---






