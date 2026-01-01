
# 🐍 Python Programming - Complete Learning Guide

A comprehensive guide covering all core Python concepts from basics to advanced topics.

---

## 📋 Table of Contents

- [Introduction](#-introduction)
- [Getting Started](#-getting-started)
- [Basic Concepts](#-basic-concepts)
- [Data Types](#-data-types)
- [Operators](#-operators)
- [Control Flow](#-control-flow)
- [Loops](#-loops)
- [Functions](#-functions)
- [Data Structures](#-data-structures)
  - [Strings](#strings)
  - [Lists](#lists)

---

## 🎯 Introduction

Python is a versatile, beginner-friendly programming language used for:
- 🤖 Machine Learning & AI
- 📊 Data Science
- 🌐 Web Development
- 💻 Data Structures & Algorithms

### Why Python?
- ✅ Simple and readable syntax
- ✅ Extensive libraries and frameworks
- ✅ Large community support
- ✅ Cross-platform compatibility

---

## 🚀 Getting Started

### Hello World

```python
# Your first Python program
print("Hello, world!")
```

### Comments

```python
# Single-line comment

"""
Multi-line comment
or docstring
"""
```

### Running Python Code

```bash
# Run Python file
python script.py

# Interactive mode
python
>>> print("Hello")
```

---

## 📚 Basic Concepts

### 1. Variables

Variables store data for reuse throughout your program.

```python
# Variable assignment
message = "Hello, Python!"
count = 42
pi = 3.14

# Multiple assignment
x, y, z = 1, 2, 3

# Swapping variables
a, b = b, a
```

#### Naming Conventions

| Convention | Example | Usage |
|------------|---------|-------|
| **snake_case** | `my_variable` | ✅ Preferred in Python |
| **camelCase** | `myVariable` | Used in JavaScript |
| **PascalCase** | `MyVariable` | Used for class names |

#### Variable Rules
- ✅ Can contain letters, numbers, underscores
- ❌ Cannot start with a number
- ❌ Cannot use Python keywords (`if`, `for`, `while`, etc.)
- ❌ Cannot contain spaces

---

## 🔢 Data Types

### Primitive Types

```python
# Integer
age = 25

# Float
temperature = 98.6

# String
name = "Alice"

# Boolean
is_active = True

# None (null value)
result = None
```

### Type Checking

```python
# Check variable type
print(type(age))        # <class 'int'>
print(type(name))       # <class 'str'>
print(type(is_active))  # <class 'bool'>
```

### Type Conversion

```python
# Convert between types
num_str = "123"
num_int = int(num_str)      # String to integer
num_float = float(num_str)  # String to float

# Float to integer (rounds down)
pi = 3.14
pi_int = int(pi)  # 3

# Integer to string
age = 25
age_str = str(age)  # "25"
```

### Dynamic Typing

```python
# Variables can change types
variable = 10        # int
variable = "Hello"   # str
variable = [1, 2, 3] # list
```

> ⚠️ **Note**: While Python allows dynamic typing, it's best practice to maintain consistent types for readability.

---

## ➕ Operators

### Arithmetic Operators

```python
# Basic operations
x = 10
y = 3

addition = x + y        # 13
subtraction = x - y     # 7
multiplication = x * y  # 30
division = x / y        # 3.333... (always returns float)

# Advanced operations
floor_division = x // y # 3 (rounds down)
modulus = x % y        # 1 (remainder)
exponent = x ** y      # 1000 (10^3)
```

### Comparison Operators

```python
x = 5
y = 10

x == y  # False (equal to)
x != y  # True  (not equal to)
x < y   # True  (less than)
x > y   # False (greater than)
x <= y  # True  (less than or equal to)
x >= y  # False (greater than or equal to)
```

### Logical Operators

```python
# AND - both must be true
True and True   # True
True and False  # False

# OR - at least one must be true
True or False   # True
False or False  # False

# NOT - reverses boolean value
not True   # False
not False  # True

# Complex conditions
age = 25
if age >= 18 and age < 65:
    print("Working age")
```

### Assignment Operators

```python
# Shorthand operators
count = 0
count += 1  # count = count + 1
count -= 1  # count = count - 1
count *= 2  # count = count * 2
count /= 2  # count = count / 2
count //= 2 # count = count // 2
count %= 2  # count = count % 2
count **= 2 # count = count ** 2
```

---

## 🎮 Control Flow

### If Statements

```python
# Basic if statement
balance = 100

if balance > 0:
    print("Account is positive")
```

### If-Else Statements

```python
age = 20

if age >= 18:
    print("Adult")
else:
    print("Minor")
```

### If-Elif-Else Statements

```python
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print(f"Your grade: {grade}")
```

### Truthy and Falsy Values

```python
# Falsy values
if not 0:           # True
if not "":          # True
if not []:          # True
if not None:        # True
if not False:       # True

# Truthy values
if 42:              # True
if "text":          # True
if [1, 2, 3]:       # True
if True:            # True
```

---

## 🔁 Loops

### While Loops

```python
# Basic while loop
count = 0
while count < 5:
    print(count)
    count += 1

# Output: 0, 1, 2, 3, 4
```

### For Loops

```python
# Loop with range
for i in range(5):
    print(i)  # 0, 1, 2, 3, 4

# Loop with start and stop
for i in range(2, 6):
    print(i)  # 2, 3, 4, 5

# Loop with step
for i in range(0, 10, 2):
    print(i)  # 0, 2, 4, 6, 8

# Reverse loop
for i in range(10, 0, -1):
    print(i)  # 10, 9, 8, ..., 1

# Using reversed()
for i in reversed(range(1, 6)):
    print(i)  # 5, 4, 3, 2, 1
```

### Nested Loops

```python
# Print all pairs
for i in range(1, 4):
    for j in range(1, 4):
        print(f"({i}, {j})")

# Output: (1,1), (1,2), (1,3), (2,1), (2,2), ...
```

### Loop Control

```python
# break - exit loop
for i in range(10):
    if i == 5:
        break
    print(i)  # 0, 1, 2, 3, 4

# continue - skip iteration
for i in range(5):
    if i == 2:
        continue
    print(i)  # 0, 1, 3, 4

# pass - do nothing
for i in range(5):
    pass  # Placeholder
```

---

## 🔧 Functions

### Basic Functions

```python
# Function definition
def greet():
    print("Hello, World!")

# Function call
greet()
```

### Functions with Parameters

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")  # Hello, Alice!
```

### Functions with Return Values

```python
def add(x, y):
    return x + y

result = add(5, 3)  # 8
```

### Multiple Parameters

```python
def calculate_area(length, width):
    return length * width

area = calculate_area(5, 10)  # 50
```

### Default Arguments

```python
def greet(name="World"):
    print(f"Hello, {name}!")

greet()          # Hello, World!
greet("Alice")   # Hello, Alice!
```

### Type Hints

```python
def add(x: int, y: int) -> int:
    return x + y

def greet(name: str) -> None:
    print(f"Hello, {name}!")
```

### Variable Scope

```python
# Global scope
global_var = "I'm global"

def my_function():
    # Local scope
    local_var = "I'm local"
    print(global_var)  # Can access global
    print(local_var)   # Can access local

my_function()
# print(local_var)  # Error: local_var not defined
```

---

## 📦 Data Structures

### Strings

#### String Basics

```python
# Creating strings
text = "Hello, World!"
text2 = 'Python Programming'

# String length
length = len(text)  # 13

# String indexing (zero-based)
first_char = text[0]   # 'H'
last_char = text[-1]   # '!'

# String slicing
substring = text[0:5]   # "Hello"
substring = text[:5]    # "Hello"
substring = text[7:]    # "World!"
substring = text[::2]   # "Hlo ol!"
reversed_text = text[::-1]  # "!dlroW ,olleH"
```

#### String Methods

```python
text = "Hello, World!"

# Case conversion
text.upper()      # "HELLO, WORLD!"
text.lower()      # "hello, world!"
text.capitalize() # "Hello, world!"

# String checks
text.startswith("Hello")  # True
text.endswith("!")        # True
"123".isdigit()           # True
"abc".isalpha()           # True

# Find and replace
text.find("World")        # 7
text.replace("World", "Python")  # "Hello, Python!"

# Split and join
words = text.split(", ")  # ["Hello", "World!"]
" ".join(words)           # "Hello World!"

# Strip whitespace
"  hello  ".strip()       # "hello"
```

#### String Formatting

```python
name = "Alice"
age = 25

# f-strings (Python 3.6+) - Recommended
message = f"My name is {name} and I'm {age} years old"

# .format() method
message = "My name is {} and I'm {} years old".format(name, age)

# % operator (old style)
message = "My name is %s and I'm %d years old" % (name, age)
```

#### String Immutability

```python
text = "Hello"
# text[0] = "h"  # Error: strings are immutable

# Create new string instead
text = "h" + text[1:]  # "hello"
```

#### Looping Through Strings

```python
text = "Python"

# Loop through characters
for char in text:
    print(char)

# Loop with index
for i in range(len(text)):
    print(f"{i}: {text[i]}")
```

### Lists

#### List Basics

```python
# Creating lists
numbers = [1, 2, 3, 4, 5]
mixed = [1, "two", 3.0, True]
empty = []

# List length
length = len(numbers)  # 5

# Accessing elements
first = numbers[0]   # 1
last = numbers[-1]   # 5

# Modifying elements (lists are mutable)
numbers[0] = 10  # [10, 2, 3, 4, 5]
```

#### List Methods

```python
numbers = [1, 2, 3]

# Add elements
numbers.append(4)      # [1, 2, 3, 4]
numbers.extend([5, 6]) # [1, 2, 3, 4, 5, 6]
numbers.insert(0, 0)   # [0, 1, 2, 3, 4, 5, 6]

# Remove elements
numbers.pop()          # Removes and returns last element
numbers.pop(0)         # Removes element at index 0
numbers.remove(3)      # Removes first occurrence of 3
numbers.clear()        # Removes all elements

# Find elements
index = numbers.index(3)  # Returns index of first 3
count = numbers.count(2)  # Counts occurrences of 2

# Check membership
if 3 in numbers:
    print("3 is in the list")

# Sort and reverse
numbers.sort()          # Sort in place (ascending)
numbers.sort(reverse=True)  # Sort descending
numbers.reverse()       # Reverse in place
sorted_nums = sorted(numbers)  # Returns new sorted list
```

#### List Slicing

```python
numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]

# Basic slicing
numbers[2:5]    # [2, 3, 4]
numbers[:5]     # [0, 1, 2, 3, 4]
numbers[5:]     # [5, 6, 7, 8, 9]
numbers[::2]    # [0, 2, 4, 6, 8]
numbers[::-1]   # [9, 8, 7, 6, 5, 4, 3, 2, 1, 0]

# Last n elements
numbers[-3:]    # [7, 8, 9]
```

#### List Comprehensions

```python
# Create list with loop
squares = [x**2 for x in range(10)]
# [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# With condition
evens = [x for x in range(10) if x % 2 == 0]
# [0, 2, 4, 6, 8]

# Nested comprehension
matrix = [[i*j for j in range(3)] for i in range(3)]
# [[0, 0, 0], [0, 1, 2], [0, 2, 4]]
```

#### Built-in List Functions

```python
numbers = [3, 1, 4, 1, 5, 9, 2, 6]

sum(numbers)    # 31
min(numbers)    # 1
max(numbers)    # 9
len(numbers)    # 8
```

#### Looping Through Lists

```python
fruits = ["apple", "banana", "cherry"]

# Loop with elements
for fruit in fruits:
    print(fruit)

# Loop with index
for i in range(len(fruits)):
    print(f"{i}: {fruits[i]}")

# Python Programming Learning Guide - Data Structures (Continued)

## Data Structures

### Intro to Sets
```python
# Unordered collection of unique items
fruits = {"apple", "banana", "cherry"}
print(fruits)

# Duplicates are automatically removed
numbers = {1, 2, 2, 3, 3, 3, 4}
print(numbers)  # {1, 2, 3, 4}

# Create empty set
empty_set = set()
```

### Set Operations
```python
set1 = {1, 2, 3, 4}
set2 = {3, 4, 5, 6}

# Union (all elements from both sets)
union = set1 | set2
print(union)  # {1, 2, 3, 4, 5, 6}

# Intersection (common elements)
intersection = set1 & set2
print(intersection)  # {3, 4}

# Difference (elements in set1 but not in set2)
difference = set1 - set2
print(difference)  # {1, 2}

# Symmetric difference (elements in either set, but not both)
sym_diff = set1 ^ set2
print(sym_diff)  # {1, 2, 5, 6}

# Add element
set1.add(5)

# Remove element
set1.remove(1)  # Raises error if not found
set1.discard(1)  # No error if not found
```

### Set Practice
```python
# Check membership
fruits = {"apple", "banana", "cherry"}

if "apple" in fruits:
    print("Apple is in the set")

# Get length
print(len(fruits))  # 3

# Clear all elements
fruits_copy = fruits.copy()
fruits_copy.clear()
print(fruits_copy)  # set()

# Remove duplicates from list
numbers = [1, 2, 2, 3, 3, 3, 4, 4]
unique_numbers = list(set(numbers))
print(unique_numbers)  # [1, 2, 3, 4]
```

### Intro to Dictionaries
```python
# Key-value pairs
student = {
    "name": "Alice",
    "age": 20,
    "grade": "A"
}

# Access values
print(student["name"])  # Alice
print(student.get("age"))  # 20

# Add/modify entries
student["email"] = "alice@example.com"
student["age"] = 21

print(student)
```

### Dict Operations
```python
person = {
    "name": "Bob",
    "age": 25,
    "city": "New York"
}

# Get value with default
email = person.get("email", "No email")
print(email)  # No email

# Check if key exists
if "name" in person:
    print("Name exists")

# Get all keys
keys = person.keys()
print(keys)  # dict_keys(['name', 'age', 'city'])

# Get all values
values = person.values()
print(values)  # dict_values(['Bob', 25, 'New York'])

# Get all items (key-value pairs)
items = person.items()
print(items)  # dict_items([('name', 'Bob'), ('age', 25), ('city', 'New York')])
```

### Dict Looping
```python
student = {
    "name": "Charlie",
    "age": 22,
    "major": "Computer Science"
}

# Loop through keys
for key in student:
    print(key)

# Loop through values
for value in student.values():
    print(value)

# Loop through key-value pairs
for key, value in student.items():
    print(f"{key}: {value}")
```

### Dict Practice
```python
# Create a dictionary of word counts
text = "hello world hello python world"
words = text.split()

word_count = {}
for word in words:
    if word in word_count:
        word_count[word] += 1
    else:
        word_count[word] = 1

print(word_count)  # {'hello': 2, 'world': 2, 'python': 1}

# Using get() method (cleaner approach)
word_count = {}
for word in words:
    word_count[word] = word_count.get(word, 0) + 1

print(word_count)
```

### Dict Remove
```python
person = {
    "name": "David",
    "age": 30,
    "city": "Boston",
    "email": "david@example.com"
}

# Remove specific key
del person["email"]

# Remove and return value
age = person.pop("age")
print(age)  # 30

# Remove last inserted item (Python 3.7+)
last_item = person.popitem()
print(last_item)  # ('city', 'Boston')

print(person)  # {'name': 'David'}
```

### Dict Values
```python
inventory = {
    "apples": 50,
    "bananas": 30,
    "oranges": 40
}

# Get all values
quantities = inventory.values()
print(list(quantities))  # [50, 30, 40]

# Sum all values
total = sum(inventory.values())
print(total)  # 120

# Max value
max_quantity = max(inventory.values())
print(max_quantity)  # 50

# Find key with max value
max_item = max(inventory, key=inventory.get)
print(max_item)  # apples
```

---

## Input/Output

### Reading Input
```python
# Get user input (always returns string)
name = input("Enter your name: ")
print(f"Hello, {name}!")

# Input without prompt
data = input()
print(data)
```

### Type Conversion with Input
```python
# Convert input to integer
age = int(input("Enter your age: "))
print(f"Next year you'll be {age + 1}")

# Convert input to float
price = float(input("Enter price: "))
print(f"With tax: ${price * 1.1:.2f}")

# Convert input to boolean (careful - any non-empty string is True)
response = input("Continue? (yes/no): ")
continue_flag = response.lower() == "yes"
```

### Parse Input
```python
# Split input by spaces
numbers = input("Enter numbers separated by spaces: ")
num_list = numbers.split()
print(num_list)

# Convert to integers
num_list = [int(x) for x in numbers.split()]
print(sum(num_list))

# Parse comma-separated values
data = input("Enter values separated by commas: ")
values = data.split(",")
values = [x.strip() for x in values]  # Remove whitespace
print(values)
```

### Reading Input Practice
```python
# Calculate rectangle area
width = float(input("Enter width: "))
height = float(input("Enter height: "))
area = width * height
print(f"Area: {area}")

# Multiple inputs on one line
print("Enter two numbers separated by space:")
a, b = input().split()
a, b = int(a), int(b)
print(f"Sum: {a + b}")

# Read multiple lines
lines = []
print("Enter text (type 'done' to finish):")
while True:
    line = input()
    if line.lower() == "done":
        break
    lines.append(line)
print("You entered:", lines)
```

---

## Error Handling

### Try Except
```python
# Basic error handling
try:
    number = int(input("Enter a number: "))
    print(f"You entered: {number}")
except:
    print("That's not a valid number!")
```

### Error Catching
```python
# Catch specific error types
try:
    numerator = int(input("Enter numerator: "))
    denominator = int(input("Enter denominator: "))
    result = numerator / denominator
    print(f"Result: {result}")
except ValueError:
    print("Please enter valid integers!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

### Multiple Except Blocks
```python
# Handle different errors differently
try:
    age = int(input("Enter your age: "))
    
    if age < 0:
        raise ValueError("Age cannot be negative")
    
    years_to_100 = 100 / age
    print(f"You'll reach 100 in {years_to_100:.1f} years")
    
except ValueError as e:
    print(f"Invalid input: {e}")
except ZeroDivisionError:
    print("Age cannot be zero!")
except Exception as e:
    print(f"An unexpected error occurred: {e}")
else:
    print("Calculation completed successfully!")
finally:
    print("Thank you for using the program!")
```

### Complete Error Handling Example
```python
def safe_divide(a, b):
    """Safely divide two numbers with error handling"""
    try:
        result = float(a) / float(b)
        return result
    except ValueError:
        print("Error: Both inputs must be numbers")
        return None
    except ZeroDivisionError:
        print("Error: Cannot divide by zero")
        return None
    except Exception as e:
        print(f"Unexpected error: {e}")
        return None

# Test the function
print(safe_divide(10, 2))      # 5.0
print(safe_divide(10, 0))      # Error message, returns None
print(safe_divide("10", "a"))  # Error message, returns None
```

---
