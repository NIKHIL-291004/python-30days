
# 🧵 Python Strings – Complete & Detailed Notes

---

## 📌 1. What is a String in Python?
In Python, a **string** is a sequence of characters used to store and manipulate text data.

✔ Any data enclosed within:
- Single quotes `' '`
- Double quotes `" "`
- Triple quotes `''' '''` or `""" """`

is treated as a **string**.

📌 Python does **not** have a separate `char` data type.  
Even a **single character** is considered a string of length **1**.

---

## 🧱 2. Creating Strings

### 🔹 Single & Double Quotes
```python
s1 = 'GfG'
s2 = "GfG"
print(s1)
print(s2)
````

**Output**

```
GfG
GfG
```

---

### 🔹 Single Character String

```python
letter = 'P'
print(letter)
print(len(letter))
```

**Output**

```
P
1
```

---

## 🧾 3. Multi-Line Strings

Used when text spans multiple lines.
Created using **triple quotes**.

```python
text = """I am learning Python.
Strings are immutable.
They are very powerful."""
print(text)
```

✔ Newlines are preserved automatically.

---

## 🔗 4. String Concatenation

Joining two or more strings using `+` operator.

```python
first_name = "Asabeneh"
last_name = "Yetayeh"
full_name = first_name + " " + last_name
print(full_name)
```

**Output**

```
Asabeneh Yetayeh
```

---

## 📏 5. Length of a String

The `len()` function returns total characters (including spaces).

```python
text = "Hello World"
print(len(text))
```

**Output**

```
11
```

---

## 🔐 6. Escape Sequences

Escape sequences are special characters preceded by `\`.

| Escape | Meaning      |
| ------ | ------------ |
| `\n`   | New Line     |
| `\t`   | Tab Space    |
| `\\`   | Backslash    |
| `\"`   | Double Quote |
| `\'`   | Single Quote |

```python
print("Hello\nWorld")
print("Day\tTopic")
print("This is a backslash \\")
```

---

## 🎨 7. String Formatting

### 7.1 Old Style Formatting (`%`)

```python
name = "Asabeneh"
age = 250
print("I am %s and I am %d years old." % (name, age))
```

---

### 7.2 `str.format()` Method

```python
a, b = 4, 3
print("{} + {} = {}".format(a, b, a + b))
print("{} / {} = {:.2f}".format(a, b, a / b))
```

---

### 7.3 f-Strings (Python 3.6+) ✅

✔ Most recommended and readable

```python
name = "Alice"
age = 22
print(f"Name: {name}, Age: {age}")
```

---

## 🔡 8. Accessing Characters in a String

### 🔹 Positive Indexing

```python
s = "Python"
print(s[0])   # P
print(s[3])   # h
```

### 🔹 Negative Indexing

```python
print(s[-1])  # n
print(s[-2])  # o
```

📌 Indexing starts from **0** (left) and **-1** (right).

---

## ✂️ 9. String Slicing

Extract a portion of string using slicing.

```python
s = "Python"
print(s[0:3])   # Pyt
print(s[3:])    # hon
print(s[-3:])   # hon
```

---

## 🔄 10. Reversing a String

```python
s = "Hello"
print(s[::-1])
```

**Output**

```
olleH
```

---

## 🔁 11. Iterating Through a String

```python
for char in "Python":
    print(char)
```

---

## 🔒 12. String Immutability

Strings **cannot be changed directly**.

❌ This is invalid:

```python
s[0] = 'P'
```

✅ Correct way:

```python
s = "python"
s = "P" + s[1:]
print(s)
```

---

## 🧹 13. Updating & Deleting Strings

### 🔹 Updating

```python
s = "hello geeks"
s = s.replace("geeks", "GeeksforGeeks")
print(s)
```

### 🔹 Deleting

```python
s = "GfG"
del s
```

---

## 🧠 14. Important String Methods

### 🔹 Case Methods

```python
s = "python"
print(s.upper())
print(s.lower())
print(s.title())
print(s.swapcase())
```

---

### 🔹 Checking Methods

```python
print("123".isdigit())
print("abc".isalpha())
print("abc123".isalnum())
print("var_name".isidentifier())
```

---

### 🔹 Searching Methods

```python
s = "thirty days of python"
print(s.find("python"))
print(s.count("y"))
```

---

### 🔹 Split & Join

```python
s = "python is fun"
print(s.split())

langs = ["Python", "Java", "C"]
print(" | ".join(langs))
```

---

### 🔹 Strip

```python
s = "   hello   "
print(s.strip())
```

---

## 🔍 15. Membership Operators

```python
s = "GeeksforGeeks"
print("Geeks" in s)
print("Java" in s)
```

---

## Exercises
## 📌 Problem 1: Convert String to Lowercase

### 📝 Problem Statement
Given a string `s`, convert **all uppercase characters** in the string to **lowercase**.

### 🔢 Examples
Input: s = "ABCddE"
Output: "abcdde"

Input: s = "LMNOppQQ"
Output: "lmnoppqq"

yaml
Copy code

### 📋 Constraints
- 1 ≤ |s| ≤ 10⁶

---

## 📌 Problem 2: Reverse a String

### 📝 Problem Statement
Given a string `s`, reverse the string and return the reversed result.

### 🔢 Examples
Input: s = "Hello"
Output: "olleH"

Input: s = "World"
Output: "dlroW"

yaml
Copy code

---

## 📌 Problem 3: Check Palindrome (Case-Insensitive)

### 📝 Problem Statement
Given a string `s`, check whether it is a **palindrome**.

📌 A palindrome is a string that reads the same forward and backward.  
📌 **Ignore character case** while checking.

### 🔢 Examples
Input: s = "Hello"
Output: false

Input: s = "TenEt"
Output: true

pgsql
Copy code

---

## 📌 Problem 4: Sum of Two Large Numbers

### 📝 Problem Statement
Given two strings `s1` and `s2` representing **non-negative integers**, compute their **sum** and return it as a string.

📌 The numbers can be very large, so direct integer conversion may not be allowed.

### 🔢 Examples
Input: s1 = "25", s2 = "23"
Output: "48"

Input: s1 = "2500", s2 = "23"
Output: "2523"

Input: s1 = "2", s2 = "3"
Output: "5"

yaml
Copy code

### 📋 Constraints
- 1 ≤ |s1|, |s2| ≤ 10⁵

---

## extra problems
1. Concatenate the string 'Thirty', 'Days', 'Of', 'Python' to a single string, 'Thirty Days Of Python'.
2. Concatenate the string 'Coding', 'For' , 'All' to a single string, 'Coding For All'.
3. Declare a variable named company and assign it to an initial value "Coding For All".
4. Print the variable company using _print()_.
5. Print the length of the company string using _len()_ method and _print()_.
6. Change all the characters to uppercase letters using _upper()_ method.
7. Change all the characters to lowercase letters using _lower()_ method.
8. Use capitalize(), title(), swapcase() methods to format the value of the string _Coding For All_.
9. Cut(slice) out the first word of _Coding For All_ string.
10. Check if _Coding For All_ string contains a word Coding using the method index, find or other methods.
11. Replace the word coding in the string 'Coding For All' to Python.
12. Change Python for Everyone to Python for All using the replace method or other methods.
13. Split the string 'Coding For All' using space as the separator (split()) .
14. "Facebook, Google, Microsoft, Apple, IBM, Oracle, Amazon" split the string at the comma.
15. What is the character at index 0 in the string _Coding For All_.
16. What is the last index of the string _Coding For All_.
17. What character is at index 10 in "Coding For All" string.
18. Create an acronym or an abbreviation for the name 'Python For Everyone'.
19. Create an acronym or an abbreviation for the name 'Coding For All'.
20. Use index to determine the position of the first occurrence of C in Coding For All.
21. Use index to determine the position of the first occurrence of F in Coding For All.
22. Use rfind to determine the position of the last occurrence of l in Coding For All People.
23. Use index or find to find the position of the first occurrence of the word 'because' in the following sentence: 'You cannot end a sentence with because because because is a conjunction'
24. Use rindex to find the position of the last occurrence of the word because in the following sentence: 'You cannot end a sentence with because because because is a conjunction'
25. Slice out the phrase 'because because because' in the following sentence: 'You cannot end a sentence with because because because is a conjunction'
26. Find the position of the first occurrence of the word 'because' in the following sentence: 'You cannot end a sentence with because because because is a conjunction'
27. Slice out the phrase 'because because because' in the following sentence: 'You cannot end a sentence with because because because is a conjunction'
28. Does '\'Coding For All' start with a substring _Coding_?
29. Does 'Coding For All' end with a substring _coding_?
30. '&nbsp;&nbsp; Coding For All &nbsp;&nbsp;&nbsp; &nbsp;' &nbsp;, remove the left and right trailing spaces in the given string.
31. Which one of the following variables return True when we use the method isidentifier():
    - 30DaysOfPython
    - thirty_days_of_python
32. The following list contains the names of some of python libraries: ['Django', 'Flask', 'Bottle', 'Pyramid', 'Falcon']. Join the list with a hash with space string.
33. Use the new line escape sequence to separate the following sentences.
    ```py
    I am enjoying this challenge.
    I just wonder what is next.
    ```
34. Use a tab escape sequence to write the following lines.
    ```py
    Name      Age     Country   City
    Asabeneh  250     Finland   Helsinki
    ```
35. Use the string formatting method to display the following:

```sh
radius = 10
area = 3.14 * radius ** 2
The area of a circle with radius 10 is 314 meters square.
```

36. Make the following using string formatting methods:

```sh
8 + 6 = 14
8 - 6 = 2
8 * 6 = 48
8 / 6 = 1.33
8 % 6 = 2
8 // 6 = 1
8 ** 6 = 262144
```
