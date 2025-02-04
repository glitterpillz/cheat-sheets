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

- Primitive
    ```python
    str = "Your mom"    # string

    int = 42    # whole number (integer)

    float = 3.14    # decimal

    bool = True     # boolean
    ```

- Collections
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

- Lowercase → ```lower()```
    ```python
    "Python".lower()    # "python"
    ```

- Uppercase → ```upper()``` 
    ```python
    "Python".upper()    # "PYTHON"
    ```

- Remove leading/trailing characters → ```strip()``` 
    ```python
    " Python ".strip()  # "Python"
    ```

- Split by separator → ```split([sep])``` 
    ```python
    "Python is cool".split(" ")    # ['Python', 'is', 'cool']
    ```

- Replace substring → ```replace(old, new[, count])``` 
    ```python
    "Pythin".replace("i", "o")  # "Python"
    ```

- Find substring index → ```find(sub[, start][, end])```
    ```python
    "Python is cool".find("cool")   # 10
    ```

- Format string → ```format(*args, **kwargs)```
    ```python
    name = "Cosmo"
    language - "Python"

    greeting = "Hello, my name is {} amd I love {}!".format(name, language)

    # OR

    greeting = "Hello, my name is {name} and I love {language}!".format(name="Cosmo", language="Python")
    ```


<br></br>

## 📃 List Methods

- Add item to end → ```append(item)```
    ```python
    lst = [1, 2, 3]
    lst.append(4)   # lst = [1, 2, 3, 4]
    ```

- Add elements of iterable - ```extend(iterable)```
    ```python
    lst = [1, 2, 3]
    lst.extend([4, 5, 6])   # lst = [1, 2, 3, 4, 5, 6]
    ```

- Insert item at index - ```insert(index, item)```
    ```python
    lst = [1, 2, 3]
    lst.insert(1, 99)   # lst = [1, 99, 2, 3]
    ```

- Remove first occurrence - ```remove(item)```
    ```python
    lst = [1, 2, 3, 2]
    lst.remove(2)   # lst = [1, 3, 2] (only removes 1st '2')
    ```

- Remove & return item - ```pop([index])```
    ```python
    lst = [1, 2, 3]
    last_item = lst.pop()   # last_item = 3 | lst = [1, 2]
    second_item = lst.pop(1)    # second_item = 2 | lst = [1]
    ```

- Find item index - ```index(item[, start][, end])```
    ```python
    lst = [10, 20, 30, 40, 30]
    idx = lst.index(30)     # idx = 2 (first occurrence)
    idx2 = lst.index(30, 3)     # idx2 = 4 (finds 30 starting from index 3)
    ```

- Count occurrences - ```count(item)```
    ```python
    lst = [1, 2, 3, 2, 2, 4]
    count - lst.count(2)    # count = 3 (2 appears three times)
    ```

- Sort list - ```sort([key][, reverse])```
    ```python
    lst = [3, 2, 4, 1, 5, 9]
    lst.sort()      # lst = [1, 1, 3, 4, 5, 9]

    lst.sort(reverse=True)  # lst = [9, 5, 4, 3, 1, 1]

    fruits = ["banana", "apple", "cherry"]
    fruits.sort(key=len)    # sort by length → words = ["apple", "banana", "cherry"]
    ```
