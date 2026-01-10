# 🧠 Python List Comprehension – Ultra Detailed Notes with Outputs

---

## 📘 1. Introduction to List Comprehension

**List comprehension** is a concise and elegant way to create lists in Python using a single line of code.

It allows:

* Iteration
* Transformation
* Filtering

all in **one readable expression**.

📌 Compared to traditional `for` loops, list comprehensions are:

* Shorter
* Cleaner
* Often faster

---

## 🔑 2. Basic Syntax

```python
[expression for item in iterable if condition]
```

### Syntax Breakdown

| Component    | Meaning                                     |
| ------------ | ------------------------------------------- |
| expression   | Operation to apply on each item             |
| item         | Variable representing each element          |
| iterable     | Sequence (list, tuple, string, range, etc.) |
| if condition | Optional filter                             |

---

## 🧪 3. Simple Example – String to List

### Method 1: Using `list()`

```python
language = 'Python'
lst = list(language)
print(type(lst))
print(lst)
```

**Output**

```text
<class 'list'>
['P', 'y', 't', 'h', 'o', 'n']
```

---

### Method 2: Using List Comprehension

```python
language = 'Python'
lst = [i for i in language]
print(type(lst))
print(lst)
```

**Output**

```text
<class 'list'>
['P', 'y', 't', 'h', 'o', 'n']
```

✔ Both outputs are same
✔ List comprehension is **shorter and preferred**

---

## 🔢 4. Generating Numbers Using List Comprehension

```python
numbers = [i for i in range(11)]
print(numbers)
```

**Output**

```text
[0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

---

## ➗ 5. Performing Mathematical Operations

### Squaring Numbers

```python
squares = [i * i for i in range(11)]
print(squares)
```

**Output**

```text
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

---

### Creating List of Tuples

```python
pairs = [(i, i * i) for i in range(6)]
print(pairs)
```

**Output**

```text
[(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25)]
```

---

## 🔍 6. List Comprehension with Conditions

### Generating Even Numbers

```python
even_numbers = [i for i in range(21) if i % 2 == 0]
print(even_numbers)
```

**Output**

```text
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
```

---

### Generating Odd Numbers

```python
odd_numbers = [i for i in range(21) if i % 2 != 0]
print(odd_numbers)
```

**Output**

```text
[1, 3, 5, 7, 9, 11, 13, 15, 17, 19]
```

---

## 🧹 7. Filtering Data from a List

```python
numbers = [-8, -7, -3, -1, 0, 1, 3, 4, 5, 7, 6, 8, 10]
positive_even_numbers = [i for i in numbers if i % 2 == 0 and i > 0]
print(positive_even_numbers)
```

**Output**

```text
[4, 6, 8, 10]
```

✔ Filters:

* even numbers
* positive values

---

## 🔁 8. Flattening a Nested List (Very Important)

```python
list_of_lists = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
flattened_list = [number for row in list_of_lists for number in row]
print(flattened_list)
```

**Output**

```text
[1, 2, 3, 4, 5, 6, 7, 8, 9]
```

📌 Execution Order:

1. Loop through each `row`
2. Loop through each `number` in row

---

## 🔄 9. For Loop vs List Comprehension

### Using For Loop

```python
a = [1, 2, 3, 4, 5]
res = []
for val in a:
    res.append(val * 2)
print(res)
```

**Output**

```text
[2, 4, 6, 8, 10]
```

---

### Using List Comprehension

```python
a = [1, 2, 3, 4, 5]
res = [val * 2 for val in a]
print(res)
```

**Output**

```text
[2, 4, 6, 8, 10]
```

✔ Same output
✔ Less code
✔ More readable

---

## 🧠 10. Nested List Comprehension

```python
coordinates = [(x, y) for x in range(3) for y in range(3)]
print(coordinates)
```

**Output**

```text
[(0, 0), (0, 1), (0, 2),
 (1, 0), (1, 1), (1, 2),
 (2, 0), (2, 1), (2, 2)]
```

---

## 🧪 11. Conditional Transformation (If-Else)

```python
nums = [1, 2, 3, 4, 5]
res = ['Even' if i % 2 == 0 else 'Odd' for i in nums]
print(res)
```

**Output**

```text
['Odd', 'Even', 'Odd', 'Even', 'Odd']
```

## 💻 Exercises:

1. Filter only negative and zero in the list using list comprehension
   ```py
   numbers = [-4, -3, -2, -1, 0, 2, 4, 6]
   ```
2. Flatten the following list of lists of lists to a one dimensional list :

   ```py
   list_of_lists =[[[1, 2, 3]], [[4, 5, 6]], [[7, 8, 9]]]

   output
   [1, 2, 3, 4, 5, 6, 7, 8, 9]
   ```

3. Using list comprehension create the following list of tuples:
   ```py
   [(0, 1, 0, 0, 0, 0, 0),
   (1, 1, 1, 1, 1, 1, 1),
   (2, 1, 2, 4, 8, 16, 32),
   (3, 1, 3, 9, 27, 81, 243),
   (4, 1, 4, 16, 64, 256, 1024),
   (5, 1, 5, 25, 125, 625, 3125),
   (6, 1, 6, 36, 216, 1296, 7776),
   (7, 1, 7, 49, 343, 2401, 16807),
   (8, 1, 8, 64, 512, 4096, 32768),
   (9, 1, 9, 81, 729, 6561, 59049),
   (10, 1, 10, 100, 1000, 10000, 100000)]
   ```
4. Flatten the following list to a new list:
   ```py
   countries = [[('Finland', 'Helsinki')], [('Sweden', 'Stockholm')], [('Norway', 'Oslo')]]
   output:
   [['FINLAND','FIN', 'HELSINKI'], ['SWEDEN', 'SWE', 'STOCKHOLM'], ['NORWAY', 'NOR', 'OSLO']]
   ```
5. Change the following list to a list of dictionaries:
   ```py
   countries = [[('Finland', 'Helsinki')], [('Sweden', 'Stockholm')], [('Norway', 'Oslo')]]
   output:
   [{'country': 'FINLAND', 'city': 'HELSINKI'},
   {'country': 'SWEDEN', 'city': 'STOCKHOLM'},
   {'country': 'NORWAY', 'city': 'OSLO'}]
   ```
6. Change the following list of lists to a list of concatenated strings:
   ```py
   names = [[('Asabeneh', 'Yetayeh')], [('David', 'Smith')], [('Donald', 'Trump')], [('Bill', 'Gates')]]
   output
   ['Asabeneh Yetaeyeh', 'David Smith', 'Donald Trump', 'Bill Gates']
