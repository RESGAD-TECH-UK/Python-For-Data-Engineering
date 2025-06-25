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


