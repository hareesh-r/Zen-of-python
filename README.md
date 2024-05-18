# Zen of Python Examples

This project demonstrates the principles of the Zen of Python through code examples. The Zen of Python is a collection of software design principles for the Python programming language, which can be found by importing the `this` module in Python.

## Principles and Examples

### Beautiful is better than ugly.

```python
# Beautiful
def greet(name):
    print(f"Hello, {name}!")

# Ugly
def greet(name):
    print("Hello, " + name + "!")
```

### Explicit is better than implicit.

```python
# Explicit
import math
radius = 2
area = math.pi * radius ** 2

# Implicit
from math import *
radius = 2
area = math.pi * radius ** 2
```

### Simple is better than complex.

```python
# Simple
def sum_numbers(numbers):
    return sum(numbers)

# Complex
def sum_numbers(numbers):
    total = 0
    for number in numbers:
        total += number
    return total
```

### Complex is better than complicated.

```python
# Complex
groceries = ["banana", "orange", "peanut butter", "rice", "lentils"]
fruits = ["banana", "orange", "apple", "blueberries"]
fruits_groceries = [item for item in groceries if item in fruits]

# Complicated
groceries = ["banana", "orange", "peanut butter", "rice", "lentils"]
fruits = ["banana", "orange", "apple", "blueberries"]

fruits_groceries = []
for item in groceries:
    if item in fruits:
        fruits_groceries.append(item)
```

### Flat is better than nested.

```python
# Flat
def check_apples(item: str, num: int):
    if item == "apple" and num == 0:
        print("No apples")
    elif item == "apple" and num > 10:
        print("Yup, we got apples - but there's too many")
    elif item == "apple" and num == 0:
        print("No apples")
    elif item != "apple":
        print("Item is not an apple!")

# Nested
def check_apples(item: str, num: int):
    if item == "apple":
        if num == 0:
            print("No apples")
        elif num > 10:
            print("Yup, we got apples - but there's too many")
        elif num == 0:
            print("No apples")
    else:
        print("Item is not an apple!")
```

### Sparse is better than dense.

```python
# Sparse
name = "Hareesh"
age = 22
print(f"{name}'s age is {age}")

# Dense
name, age = "Hareesh", 22
print(f"{name}'s age is {age}")
```

### Readability counts.

```python
# Readable
distance_traveled = starting_point + speed * time

# Less readable
d = sp + s * t

# More less readable
d=sp+s*t
```

### Errors should never pass silently.

```python
# Alerting on error
try:
    with open('config.txt', 'r') as cfg:
        settings = cfg.read()
except Exception as e:
    print("Error:")
    print(e)

# Passing silently
try:
    with open('config.txt', 'r') as cfg:
        settings = cfg.read()
except:
    pass
```

### Unless explicitly silenced.

```python
# This is OK
try:
    with open('config.txt', 'r') as cfg:
        settings = cfg.read()
except IOError:
    pass
except Exception as e:
    print("Error")
    print(e)
```

### In the face of ambiguity, refuse the temptation to guess.

```python
# Refuse to guess
age = input("What is your age")
try:
    int(age.strip())
except:
    raise ValueError("Invalid age")
```

### There should be one-- and preferably only one --obvious way to do it.

```python
# Obvious way
greetings = "Hello World"
print(greetings.lower())

# Less obvious way
print("".join([char.lower() for char in greetings]))
```
### Now is better than never.
### Although never is often better than right now.
### If the implementation is hard to explain, it's a bad idea.
### If the implementation is easy to explain, it may be a good idea.
### Namespaces are one honking great idea -- let's do more of those!

