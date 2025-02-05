# 🐍 PYTHON - CHEAT SHEET

<br></br>

## 📚 Fundamentals

```python
x = 5   # variables

print("Your mom")   # print to console

# this is a comment

'''multiline 
comment'''
```


<br></br>

## 🔤 Data Types

### Primitive

```python
str = "Your mom"    # string

int = 42    # whole number (integer)

float = 3.14    # decimal

bool = True     # boolean
```

<hr>

### Collections

```python
list = [1, 2, 3]

tuple = (1, 2, 3)

set = {1, 2, 3}

dict = {"key": "value"}  # dictionary
```


<br></br>

## 📋 Operators

- Arithmetic:  ```+``` ```-``` ```*``` ```/``` ```//``` ```%``` ```**```

- Comparison: ```==``` ```!=``` ```<``` ```>``` ```<=``` ```=>```

- Logical: ```and``` ```or``` ```not```

- Membership: ```in``` ```not in```

- Identity: ```is``` ```is not```


<br></br>

## 🔀 Conditionals

- If: ```if x > y:```

- Elif: ```elif x < y:```

- Else: ```else:```


<br></br>

## ➿ Loops

- For: ```for x in range(5)```

- While: ```while x < 5```

- Break: ```break```

- Continue: ```continue```


<br></br>

## ⚙️ Functions

```python
# defining
def my_function():

# calling
my_function()

# default parameters
def function(x, y=0)

# variable-length arguments
def func(*args, **kwargs):
```


<br></br>

## 🏛️ Classes & Objects

```python
# class definition
class MyClass:

# constructor
def __init__(self):

# instance methods
def method(self):

# static methods
@staticmethod
def my_static_method(arg1, arg2):
    # do something with both args
    return result

# class variables
class_var = 0

# object instantiation
my_object = MyClass()

# inheritance
class DerivedClass(BaseClass):

# method overriding
def method(self):
```


<br></br>

## 🚨 Error Handling

```python
try:    # try

except Exception as e:  # except (catch)

raise ValueError("Error message")   # raise error

finally:    # finally
```


<br></br>

## 📑 Importing Libraries

- Import - ```import numpy```

- Alias - ```import numpy as np```

- Specific import - ```from math import pi```


<br></br>

## 📂 File I/O

- Open - ```with open("file.txt", "r") as file:```

- Read - ```file.read()```

- Write - ```with open("file.txt", "w") as file:```

- Append - ```with open("file.txt", "a") as file:```


<br></br>

## 📜 List Comprehensions

- Syntax - ```[expression for item in iterable if condition]```


<br></br>

## 📝 Lambda Functions

- Syntax - ```lambda arguments: expression```


<br></br>

## 🔌 Iterators & Generators

- Iterator - ```iter(obj)```

- Next item - ```next(iterator)```

- Generator function
    ```python
    def my_generator(): yield value
    ```

- Generator expression - ```(expression for item in iterable if condition)```


<br></br>

## 🔍 Context Managers

```python
# defining
class MyContext:

# enter method
def __enter__(self):

# exit method
def __exit__(self, exc_type, exc_value, traceback):

# using
with MyContext() as my_context:
```


<br></br>

## 🛠️ Built-in Functions

- ```len(obj)``` → length of object

- ```sum(iterable[, start])``` → sum of elements

- ```max(iterable[, key])``` → maximum element

- ```min(iterable[, key])``` → minimum element

- ```sorted(iterable[, key][, reverse])``` → sorted list

- ```range(stop[, start][, step])``` → sequence of numbers

- ```zip(*iterables)``` → iterator of tuples

- ```map(function, iterable)``` → apply function to all items

- ```filter(function, iterable)``` → filter elements by function

- ```isinstance(obj, classInfo)``` → check object's class


<br></br>

## 🧵 String Methods

### ```lower()``` → lowercase 
```python
"Python".lower()    # "python"
```

<hr>

### ```upper()``` → uppercase 
```python
"Python".upper()    # "PYTHON"
```

<hr>

### ```strip()``` → remove leading/trailing characters
```python
" Python ".strip()  # "Python"
```

<hr>

### ```split([sep])``` → split by separator  
```python
"Python is cool".split(" ")    # ['Python', 'is', 'cool']
```

<hr>

### ```replace(old, new[, count])``` → replace substring
```python
"Pythin".replace("i", "o")  # "Python"
```

<hr>

### ```find(sub[, start][, end])``` → find substring index
```python
"Python is cool".find("cool")   # 10
```

<hr>

### ```format(*args, **kwargs)``` → format string
```python
name = "Cosmo"
language - "Python"

greeting = "Hello, my name is {} amd I love {}!".format(name, language)

# OR

greeting = "Hello, my name is {name} and I love {language}!".format(name="Cosmo", language="Python")
```


<br></br>

## 📃 List Methods

### ```append(item)``` → add item to end 
```python
lst = [1, 2, 3]
lst.append(4)   # lst = [1, 2, 3, 4]
```

<hr>

### ```extend(iterable)``` → add elements of iterable
```python
lst = [1, 2, 3]
lst.extend([4, 5, 6])   # lst = [1, 2, 3, 4, 5, 6]
```

<hr>

### ```insert(index, item)``` → insert item at index 
```python
lst = [1, 2, 3]
lst.insert(1, 99)   # lst = [1, 99, 2, 3]
```

<hr>

### ```remove(item)``` → remove first occurrence 
```python
lst = [1, 2, 3, 2]
lst.remove(2)   # lst = [1, 3, 2] (only removes 1st '2')
```

<hr>

### ```pop([index])``` → remove & return item
```python
lst = [1, 2, 3]
last_item = lst.pop()   # last_item = 3 | lst = [1, 2]
second_item = lst.pop(1)    # second_item = 2 | lst = [1]
```

<hr>

### ```index(item[, start][, end])``` → find item index
```python
lst = [10, 20, 30, 40, 30]
idx = lst.index(30)     # idx = 2 (first occurrence)
idx2 = lst.index(30, 3)     # idx2 = 4 (finds 30 starting from index 3)
```

<hr>

### ```count(item)``` → count occurrences
```python
lst = [1, 2, 3, 2, 2, 4]
count - lst.count(2)    # count = 3 (2 appears three times)
```

<hr>

### ```sort([key][, reverse])``` → sort list 
```python
lst = [3, 2, 4, 1, 5, 9]
lst.sort()      # lst = [1, 1, 3, 4, 5, 9]

lst.sort(reverse=True)  # lst = [9, 5, 4, 3, 1, 1]

fruits = ["banana", "apple", "cherry"]
fruits.sort(key=len)    # sort by length → words = ["apple", "banana", "cherry"]
```

<hr>

### ```reverse()``` → reverse list 
```python
lst = [1, 2, 3, 4]
lst.reverse()   # lst = [4, 3, 2, 1]
```

<br></br>

## 📖 Dictionary Methods

### ```keys()``` → view list of keys 
```python
cat = {"name": "Cosmo", "age": 10, "city": "Fairfax"}
keys = cat.keys()   # dict_keys(['name', 'age', 'city'])
```

<hr>

### ```values()``` → view list of values
```python
values = cat.values()   # dict_values(['Cosmo', 10, 'Fairfax'])
```

<hr>

### ```items()``` → view key-value pairs
```python
items = cat.items()     # dict_items([('name', 'Cosmo'), ('age')])
```

<hr>

### ```get(key[, default])``` → get value for key
```python
age = cat.get("age")    # 10
toys = cat.get("toys", "Not specified")     # "Not specified" (default value)
```

<hr>

### ```update([other])``` → update dictionary
```python
cat.update({"toys": ["mouse", "bird"], "city": "Tallahassee"})  # cat = {'name': 'Cosmo', 'age': 10, 'city': 'Tallahassee', 'toys': ['mouse', 'bird']}
```

<hr>

### ```pop(key[, default])``` → remove & return value
```python
age = cat.pop("age")    # 10 (removes 'age' from the dictionary)
missing = cat.pop("behavior", "Not provided")   # "Not provided" (default value)
```

<hr>

### ```clear()``` → remove all items
```python
cat.clear()     # cat = {}
```


<br></br>

## 🔢 Set Methods

### ```add(item)``` - add item
```python
s = {1, 2, 3}
s.add(4)
# s = {1, 2, 3, 4}
```

<hr>

### ```update(iterable)``` - add elements of iterable
```python
s.update([5, 6, 7])
# s = {1, 2, 3, 4, 5, 6, 7}
```

<hr>

### ```discard(item)``` - remove item if present
```python
s.discard(3)
# s = {1, 2, 4, 5, 6, 7} (no error if item is missing)

s.discard(100)
# No error even though 100 is not in the set
```

<hr>

### ```remove(item)``` - remove item or raise KeyError
```python
s.remove(2)
# s = {1, 4, 5, 6, 7}

s.remove(100)
# ❌ Raises KeyError because 100 is not in the set
```

<hr>

### ```pop()``` - remove & return item
```python
item = s.pop()
# removes a random item from 's' and returns it
```

<hr>

### ```clear()``` - remove all items
```python
s.clear()   # s = set()
```

<hr>

### ```union(*others)``` - union of sets
```python
a = {1, 2, 3}
b = {3, 4, 5}
c = a.union(b)
# c = {1, 2, 3, 4, 5} (combines both sets)
```

<hr>

### ```intersection(*others)``` - intersection of sets
```python
a = {1, 2, 3}
b = {2, 3, 4}
c = a.intersection(b)
# c = {2, 3} (common elements)
```

<hr>

### ```difference(*others)``` - difference of sets
```python
a = {1, 2, 3, 4}
b = {3, 4, 5}
c = a.difference(b)
# c = {1, 2} (elements in 'a' but not in 'b')
```

<hr>

### ```issubset(other)``` - check if subset
```python
small = {1, 2}
big = {1, 2, 3, 4}
is_subset = small.issubset(big)
# True (all elements of 'small' are in 'big')
```

<hr>

### ```issuperset(other)``` - check if superset
```python
is_superset = big.issuperset(small)
# True ('big' contains all elements of 'small')
```

<br></br>

## 🖼️ Regular Expressions (```re``` module)

### 1️⃣ Import the module → ```import re```

- Before using regular expressions, you need to import Python's built-in ```re``` module

```python
import re
```

<hr>

### 2️⃣ ```re.search(pattern, string)```

- Finds the first match of the pattern anywhere in the string

```python
result = re.search(r"\d", "Price: 100 dollars")
print(result.group())   # "100"
```

<hr>

### 3️⃣ ```re.match(pattern, string)```

- Checks if the pattern appears at the start of the string

```python
result = re.match(r"Your", "Your, mom!")
print(bool(result))     # True

result2 = re.match(r"mom", "Your, mom!")
print(bool(result2))    # False (does not start with "mom")
```

<hr>

### 4️⃣ ```re.findall(pattern, string)```

- Finds all matches in a string and returns a list

```python
result = re.findall(r"\d+", "Order 3 apples, 5 bananas, and 10 oranges")
print(result)  # ['3', '5', '10']
```

<hr>

### 5️⃣ ```re.sub(pattern, repl, string)```

- Replaces all occurrences of ```pattern``` with ```repl```

```python
text = "I love cats! Cats are cute."
result = re.sub(r"cats", "dogs", text, flags=re.IGNORECASE)
print(result)  # "I love dogs! Dogs are cute."
```

<hr>

### 🧮 Common Patterns

| Pattern | Meaning |
| ------- | ------- |
| ```\d``` | Digit (0-9) |
| ```\w``` | Word character (a-z, A-Z, 0-9, _) |
| ```\s``` | Whitespace (space, tab, newline) |
| ```.``` | Any character except newline |
| ```^``` | Start of a string |
| ```$``` | End of a string |
| ```*``` | 0 or more occurrences |
| ```+``` | 1 or more occurrences |
| ```?``` | 0 or 1 occurrence |
| ```{n}``` | Exactly ```n``` occurrences |
| ```{n,}``` | At least ```n``` occurrences |
| ```{,m}``` | At most ```m``` occurrences |
| ```{n,m}``` | Between ```n``` and ```m``` occurrences |

#### Examples:

```python
re.findall(r"\d+", "123 Main St, Apt 4B")  
# ['123', '4']

re.findall(r"\w+", "Hello, world!")  
# ['Hello', 'world']

re.findall(r"^Hello", "Hello, world!")  
# ['Hello'] (matches only if "Hello" is at the start)

re.findall(r"end$", "The story will end")  
# ['end'] (matches only if "end" is at the end)
```