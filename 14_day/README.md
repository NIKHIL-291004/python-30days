# 📘 Python Dictionaries – Complete & Extremely Detailed Guide

## 🔹 Introduction to Dictionaries

A **dictionary** in Python is a built-in data structure that stores data in **key : value** pairs.

📌 Dictionaries are widely used to represent **real-world data**, such as:

* Student records
* User profiles
* Configuration settings
* JSON-like data

### 🔑 Definition

> A dictionary is an **unordered (in older versions)**, **mutable**, and **indexed by keys** collection of **key-value pairs**.

📢 From **Python 3.7+**, dictionaries **preserve insertion order**.

---

## 🔍 Key Characteristics of Dictionaries

| Feature                | Description                         |
| ---------------------- | ----------------------------------- |
| Key–Value Pair         | Data stored as `key: value`         |
| Mutable                | Values can be modified              |
| Keys are Unique        | Duplicate keys overwrite old values |
| Keys are Immutable     | Strings, numbers, tuples allowed    |
| Values can be Any Type | int, str, list, tuple, set, dict    |
| Ordered (Python 3.7+)  | Maintains insertion order           |
| Fast Operations        | O(1) average time complexity        |

⚠️ **Important Rules**

* Keys are **case-sensitive**
* Lists, sets, dictionaries **cannot be keys**
* Duplicate keys are not allowed

---

## 🧠 Internal Working of Dictionaries

* Implemented using **hash tables**
* Each key is hashed to a memory location
* Enables:

  * Fast lookup
  * Fast insertion
  * Fast deletion

---

## 🏗️ Creating Dictionaries

### 1️⃣ Empty Dictionary

```python
empty_dict = {}
```

or

```python
empty_dict = dict()
```

---

### 2️⃣ Dictionary with Initial Data

```python
person = {
    'first_name': 'Asabeneh',
    'last_name': 'Yetayeh',
    'age': 250,
    'country': 'Finland',
    'is_married': True,
    'skills': ['JavaScript', 'React', 'Node', 'MongoDB', 'Python'],
    'address': {
        'street': 'Space street',
        'zipcode': '02210'
    }
}
```

✔️ Values can be **any data type**, including another dictionary.

---

### 3️⃣ Using `dict()` Constructor

```python
d = dict(name="Python", version=3.12, type="Programming Language")
```

---

## 📏 Length of a Dictionary

Returns number of key-value pairs.

```python
len(person)
```

---

## 🔑 Accessing Dictionary Items

### Access Using Keys

```python
person['first_name']
```

### Access Nested Data

```python
person['address']['street']
```

### Access List Inside Dictionary

```python
person['skills'][0]
```

---

## ⚠️ KeyError Problem

Accessing a non-existing key causes an error:

```python
person['city']  # ❌ KeyError
```

### Safe Access Using `get()`

```python
person.get('city')  # Returns None
```

You can also provide a default value:

```python
person.get('city', 'Not Found')
```

---

## ➕ Adding Items to a Dictionary

```python
person['job_title'] = 'Instructor'
```

Adding to existing list inside dictionary:

```python
person['skills'].append('HTML')
```

---

## ✏️ Modifying Dictionary Items

```python
person['first_name'] = 'Eyob'
person['age'] = 252
```

---

## 🔍 Checking Keys in Dictionary

```python
'age' in person       # True
'city' in person      # False
```

---

## ❌ Removing Items from Dictionary

### pop(key)

Removes item by key

```python
person.pop('first_name')
```

### popitem()

Removes **last inserted item**

```python
person.popitem()
```

### del

```python
del person['is_married']
```

---

## 🔄 Converting Dictionary to List

### items()

```python
person.items()
```

Returns:

```text
dict_items([('first_name', 'Asabeneh'), ('age', 250), ...])
```

---

## 🧹 Clearing a Dictionary

Removes all items but keeps dictionary object.

```python
person.clear()
```

---

## 🗑️ Deleting a Dictionary

```python
del person
```

---

## 📋 Copying a Dictionary

### Shallow Copy

```python
person_copy = person.copy()
```

Avoids modifying original dictionary.

---

## 🔑 Getting Keys

```python
keys = person.keys()
```

---

## 📦 Getting Values

```python
values = person.values()
```

---

## 🔁 Iterating Through Dictionary

### Iterate Over Keys

```python
for key in person:
    print(key)
```

### Iterate Over Values

```python
for value in person.values():
    print(value)
```

### Iterate Over Key–Value Pairs

```python
for key, value in person.items():
    print(key, value)
```

---

## 🪜 Nested Dictionaries

A dictionary inside another dictionary.

```python
data = {
    1: 'Python',
    2: 'Programming',
    3: {
        'A': 'Welcome',
        'B': 'To',
        'C': 'Python'
    }
}
```

Access:

```python
data[3]['A']
```

---

## 🧪 Comparison: Dictionary vs List vs Set

| Feature        | List | Set | Dictionary |
| -------------- | ---- | --- | ---------- |
| Ordered        | ✅    | ❌   | ✅ (3.7+)   |
| Mutable        | ✅    | ✅   | ✅          |
| Indexed        | ✅    | ❌   | By keys    |
| Key-Value Pair | ❌    | ❌   | ✅          |
| Duplicates     | ✅    | ❌   | Keys ❌     |

---

## 💻 Exercises: Day 8

1. Create  an empty dictionary called dog
2. Add name, color, breed, legs, age to the dog dictionary
3. Create a student dictionary and add first_name, last_name, gender, age, marital status, skills, country, city and address as keys for the dictionary
4. Get the length of the student dictionary
5. Get the value of skills and check the data type, it should be a list
6. Modify the skills values by adding one or two skills
7. Get the dictionary keys as a list
8. Get the dictionary values as a list
9. Change the dictionary to a list of tuples using _items()_ method
10. Delete one of the items in the dictionary
11. Delete one of the dictionaries
12. 
