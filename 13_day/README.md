# 🧮 Python Sets – Complete & Detailed Guide

## 📘 Introduction

A **set** in Python is a built-in data structure used to store a collection of **unique elements**.
It follows the mathematical definition of a set and is optimized for **fast membership testing** and **set operations**.

---

## 🔑 Key Characteristics of Sets

* Unordered collection
* Unindexed (no position-based access)
* Mutable (can add/remove elements)
* No duplicate values allowed
* Can store multiple data types
* Implemented using hash tables
* Fast lookup time (O(1) average)

⚠️ Sets **cannot store mutable objects** like lists or dictionaries.

---

## 🏗️ Creating Sets

### Empty Set

```python
st = set()
```

### Set with Elements

```python
fruits = {'banana', 'orange', 'mango', 'lemon'}
```

### Using `set()` Constructor

```python
set1 = set("Python")
set2 = set([1, 2, 3, 3, 4])
set3 = set((10, 20, 30))
set4 = set({"a": 1, "b": 2})  # keys only
```

---

## 📏 Length of a Set

```python
len(fruits)
```

---

## 🔁 Accessing Set Elements

Sets are unindexed, so use loops:

```python
for item in fruits:
    print(item)
```

---

## 🔎 Membership Testing

```python
'mango' in fruits
```

---

## ➕ Adding Elements

### Add One Element

```python
fruits.add('apple')
```

### Add Multiple Elements

```python
fruits.update(['grapes', 'papaya'])
```

---

## ❌ Removing Elements

### remove()

Raises error if element not found

```python
fruits.remove('banana')
```

### discard()

No error if element not found

```python
fruits.discard('banana')
```

### pop()

Removes a random element

```python
fruits.pop()
```

---

## 🧹 Clearing & Deleting Sets

### clear()

```python
fruits.clear()
```

### del

```python
del fruits
```

---

## 🔄 Type Conversion

### List to Set

```python
lst = [1, 2, 2, 3, 4]
st = set(lst)
```

### Set to List

```python
lst = list(st)
```

---

## 🔗 Set Operations

### Union

```python
A.union(B)
```

### Intersection

```python
A.intersection(B)
```

### Difference

```python
A.difference(B)
```

### Symmetric Difference

```python
A.symmetric_difference(B)
```

---

## 📦 Subset & Superset

### Subset

```python
B.issubset(A)
```

### Superset

```python
A.issuperset(B)
```

---

## 🚫 Disjoint Sets

```python
A.isdisjoint(B)
```

---

## ❄️ Frozen Sets

A **frozenset** is an immutable set.

```python
fs = frozenset([1, 2, 3, 4])
```

---

## 🧪 Comparison Table

| Feature     | List | Tuple | Set |
| ----------- | ---- | ----- | --- |
| Ordered     | ✅    | ✅     | ❌   |
| Mutable     | ✅    | ❌     | ✅   |
| Duplicates  | ✅    | ✅     | ❌   |
| Indexed     | ✅    | ✅     | ❌   |
| Fast Lookup | ❌    | ❌     | ✅   |

---

## 🎯 Use Cases

* Removing duplicate values
* Fast membership checking
* Mathematical set operations
* Data filtering and comparison


# Exercises
### Exercises: Level 1

1. Find the length of the set it_companies
2. Add 'Twitter' to it_companies
3. Insert multiple IT companies at once to the set it_companies
4. Remove one of the companies from the set it_companies
5. What is the difference between remove and discard

### Exercises: Level 2

1. Join A and B
1. Find A intersection B
1. Is A subset of B
1. Are A and B disjoint sets
1. Join A with B and B with A
1. What is the symmetric difference between A and B
1. Delete the sets completely

### Exercises: Level 3

1. Convert the ages to a set and compare the length of the list and the set, which one is bigger?
1. Explain the difference between the following data types: string, list, tuple and set
2. _I am a teacher and I love to inspire and teach people._ How many unique words have been used in the sentence? Use the split methods and set to get the unique words.




