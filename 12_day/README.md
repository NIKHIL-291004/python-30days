
# 🐍 Python Tuples 

---

## 📌 What is a Tuple?

A **tuple** is a built-in Python data structure used to store an **ordered collection of elements** that **cannot be modified** after creation.

➡️ Tuples are **immutable**, meaning:
- You **cannot add**
- You **cannot remove**
- You **cannot update** elements

Once created, a tuple’s structure and values remain fixed.

---

## 📌 Key Characteristics of Tuples

| Property | Description |
|--------|-------------|
| Ordered | Elements maintain insertion order |
| Immutable | Cannot be changed after creation |
| Indexed | Supports positive & negative indexing |
| Heterogeneous | Can store mixed data types |
| Duplicates | Allows duplicate values |
| Hashable | Can be dictionary keys (if elements are immutable) |
| Faster | Faster than lists due to immutability |

---

## 📌 Tuple vs List (Very Important)

| Feature | List | Tuple |
|------|------|------|
| Mutable | ✅ Yes | ❌ No |
| Syntax | `[ ]` | `( )` |
| Speed | Slower | Faster |
| Memory | More | Less |
| Methods | Many | Very few |
| Safety | Less safe | More safe |
| Use Case | Dynamic data | Fixed data |

---

## 📌 Creating Tuples

### 1️⃣ Empty Tuple
```python
tup = ()
tup = tuple()
````

---

### 2️⃣ Tuple with Elements

```python
tup = ('apple', 'banana', 'cherry')
```

---

### 3️⃣ Single Element Tuple (IMPORTANT)

```python
tup = ('apple',)   # comma is mandatory
```

❌ Incorrect:

```python
tup = ('apple')    # This is a string, NOT a tuple
```

---

### 4️⃣ Tuple from List

```python
lst = [1, 2, 3]
tup = tuple(lst)
```

---

### 5️⃣ Tuple from String

```python
tup = tuple("Python")
```

---

### 6️⃣ Tuple with Mixed Data Types

```python
tup = (10, 3.14, "Python", True)
```

---

### 7️⃣ Nested Tuples

```python
tup1 = (1, 2, 3)
tup2 = ('a', 'b')
nested = (tup1, tup2)
```

---

### 8️⃣ Tuple with Repetition

```python
tup = ('Hi',) * 5
```

---

## 📌 Length of Tuple

```python
len(tup)
```

---

## 📌 Accessing Tuple Elements

### 🔹 Positive Indexing

```python
tup = ('a', 'b', 'c', 'd')
tup[0]
tup[2]
```

---

### 🔹 Negative Indexing

```python
tup[-1]   # last element
tup[-2]   # second last
```

---

## 📌 Tuple Slicing

### Syntax

```python
tuple[start : stop : step]
```

---

### Positive Slicing

```python
tup[1:4]
tup[:3]
tup[2:]
```

---

### Negative Slicing

```python
tup[-4:-1]
tup[::-1]   # reverse tuple
```

---

## 📌 Tuple Unpacking

### Basic Unpacking

```python
tup = ('Python', 'Java', 'C')
a, b, c = tup
```

---

### Unpacking with Asterisk (*)

```python
tup = (1, 2, 3, 4, 5)
a, *b, c = tup
```

✔ `a` → first element
✔ `c` → last element
✔ `b` → remaining elements (list)

---

## 📌 Checking Membership

```python
'banana' in ('apple', 'banana', 'cherry')
```

Returns `True` or `False`

---

## 📌 Tuple Methods (VERY FEW)

Tuples support **only two methods**:

### 1️⃣ count()

```python
tup = (1, 2, 2, 3)
tup.count(2)
```

---

### 2️⃣ index()

```python
tup.index(3)
```

---

## 📌 Why Tuples Have Fewer Methods?

Because tuples are **immutable**, operations that modify data are not allowed.
This makes tuples:

✔ Safer
✔ Faster
✔ Memory-efficient

---

## 📌 Modifying Tuples (Indirect Way)

Tuples cannot be modified directly.
To modify:

### Step 1: Convert to list

### Step 2: Modify

### Step 3: Convert back to tuple

```python
tup = ('apple', 'banana')
lst = list(tup)
lst[0] = 'orange'
tup = tuple(lst)
```

---

## 📌 Concatenating Tuples

```python
tup1 = (1, 2)
tup2 = (3, 4)
tup3 = tup1 + tup2
```

⚠️ Only tuples can be concatenated with tuples.

---

## 📌 Deleting Tuples

❌ Cannot delete individual elements
✅ Can delete entire tuple

```python
tup = (1, 2, 3)
del tup
```

Accessing it after deletion causes **NameError**.

---

## 📌 Tuples as Dictionary Keys

Tuples can be dictionary keys **if they contain only immutable elements**.

```python
data = {
    (1, 2): "value",
    (3, 4): "another"
}
```

---

## 📌 Performance: Tuple vs List

* Tuples use **less memory**
* Tuples are **faster in iteration**
* Python optimizes tuples internally

➡️ Use tuples when data **should not change**

---

## 📌 Real-World Use Cases of Tuples

✔ Coordinates (x, y)
✔ Database records
✔ Function return values
✔ Dictionary keys
✔ Fixed configuration values

---

## 📌 Common Errors with Tuples

❌ Trying to modify element

```python
tup[0] = 10   # TypeError
```

❌ Forgetting comma in single-element tuple

```python
('apple')   # Not a tuple
```

---

### Exercises: Level 1

1. Create an empty tuple
2. Create a tuple containing names of your sisters and your brothers (imaginary siblings are fine)
3. Join brothers and sisters tuples and assign it to siblings
4. How many siblings do you have?
5. Modify the siblings tuple and add the name of your father and mother and assign it to family_members

### Exercises: Level 2

1. Unpack siblings and parents from family_members
1. Create fruits, vegetables and animal products tuples. Join the three tuples and assign it to a variable called food_stuff_tp.
1. Change the about food_stuff_tp  tuple to a food_stuff_lt list
1. Slice out the middle item or items from the food_stuff_tp tuple or food_stuff_lt list.
1. Slice out the first three items and the last three items from food_staff_lt list
1. Delete the food_staff_tp tuple completely
1. Check if an item exists in  tuple:

- Check if 'Estonia' is a nordic country
- Check if 'Iceland' is a nordic country

  ```py
  nordic_countries = ('Denmark', 'Finland','Iceland', 'Norway', 'Sweden')
  ```

### Exercises: Level 3

## 1️⃣ Tuple 1 – Double the Values

### 📌 Problem Statement
You are given a tuple `tup` that contains integers.  
You need to **return a tuple containing doubles of the given numbers**.

### 🧪 Examples

**Input:**  
`tup = (4, 5, 1, 2, 3, 5)`

**Output:**  
`8 10 2 4 6 10`

**Explanation:**  
Each element of the tuple is multiplied by 2.

---

**Input:**  
`tup = (3, 1, 4, 7, 2, 6, 4)`

**Output:**  
`6 2 8 14 4 12 8`

**Explanation:**  
Each element of the tuple is multiplied by 2.

---

## 2️⃣ Extend AP (Arithmetic Progression)

### 📌 Problem Statement
You are given an array `arr[]` whose elements form an **Arithmetic Progression (A.P.)**.  
Your task is to **determine the next three numbers in the progression** and return a new array containing the **original sequence along with these three additional terms**.

### 🧪 Examples

**Input:**  
`arr = (1, 5, 9, 13, 17)`

**Output:**  
`1 5 9 13 17 21 25 29`

**Explanation:**  
The common difference is `4`.  
The next three terms are `21`, `25`, and `29`.

---

**Input:**  
`arr = (3, 1, -1, -3, -5, -7)`

**Output:**  
`3 1 -1 -3 -5 -7 -9 -11 -13`

**Explanation:**  
The common difference is `-2`.  
The next three terms are `-9`, `-11`, and `-13`.

---
