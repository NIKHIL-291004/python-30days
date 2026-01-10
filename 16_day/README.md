# 🐍 Python Functions – Complete & Detailed Notes

---

## 📌 1. What is a Function?

A **function** is a reusable block of code designed to perform a specific task.
Instead of writing the same code repeatedly, we define it once and **reuse it**.

### ✅ Why Functions?

* Code reusability
* Better readability
* Easy debugging
* Modular programming

---

## 📌 2. Defining & Calling a Function

### Syntax

```python
def function_name():
    statements

function_name()   # calling the function
```

### Example

```python
def greet():
    print("Welcome to Python")

greet()
```

**Output**

```
Welcome to Python
```

---

## 📌 3. Function Without Parameters

```python
def add_numbers():
    a = 2
    b = 3
    print(a + b)

add_numbers()
```

**Output**

```
5
```

---

## 📌 4. Function Returning a Value

If a function does **not return**, it returns `None` by default.

```python
def add():
    return 10 + 20

print(add())
```

**Output**

```
30
```

---

## 📌 5. Function With Parameters

### Single Parameter

```python
def square(n):
    return n * n

print(square(5))
```

**Output**

```
25
```

---

### Two Parameters

```python
def add(a, b):
    return a + b

print(add(4, 6))
```

**Output**

```
10
```

---

## 📌 6. Keyword Arguments

Order does not matter.

```python
def full_name(first, last):
    return first + " " + last

print(full_name(last="Reddy", first="Nikhil"))
```

**Output**

```
Nikhil Reddy
```

---

## 📌 7. Default Parameters

```python
def greet(name="Guest"):
    return "Hello " + name

print(greet())
print(greet("Nikhil"))
```

**Output**

```
Hello Guest
Hello Nikhil
```

---

## 📌 8. Arbitrary Arguments (*args)

Used when number of arguments is unknown.

```python
def total(*nums):
    return sum(nums)

print(total(1, 2, 3, 4))
```

**Output**

```
10
```

---

## 📌 9. Arbitrary Keyword Arguments (**kwargs)

```python
def details(**data):
    for k, v in data.items():
        print(k, ":", v)

details(Name="Nikhil", Age=21, Role="Student")
```

**Output**

```
Name : Nikhil
Age : 21
Role : Student
```

---

## 📌 10. Function Inside a Function (Nested Function)

```python
def outer():
    msg = "Hello"
    def inner():
        print(msg)
    inner()

outer()
```

**Output**

```
Hello
```

---

## 📌 11. Lambda (Anonymous Functions)

### Syntax

```python
lambda arguments : expression
```

### Example

```python
square = lambda x: x * x
print(square(6))
```

**Output**

```
36
```

---

## 📌 12. Higher Order Functions (HOF)

A function that:

* Takes another function as argument OR
* Returns a function

### Function as Parameter

```python
def square(x):
    return x * x

def operate(f, n):
    return f(n)

print(operate(square, 5))
```

**Output**

```
25
```

---

## 📌 13. Closures

A function remembering its outer variable.

```python
def add_ten():
    ten = 10
    def add(x):
        return x + ten
    return add

closure = add_ten()
print(closure(5))
```

**Output**

```
15
```

---

## 📌 14. Decorators

Used to **modify a function without changing its code**.

```python
def uppercase(func):
    def wrapper():
        return func().upper()
    return wrapper

@uppercase
def greet():
    return "welcome to python"

print(greet())
```

**Output**

```
WELCOME TO PYTHON
```

---

## 📌 15. map(), filter(), reduce()

### map()

```python
nums = [1, 2, 3]
result = map(lambda x: x * 2, nums)
print(list(result))
```

**Output**

```
[2, 4, 6]
```

---

### filter()

```python
nums = [1, 2, 3, 4]
even = filter(lambda x: x % 2 == 0, nums)
print(list(even))
```

**Output**

```
[2, 4]
```

---

### reduce()

```python
from functools import reduce

nums = [1, 2, 3, 4]
result = reduce(lambda x, y: x * y, nums)
print(result)
```

**Output**

```
24
```

---

## 📌 16. Difference: lambda vs def

| Feature   | lambda   | def       |
| --------- | -------- | --------- |
| Lines     | Single   | Multiple  |
| Name      | Optional | Mandatory |
| Logic     | Simple   | Complex   |
| Docstring | ❌        | ✅         |


# Exercise:
### Exercises: Level 1

1. Declare a function _add_two_numbers_. It takes two parameters and it returns a sum.
2. Area of a circle is calculated as follows: area = π x r x r. Write a function that calculates _area_of_circle_.
3. Write a function called add_all_nums which takes arbitrary number of arguments and sums all the arguments. Check if all the list items are number types. If not do give a reasonable feedback.
4. Temperature in °C can be converted to °F using this formula: °F = (°C x 9/5) + 32. Write a function which converts °C to °F, _convert_celsius_to-fahrenheit_.
5. Write a function called check-season, it takes a month parameter and returns the season: Autumn, Winter, Spring or Summer.
6. Write a function called calculate_slope which return the slope of a linear equation
7. Quadratic equation is calculated as follows: ax² + bx + c = 0. Write a function which calculates solution set of a quadratic equation, _solve_quadratic_eqn_.
8. Declare a function named print_list. It takes a list as a parameter and it prints out each element of the list.
9. Declare a function named reverse_list. It takes an array as a parameter and it returns the reverse of the array (use loops).

```py
print(reverse_list([1, 2, 3, 4, 5]))
# [5, 4, 3, 2, 1]
print(reverse_list1(["A", "B", "C"]))
# ["C", "B", "A"]
```

10. Declare a function named capitalize_list_items. It takes a list as a parameter and it returns a capitalized list of items
11. Declare a function named add_item. It takes a list and an item parameters. It returns a list with the item added at the end.

```py
food_staff = ['Potato', 'Tomato', 'Mango', 'Milk']
print(add_item(food_staff, 'Meat'))     # ['Potato', 'Tomato', 'Mango', 'Milk','Meat']
numbers = [2, 3, 7, 9]
print(add_item(numbers, 5))      [2, 3, 7, 9, 5]
```

12. Declare a function named remove_item. It takes a list and an item parameters. It returns a list with the item removed from it.

```py
food_staff = ['Potato', 'Tomato', 'Mango', 'Milk']
print(remove_item(food_staff, 'Mango'))  # ['Potato', 'Tomato', 'Milk'];
numbers = [2, 3, 7, 9]
print(remove_item(numbers, 3))  # [2, 7, 9]
```

13. Declare a function named sum_of_numbers. It takes a number parameter and it adds all the numbers in that range.

```py
print(sum_of_numbers(5))  # 15
print(sum_of_numbers(10)) # 55
print(sum_of_numbers(100)) # 5050
```

14. Declare a function named sum_of_odds. It takes a number parameter and it adds all the odd numbers in that range.
15. Declare a function named sum_of_even. It takes a number parameter and it adds all the even numbers in that - range.

### Exercises: Level 2

1. Declare a function named evens_and_odds . It takes a positive integer as parameter and it counts number of evens and odds in the number.

```py
    print(evens_and_odds(100))
    # The number of odds are 50.
    # The number of evens are 51.
```

1. Call your function factorial, it takes a whole number as a parameter and it return a factorial of the number
1. Call your function _is_empty_, it takes a parameter and it checks if it is empty or not
1. Write different functions which take lists. They should calculate_mean, calculate_median, calculate_mode, calculate_range, calculate_variance, calculate_std (standard deviation).

### Exercises: Level 3

1. Write a function called is_prime, which checks if a number is prime.
1. Write a functions which checks if all items are unique in the list.
1. Write a function which checks if all the items of the list are of the same data type.
1. Write a function which check if provided variable is a valid python variable
1. Go to the data folder and access the countries-data.py file.

- Create a function called the most_spoken_languages in the world. It should return 10 or 20 most spoken languages in the world in descending order
- Create a function called the most_populated_countries. It should return 10 or 20 most populated countries in descending order.

# Exercise: for higher functions
```py
countries = ['Estonia', 'Finland', 'Sweden', 'Denmark', 'Norway', 'Iceland']
names = ['Asabeneh', 'Lidiya', 'Ermias', 'Abraham']
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
```

### Exercises: Level 1

1. Explain the difference between map, filter, and reduce.
2. Explain the difference between higher order function, closure and decorator
3. Define a call function before map, filter or reduce, see examples.
4. Use for loop to print each country in the countries list.
5. Use for to print each name in the names list.
6. Use for to print each number in the numbers list.

### Exercises: Level 2

1. Use map to create a new list by changing each country to uppercase in the countries list
1. Use map to create a new list by changing each number to its square in the numbers list
1. Use map to change each name to uppercase in the names list
1. Use filter to filter out countries containing 'land'.
1. Use filter to filter out countries having exactly six characters.
1. Use filter to filter out countries containing six letters and more in the country list.
1. Use filter to filter out countries starting with an 'E'
1. Chain two or more list iterators (eg. arr.map(callback).filter(callback).reduce(callback))
1. Declare a function called get_string_lists which takes a list as a parameter and then returns a list containing only string items.
1. Use reduce to sum all the numbers in the numbers list.
1. Use reduce to concatenate all the countries and to produce this sentence: Estonia, Finland, Sweden, Denmark, Norway, and Iceland are north European countries
1. Declare a function called categorize_countries that returns a list of countries with some common pattern (you can find the [countries list](https://github.com/Asabeneh/30-Days-Of-Python/blob/master/data/countries.py) in this repository as countries.js(eg 'land', 'ia', 'island', 'stan')).
1. Create a function returning a dictionary, where keys stand for starting letters of countries and values are the number of country names starting with that letter.
2. Declare a get_first_ten_countries function - it returns a list of first ten countries from the countries.js list in the data folder.
1. Declare a get_last_ten_countries function that returns the last ten countries in the countries list.

### Exercises: Level 3

1. Use the countries_data.py (https://github.com/Asabeneh/30-Days-Of-Python/blob/master/data/countries-data.py) file and follow the tasks below:
   - Sort countries by name, by capital, by population
   - Sort out the ten most spoken languages by location.
   - Sort out the ten most populated countries.
