
# 🐍 Python Lists 

## 📌 Introduction to Python Lists

In Python, **lists** are one of the most commonly used **collection data types**. They allow us to store multiple values in a single variable.

Python provides **four main collection data types**:

| Data Type | Ordered | Mutable | Indexed | Duplicates |
|---------|--------|---------|---------|------------|
| List | ✅ Yes | ✅ Yes | ✅ Yes | ✅ Yes |
| Tuple | ✅ Yes | ❌ No | ✅ Yes | ✅ Yes |
| Set | ❌ No | ❌ No* | ❌ No | ❌ No |
| Dictionary | ❌ No | ✅ Yes | ✅ Yes (keys) | ❌ No (keys) |

> *Sets are unmodifiable, but new elements can be added.*

---

## 📌 What is a List?

A **list** is:
- An **ordered** collection of items
- **Mutable** (can be changed after creation)
- **Index-based** (index starts from `0`)
- Allows **duplicate values**
- Can store **multiple data types** (int, float, string, boolean, list, dictionary, etc.)

### Example
```python
lst = ['Asabeneh', 250, True, {'country':'Finland', 'city':'Helsinki'}]
````

---

## 📌 Creating Lists in Python

### 1️⃣ Using Square Brackets `[]`

```python
a = [1, 2, 3, 4, 5]
b = ['apple', 'banana', 'cherry']
c = [1, 'hello', 3.14, True]

print(a)
print(b)
print(c)
```

### 2️⃣ Using `list()` Constructor

```python
a = list((1, 2, 3, 'apple', 4.5))
b = list("GFG")

print(a)
print(b)
```

### 3️⃣ Creating Empty Lists

```python
lst = []
empty_list = list()

print(len(lst))  # 0
```

### 4️⃣ Creating Lists with Repeated Elements

```python
a = [2] * 5
b = [0] * 7

print(a)
print(b)
```

---

## 📌 Lists with Initial Values

```python
fruits = ['banana', 'orange', 'mango', 'lemon']
vegetables = ['Tomato', 'Potato', 'Cabbage','Onion', 'Carrot']
countries = ['Finland', 'Estonia', 'Denmark', 'Sweden', 'Norway']

print('Fruits:', fruits)
print('Number of fruits:', len(fruits))
```

---

## 📌 Accessing List Elements

### 🔹 Positive Indexing

```python
fruits = ['banana', 'orange', 'mango', 'lemon']
print(fruits[0])  # banana
print(fruits[1])  # orange
```

### 🔹 Negative Indexing

```python
print(fruits[-1])  # lemon
print(fruits[-2])  # mango
```

---

## 📌 List Slicing

### Positive Slicing

```python
fruits = ['banana', 'orange', 'mango', 'lemon']
print(fruits[1:3])   # ['orange', 'mango']
print(fruits[::2])   # ['banana', 'mango']
```

### Negative Slicing

```python
print(fruits[::-1])  # Reverse list
```

---

## 📌 Unpacking List Items

```python
lst = ['item1','item2','item3', 'item4', 'item5']
first, second, third, *rest = lst

print(first)
print(rest)
```

---

## 📌 Modifying Lists (Mutable Nature)

```python
fruits = ['banana', 'orange', 'mango', 'lemon']
fruits[0] = 'avocado'
fruits[-1] = 'lime'
print(fruits)
```

---

## 📌 Checking Membership in a List

```python
print('banana' in fruits)  # True
print('apple' in fruits)   # False
```

---

## 📌 Adding Elements to a List

### append()

```python
fruits.append('apple')
```

### insert()

```python
fruits.insert(2, 'grapes')
```

### extend()

```python
fruits.extend(['kiwi', 'papaya'])
```

---

## 📌 Removing Elements from a List

### remove()

```python
fruits.remove('banana')
```

### pop()

```python
fruits.pop()
fruits.pop(0)
```

### del

```python
del fruits[1]
del fruits[1:3]
```

### clear()

```python
fruits.clear()
```

---

## 📌 Copying a List

```python
fruits_copy = fruits.copy()
```

> Avoid `list2 = list1` as it creates a reference, not a copy.

---

## 📌 Joining Lists

### Using `+`

```python
list3 = list1 + list2
```

### Using `extend()`

```python
list1.extend(list2)
```

---

## 📌 Counting Elements

```python
ages = [22, 24, 24, 25, 24]
print(ages.count(24))  # 3
```

---

## 📌 Finding Index of an Element

```python
print(ages.index(24))  # First occurrence
```

---

## 📌 Reversing a List

```python
ages.reverse()
```

---

## 📌 Sorting Lists

### sort() – modifies original list

```python
ages.sort()
ages.sort(reverse=True)
```

### sorted() – returns new list

```python
new_list = sorted(ages)
```

---

## 📌 Iterating Over a List

```python
for item in ['apple', 'banana', 'cherry']:
    print(item)
```

---

## 📌 Nested Lists (2D Lists)

```python
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

print(matrix[1][2])  # 6
```

---

## 📌 List Comprehension

```python
squares = [x**2 for x in range(1, 6)]
print(squares)
```

---

## 📌 How Python Stores List Elements?

* Lists store **references to objects**, not actual values
* Mutable objects inside lists can change original data
* Immutable objects remain unaffected

```python
a = [10, 20, "GfG", True]
print(a)
```

---

### Exercises: Level 1

1. Declare an empty list
2. Declare a list with more than 5 items
3. Find the length of your list
4. Get the first item, the middle item and the last item of the list
5. Declare a list called mixed_data_types, put your(name, age, height, marital status, address)
6. Declare a list variable named it_companies and assign initial values Facebook, Google, Microsoft, Apple, IBM, Oracle and Amazon.
7. Print the list using _print()_
8. Print the number of companies in the list
9. Print the first, middle and last company
10. Print the list after modifying one of the companies
11. Add an IT company to it_companies
12. Insert an IT company in the middle of the companies list
13. Change one of the it_companies names to uppercase (IBM excluded!)
14. Join the it_companies with a string '#;&nbsp; '
15. Check if a certain company exists in the it_companies list.
16. Sort the list using sort() method
17. Reverse the list in descending order using reverse() method
18. Slice out the first 3 companies from the list
19. Slice out the last 3 companies from the list
20. Slice out the middle IT company or companies from the list
21. Remove the first IT company from the list
22. Remove the middle IT company or companies from the list
23. Remove the last IT company from the list
24. Remove all IT companies from the list
25. Destroy the IT companies list
26. Join the following lists:

    ```py
    front_end = ['HTML', 'CSS', 'JS', 'React', 'Redux']
    back_end = ['Node','Express', 'MongoDB']
    ```

27. After joining the lists in question 26. Copy the joined list and assign it to a variable full_stack, then insert Python and SQL after Redux.

### Exercises: Level 2

1. The following is a list of 10 students ages:

```sh
ages = [19, 22, 19, 24, 20, 25, 26, 24, 25, 24]
```

- Sort the list and find the min and max age
- Add the min age and the max age again to the list
- Find the median age (one middle item or two middle items divided by two)
- Find the average age (sum of all items divided by their number )
- Find the range of the ages (max minus min)
- Compare the value of (min - average) and (max - average), use _abs()_ method

1. Find the middle country(ies) in the [countries list](https://github.com/Asabeneh/30-Days-Of-Python/tree/master/data/countries.py)
1. Divide the countries list into two equal lists if it is even if not one more country for the first half.
1. ['China', 'Russia', 'USA', 'Finland', 'Sweden', 'Norway', 'Denmark']. Unpack the first three countries and the rest as scandic countries.

 ### Exercises: Level 3

## 1️⃣ Length of the List

### 📌 Problem Statement
You are given a list that contains integers.  
You need to **return the length of the list**.

### 🧪 Examples

**Input:**  
`arr = [54, 43, 2, 1, 5]`  

**Output:**  
`5`  

**Explanation:**  
The list contains 5 elements, so its length is 5.

---

**Input:**  
`arr = [324, 5, 2, 2]`  

**Output:**  
`4`  

**Explanation:**  
The list contains 4 elements, so its length is 4.

---

## 2️⃣ List Traversal

### 📌 Problem Statement
You are given a list that contains integers.  
You need to **print the elements of the list with a space between them**.

> **Note:** Do not add a new line at the end.

### 🧪 Examples

**Input:**  
`arr = [54, 43, 2, 1, 5]`  

**Output:**  
`54 43 2 1 5`  

**Explanation:**  
Traverse the list and print each element separated by a space.

---

**Input:**  
`arr = [324, 5, 2, 2]`  

**Output:**  
`324 5 2 2`  

**Explanation:**  
Traverse the list and print each element separated by a space.

---

## 3️⃣ Decrement List Values

### 📌 Problem Statement
You are given a list that contains integers.  
You need to **decrement each element of the list by 1** and return the updated list.

### 🧪 Examples

**Input:**  
`arr = [54, 43, 2, 1, 5]`  

**Output:**  
`53 42 1 0 4`  

**Explanation:**  
Each element is decremented by 1.

---

**Input:**  
`arr = [324, 5, 2, 2]`  

**Output:**  
`323 4 1 1`  

**Explanation:**  
Each element is decremented by 1.

---

### ✅ End of Problems

 
