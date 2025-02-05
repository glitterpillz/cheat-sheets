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

### ```len(obj)``` → length of object

### ```sum(iterable[, start])``` → sum of elements

### ```max(iterable[, key])``` → maximum element

### ```min(iterable[, key])``` → minimum element

### ```sorted(iterable[, key][, reverse])``` → sorted list

### ```range(stop[, start][, step])``` → sequence of numbers

### ```zip(*iterables)``` → iterator of tuples

### ```map(function, iterable)``` → apply function to all items

### ```filter(function, iterable)``` → filter elements by function

### ```isinstance(obj, classInfo)``` → check object's class


<br></br>

## 🧵 String Methods

### ```lower()``` → lowercase 
    ```python
    "Python".lower()    # "python"
    ```

### ```upper()``` → uppercase 
    ```python
    "Python".upper()    # "PYTHON"
    ```

### ```strip()``` → remove leading/trailing characters
    ```python
    " Python ".strip()  # "Python"
    ```

### ```split([sep])``` → split by separator  
    ```python
    "Python is cool".split(" ")    # ['Python', 'is', 'cool']
    ```

### ```replace(old, new[, count])``` → replace substring
    ```python
    "Pythin".replace("i", "o")  # "Python"
    ```

### ```find(sub[, start][, end])``` → find substring index
    ```python
    "Python is cool".find("cool")   # 10
    ```

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

### ```extend(iterable)``` → add elements of iterable
    ```python
    lst = [1, 2, 3]
    lst.extend([4, 5, 6])   # lst = [1, 2, 3, 4, 5, 6]
    ```

### ```insert(index, item)``` → insert item at index 
    ```python
    lst = [1, 2, 3]
    lst.insert(1, 99)   # lst = [1, 99, 2, 3]
    ```

### ```remove(item)``` → remove first occurrence 
    ```python
    lst = [1, 2, 3, 2]
    lst.remove(2)   # lst = [1, 3, 2] (only removes 1st '2')
    ```

### ```pop([index])``` → remove & return item
    ```python
    lst = [1, 2, 3]
    last_item = lst.pop()   # last_item = 3 | lst = [1, 2]
    second_item = lst.pop(1)    # second_item = 2 | lst = [1]
    ```

### ```index(item[, start][, end])``` → find item index
    ```python
    lst = [10, 20, 30, 40, 30]
    idx = lst.index(30)     # idx = 2 (first occurrence)
    idx2 = lst.index(30, 3)     # idx2 = 4 (finds 30 starting from index 3)
    ```

### ```count(item)``` → count occurrences
    ```python
    lst = [1, 2, 3, 2, 2, 4]
    count - lst.count(2)    # count = 3 (2 appears three times)
    ```

### ```sort([key][, reverse])``` → sort list 
    ```python
    lst = [3, 2, 4, 1, 5, 9]
    lst.sort()      # lst = [1, 1, 3, 4, 5, 9]

    lst.sort(reverse=True)  # lst = [9, 5, 4, 3, 1, 1]

    fruits = ["banana", "apple", "cherry"]
    fruits.sort(key=len)    # sort by length → words = ["apple", "banana", "cherry"]
    ```

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

### ```values()``` → view list of values
    ```python
    values = cat.values()   # dict_values(['Cosmo', 10, 'Fairfax'])
    ```

### ```items()``` → view key-value pairs
    ```python
    items = cat.items()     # dict_items([('name', 'Cosmo'), ('age')])
    ```

### ```get(key[, default])``` → get value for key
    ```python
    age = cat.get("age")    # 10
    toys = cat.get("toys", "Not specified")     # "Not specified" (default value)
    ```

### ```update([other])``` → update dictionary
    ```python
    cat.update({"toys": ["mouse", "bird"], "city": "Tallahassee"})  # cat = {'name': 'Cosmo', 'age': 10, 'city': 'Tallahassee', 'toys': ['mouse', 'bird']}
    ```

### ```pop(key[, default])``` → remove & return value
    ```python
    age = cat.pop("age")    # 10 (removes 'age' from the dictionary)
    missing = cat.pop("behavior", "Not provided")   # "Not provided" (default value)
    ```

### ```clear()``` → remove all items
    ```python
    cat.clear()     # cat = {}
    ```


<br></br>

## 🔢 Set Methods

### ```add(item)``` - add item

### ```update(iterable)``` - add elements of iterable

### ```discard(item)``` - remove item if present

### ```remove(item)``` - remove item or raise KeyError

### ```pop()``` - remove & return item

### ```clear()``` - remove all items

### ```union(*others)``` - union of sets

### ```intersection(*others)``` - intersection of sets

### ```difference(*others)``` - difference of sets

### ```issubset(other)``` - check if subset

### ```issuperset(other)``` - check if superset
