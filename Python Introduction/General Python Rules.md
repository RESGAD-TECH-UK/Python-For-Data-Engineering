# Python Code Style Guidelines (PEP 8)

Following the [PEP 8 style guide](https://www.python.org/dev/peps/pep-0008/) ensures your Python code is readable, consistent, and easier to maintain. Whether you're working with a team or coding solo, good style matters.


### 1. **Whitespace Rules**

* Use **4 spaces** per indentation level (not tabs).
* Limit lines to **79 characters**.
* Add:

  * **2 blank lines** between functions or classes.
  * **1 blank line** between methods in a class.
* Align continued lines with **4 extra spaces**.
* In dictionaries:

  ```python
  config = {"host": "localhost", "port": 8080}
  ```
* Use **one space** before and after `=` in assignments:

  ```python
  count = 10
  ```
* For type hints:

  ```python
  age: int = 25
  ```


### 2. **Naming Conventions**

* **Functions, variables**: `snake_case`
* **Protected attributes**: `_leading_underscore`
* **Private attributes**: `__double_leading_underscore`
* **Classes, exceptions**: `CapitalizedWord`
* **Constants**: `ALL_CAPS`
* **Method parameters**:

  * `self` for instance methods
  * `cls` for class methods


### 3. **Expression & Statements**

* Don't check for empty containers or sequence by comparing the length to zero, E.g., 

```python
some_list = []

#Don't use:
if len(some_list) == 0:

#Instead use:
if not some_list:
```

* Instead of trying to fit all your code into a single line, use multiple lines, indentation, and parentheses, E.g.,

```python
#Don't do this:
total = (price * quantity) - (discount * 0.1) + tax_rate * 50

#Instead do this:
total = (
    (price * quantity)
    - (discount * 0.1)
    + tax_rate * 50
)
```

* When importing libraries or modules, start at the top of the file with the standard, then the third party, lastly your project libraries. E.g., 

```python
# Standard library
import datetime
import os
import sys

# Third-party libraries
import numpy as np
import pandas as pd
import requests

# Your own modules
import data_loader
import utils
```