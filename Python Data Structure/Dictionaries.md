# Dictionaries

## Overview
A **dictionary** stores a collection of key-value pairs, where key and value are Python **objects**—this includes strings, numbers, lists, dictionaries, and more (since nearly everything in Python is an object). In other programming languages they're referred to as associative arrays or hashes. Represented as `dictionary = {key1:value, key2:values, .......}`. 
> Quick explanation what we mean by associative arrays and hashes: Associative arrays or hashes rely on hashable keys, It means the key has a fixed identity, meaning its value (the key itself) is immutable and has a stable hash code—an internal identifier under the hood used to quickly locate the associated value in the dictionary. This allows efficient lookups, even if the value itself is not hashable.

```python
key = (1, 2, 3)   # a tuple (hashable)
print(hash(key))


key = [1, 2, 3]   # a list (unhashable)
print(hash(key))  # Raises TypeError
```
What this means is that, you can use a tuple as a key in a dictionary, but you cannot use a list as a key.



## Different Ways of Creating Dictionaries
- **Using curly braces:** `{"a": 1, "b": 2}` 

This is the most common and direct way to define a dictionary when you know the key-value pairs in advance.

```python
student_scores = {"Aisha": 80, "Kaycee": 70, "Collins": 78, "Maureen": 85, "Agnes": 75, "Jerry": 48}
print(student_scores)
```
- **Using `dict()`:** `dict(a=1, b=2)`

Useful for creating dictionaries from keyword arguments when keys are valid identifiers (i.e., strings that are valid variable names).

```python
student_scores = dict(Aisha = 80, Kaycee = 70, Collins = 78, Maureen = 85, Agnes = 75, Jerry = 48)
print(student_scores)
```

- **Dictionary comprehension:** `{k: v for k, v in iterable}`

Useful for creating dictionaries from keyword arguments when keys are valid identifiers (i.e., strings that are valid variable names).

```python
squares = {x: x**2 for x in range(1, 6)}
print(squares)  # Output: {1: 1, 2: 4, 3: 9, 4: 16, 5: 25}

import random
y = ["Aisha", "Kaycee", "Collins", "Maureen", "Agnes", "Jerry", ("Aisha", "jerry"), "Collins"] 
student_score = {y[x]: random.randint(45, 100) for x in range(len(y))}

When you run this code, you will notice that the second "Collins" over-rides the first as you can't have a duplicate key. 
```

## Dictionary Usage
Dictionaries are used to store and retrieve data efficiently using unique keys.

---

## How Are Dictionaries Used?
- Lookups by key
- Counting and aggregating
- Representing structured data
- Data transformation


---

## Operations You Can Perform on Dictionaries
- `get()`, `keys()`, `values()`, `items()`
- Adding, updating, deleting
- Iteration and comprehension
- Nesting and merging
