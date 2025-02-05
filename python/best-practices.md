# 🦎 9 BEST PRACTICES FOR CLEANER CODE

<br></br>

## 1️⃣ Use Descriptive Variable Names

### ❌ Bad Practice

```python
x = 10
y = 20
z = x + y
```

<hr>

### ✅ Good Practice

```python
price = 10
tax = 20
total_price = price + tax
```


<br>

## 2️⃣ Avoid Hardcoding Values

### ❌ Bad Practice

```python
if score > 90:
    print("Excellent")
```

<hr>

### ✅ Good Practice

```python
HIGH_SCORE = 90
if score > HIGH_SCORE:
    print("Excellent")
```


<br>

## 3️⃣ Keep Functions Small and Focused

### ❌ Bad Practice

```python
def calculate_and_print_area(length, width):
    area = length * width
    print(f"Area: {area}")
```

<hr>

### ✅ Good Practice

```python
def calculate_area(length, width):
    return length * width
    
print(f"Area: {calculate_area(5, 10)}")
```


<br>

## 4️⃣ Use List Comprehensions for Simple Loops

### ❌ Bad Practice

```python
squares = []
for i in range(10):
    squares.append(i**2)
```

<hr>

### ✅ Good Practice

```python
squares = [i**2 for i in range(10)]
```


<br>

## 5️⃣ Handle Exceptions Properly

### ❌ Bad Practice

```python
try:
    result = 10 / 0
except:
    print("Error")
```

<hr>

### ✅ Good Practice

```python
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```


<br>

## 6️⃣ Avoid Mutable Default Arguments

### ❌ Bad Practice

```python
def add_item(item, items=[]):
    items.append(item)
    return items
```

<hr>

### ✅ Good Practice

```python
def add_items(item, items=None):
    if items is None:
        items = []
    items.append(item)
    return items
```


<br>

## 7️⃣ Write Readable Conditional Statements

### ❌ Bad Practice

```python
if is_admin == True:
    print("Access granted")
```

<hr>

### ✅ Good Practice

```python
if is_admin:
    print("Access granted")
```


<br>

## 8️⃣ Use f-Strings for String Formatting

### ❌ Bad Practice

```python
name = "John"
print("Hello, %s!" % name)
```

<hr>

### ✅ Good Practice

```python
name = "John"
print(f"Hello, {name}!")
```


<br>

## 9️⃣ Follow PEP 8 for Indentation and Spacing

### ❌ Bad Practice

```python
def func(a,b):
    return(a+b)
```

<hr>

### ✅ Good Practice

```python
def fun(a, b):
    return a + b
```