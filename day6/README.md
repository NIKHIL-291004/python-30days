
# Conditional Statements in Python

---

## 1. Introduction to Conditional Statements

Conditional statements in Python are used to **control the flow of execution** of a program. They allow a program to take **different actions** depending on whether a given condition is `True` or `False`.

Conditions are usually formed using:
- Relational operators (`<, >, <=, >=, ==, !=`)
- Logical operators (`and, or, not`)
- Boolean values (`True`, `False`)

Conditional statements make programs:
- Dynamic
- Decision-based
- More intelligent and flexible

---

## 2. Comments in Python

Comments are used to **explain the code** and make it easier to understand. They are ignored by the Python interpreter and do not affect program execution.

### Types of Comments

### Single-Line Comment
```python
# This is a single-line comment
````

### Multi-Line Comment

```python
"""
This is a multi-line comment.
Used to explain large blocks of code.
"""
```

---

## 3. If Conditional Statement

The `if` statement is the **simplest conditional statement**. It executes a block of code **only when the condition evaluates to True**.

### Syntax

```python
if condition:
    statement(s)
```

### Example

```python
age = 20
if age >= 18:
    print("Eligible to vote.")
```

### Output

```
Eligible to vote.
```

📌 If the condition is False, the code inside the `if` block is skipped.

---

## 4. Short-Hand If Statement

Python allows writing a single-line `if` statement when only **one statement** needs to be executed.

### Syntax

```python
if condition: statement
```

### Example

```python
age = 19
if age > 18: print("Eligible to Vote.")
```

### Output

```
Eligible to Vote.
```

📌 This is useful for simple checks but should be avoided for complex logic to maintain readability.

---

## 5. If-Else Conditional Statement

The `if-else` statement allows executing one block of code when the condition is `True`, and another block when it is `False`.

### Syntax

```python
if condition:
    statements
else:
    statements
```

### Example

```python
age = 10
if age <= 12:
    print("Travel for free.")
else:
    print("Pay for ticket.")
```

### Output

```
Travel for free.
```

📌 The `else` block executes only when the `if` condition fails.

---

## 6. Short-Hand If-Else (Ternary Operator)

Python supports a compact way to write `if-else` statements in a **single line**, known as the **ternary operator**.

### Syntax

```python
value_if_true if condition else value_if_false
```

### Example

```python
marks = 45
result = "Pass" if marks >= 40 else "Fail"
print("Result:", result)
```

### Output

```
Result: Pass
```

📌 Ternary operators are best used for **simple conditions**.

---

## 7. Elif Statement

`elif` stands for **else if**. It is used when multiple conditions need to be checked sequentially.

### Syntax

```python
if condition1:
    statements
elif condition2:
    statements
elif condition3:
    statements
else:
    statements
```

### Example

```python
age = 25

if age <= 12:
    print("Child.")
elif age <= 19:
    print("Teenager.")
elif age <= 35:
    print("Young adult.")
else:
    print("Adult.")
```

### Output

```
Young adult.
```

📌 Only the **first True condition** is executed.

---

## 8. Nested If-Else Conditional Statement

A **nested if-else** means an `if` statement inside another `if` statement. It is used when decisions depend on **multiple layers of conditions**.

### Syntax

```python
if condition1:
    if condition2:
        statements
    else:
        statements
else:
    statements
```

### Example

```python
age = 70
is_member = True

if age >= 60:
    if is_member:
        print("30% senior discount!")
    else:
        print("20% senior discount.")
else:
    print("Not eligible for a senior discount.")
```

### Output

```
30% senior discount!
```

📌 Nested conditions should be used carefully to avoid complexity.

---

## 9. Ternary Conditional Statement (Detailed)

The ternary conditional statement assigns a value based on a condition.

### Example

```python
age = 20
status = "Adult" if age >= 18 else "Minor"
print(status)
```

### Output

```
Adult
```

### Explanation

* If `age >= 18` → `"Adult"`
* Otherwise → `"Minor"`

---

## 10. Match-Case Statement (Python 3.10+)

The `match-case` statement is Python’s alternative to the switch-case found in other languages. It allows matching a value against multiple patterns.

### Syntax

```python
match variable:
    case value1:
        statements
    case value2:
        statements
    case _:
        statements
```

### Example

```python
number = 2

match number:
    case 1:
        print("One")
    case 2 | 3:
        print("Two or Three")
    case _:
        print("Other number")
```

### Output

```
Two or Three
```

📌 `_` is the default case.

---

## 11. Comparison Operators Used in Conditions

| Operator | Description           |
| -------- | --------------------- |
| `==`     | Equal to              |
| `!=`     | Not equal to          |
| `>`      | Greater than          |
| `<`      | Less than             |
| `>=`     | Greater than or equal |
| `<=`     | Less than or equal    |

---

## 12. Logical Operators Used in Conditions

| Operator | Description                            |
| -------- | -------------------------------------- |
| `and`    | True if both conditions are True       |
| `or`     | True if at least one condition is True |
| `not`    | Reverses the condition                 |

---

## **practical solved problems** using:
- `if` statement  
- `if-else` statement  
- `if-elif-else` statement  
- Nested `if-else`  
- Ternary operator  
- `match-case` statement  

Each problem includes **code and output** for better understanding.

---

## 1. `if` Statement

The `if` statement checks a condition. If the condition is `True`, the code inside the block executes.

---

### Problem 1: Check if user is eligible to vote

This program checks whether a person is eligible to vote based on age.

```python
age = int(input("Enter your age: "))
if age >= 18:
    print("You are eligible to vote.")
````

**Output:**

```
Enter your age: 22
You are eligible to vote.
```

---

### Problem 2: Check if a number is positive

This program checks if the entered number is positive.

```python
num = int(input("Enter a number: "))
if num > 0:
    print("The number is positive.")
```

**Output:**

```
Enter a number: 4
The number is positive.
```

---

## 2. `if-else` Statement

The `if-else` statement executes one block if the condition is `True` and another block if it is `False`.

---

### Problem 1: Check pass or fail in exam

This program checks whether a student has passed based on marks.

```python
marks = int(input("Enter your marks: "))

if marks >= 40:
    print("You passed the exam.")
else:
    print("You failed the exam.")
```

**Output:**

```
Enter your marks: 98
You passed the exam.
```

---

### Problem 2: Check if user can buy an item

This program checks whether the user has enough balance to buy an item.

```python
balance = float(input("Enter your balance: "))
price = float(input("Enter the item price: "))

if balance >= price:
    print("Purchase successful.")
else:
    print("Insufficient funds.")
```

**Output:**

```
Enter your balance: 100.50
Enter the item price: 56.55
Purchase successful.
```

---

## 3. `if-elif-else` Statement

The `if-elif-else` statement is used to test **multiple conditions** in sequence.

---

### Problem 1: Suggest transport based on distance

```python
distance = float(input("Enter the distance to your destination (in km): "))

if distance <= 2:
    print("You can walk.")
elif distance <= 10:
    print("Use a bicycle or scooter.")
elif distance <= 50:
    print("Take a car or public transport.")
else:
    print("Consider a train or flight.")
```

**Output:**

```
Enter the distance to your destination (in km): 240
Consider a train or flight.
```

---

### Problem 2: Battery status check

```python
battery = int(input("Enter battery percentage: "))

if battery > 80:
    print("Battery Full")
elif battery > 40:
    print("Battery Half")
else:
    print("Battery Low")
```

**Output:**

```
Enter battery percentage: 55
Battery Half
```

---

## 4. Nested `if-else` Statement

Nested `if-else` statements are used when decisions depend on previous conditions.

---

### Problem 1: Login authentication

```python
username = input("Enter username: ")
password = input("Enter password: ")

if username == "admin":
    if password == "1234":
        print("Access granted")
    else:
        print("Incorrect password")
else:
    print("Username not found")
```

**Output:**

```
Enter username: admin
Enter password: 12345
Incorrect password
```

---

### Problem 2: Exam result and scholarship eligibility

```python
marks = int(input("Enter your marks: "))

if marks >= 50:
    if marks >= 80:
        print("Passed with scholarship")
    else:
        print("Passed without scholarship")
else:
    print("Failed")
```

**Output:**

```
Enter your marks: 89
Passed with scholarship
```

---

## 5. Ternary Operator

The ternary operator is a **short-hand if-else** written in a single line.

---

### Problem 1: Check if number is even or odd

```python
num = int(input("Enter a number: "))
print("Even" if num % 2 == 0 else "Odd")
```

**Output:**

```
Enter a number: 77
Odd
```

---

### Problem 2: Compare two numbers

```python
a = int(input("Enter value of a: "))
b = int(input("Enter value of b: "))

print("a is greater" if a > b else "b is greater")
```

**Output:**

```
Enter value of a: 33
Enter value of b: 12
a is greater
```

---

### Problem 3: Temperature check

```python
temp = int(input("Enter the temperature: "))
print("Hot" if temp > 25 else "Cool")
```

**Output:**

```
Enter the temperature: 33
Hot
```

---

## 6. `match-case` Statement (Python 3.10+)

The `match-case` statement is Python’s alternative to switch-case and improves readability.

---

### Problem 1: Grade evaluation

```python
grade = input("Enter your grade (A/B/C): ").upper()

match grade:
    case "A":
        print("Excellent")
    case "B":
        print("Good")
    case "C":
        print("Average")
    case _:
        print("Fail")
```

**Output:**

```
Enter your grade (A/B/C): A
Excellent
```

---

### Problem 2: Activity suggestion based on weather

```python
weather = input("Enter the weather (sunny/rainy/cloudy/snowy): ").lower()

match weather:
    case "sunny":
        print("Great day for a picnic!")
    case "rainy":
        print("Stay indoors and read a book.")
    case "cloudy":
        print("Perfect time for a walk.")
    case "snowy":
        print("Build a snowman or go skiing!")
    case _:
        print("Unknown weather condition.")
```

**Output:**

```
Enter the weather (sunny/rainy/cloudy/snowy): sunny
Great day for a picnic!
```

---

### Problem 3: Mobile notification mode

```python
mode = input("Enter phone mode (silent/vibrate/loud/do not disturb): ").lower()

match mode:
    case "silent":
        print("Notifications are muted.")
    case "vibrate":
        print("Phone will vibrate for notifications.")
    case "loud":
        print("All notifications will play sound.")
    case "do not disturb":
        print("No calls or notifications will come through.")
    case _:
        print("Invalid mode selected.")
```

**Output:**

```
Enter phone mode (silent/vibrate/loud/do not disturb): loud
All notifications will play sound.
```

---

### Exercises: Level 1

1. Get user input using input(“Enter your age: ”). If user is 18 or older, give feedback: You are old enough to drive. If below 18 give feedback to wait for the missing amount of years. Output:

    ```sh
    Enter your age: 30
    You are old enough to learn to drive.
    Output:
    Enter your age: 15
    You need 3 more years to learn to drive.
    ```

2. Compare the values of my_age and your_age using if … else. Who is older (me or you)? Use input(“Enter your age: ”) to get the age as input. You can use a nested condition to print 'year' for 1 year difference in age, 'years' for bigger differences, and a custom text if my_age = your_age. Output:

    ```sh
    Enter your age: 30
    You are 5 years older than me.
    ```

3. Get two numbers from the user using input prompt. If a is greater than b return a is greater than b, if a is less b return a is smaller than b, else a is equal to b. Output:

```sh
Enter number one: 4
Enter number two: 3
4 is greater than 3
```

### Exercises: Level 2

   1. Write a code which gives grade to students according to theirs scores:

        ```sh
        80-100, A
        70-89, B
        60-69, C
        50-59, D
        0-49, F
        ```

   1. Check if the season is Autumn, Winter, Spring or Summer. If the user input is:
    September, October or November, the season is Autumn.
    December, January or February, the season is Winter.
    March, April or May, the season is Spring
    June, July or August, the season is Summer
   2. The following list contains some fruits:

    ```sh
    fruits = ['banana', 'orange', 'mango', 'lemon']
    ```

    If a fruit doesn't exist in the list add the fruit to the list and print the modified list. If the fruit exists print('That fruit already exist in the list')

### Exercises: Level 3

   1. Here we have a person dictionary. Feel free to modify it!

```py
        person={
    'first_name': 'Asabeneh',
    'last_name': 'Yetayeh',
    'age': 250,
    'country': 'Finland',
    'is_marred': True,
    'skills': ['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address': {
        'street': 'Space street',
        'zipcode': '02210'
    }
    }
```

     * Check if the person dictionary has skills key, if so print out the middle skill in the skills list.
     * Check if the person dictionary has skills key, if so check if the person has 'Python' skill and print out the result.
     * If a person skills has only JavaScript and React, print('He is a front end developer'), if the person skills has Node, Python, MongoDB, print('He is a backend developer'), if the person skills has React, Node and MongoDB, Print('He is a fullstack developer'), else print('unknown title') - for more accurate results more conditions can be nested!
     * If the person is married and if he lives in Finland, print the information in the following format:

```py
