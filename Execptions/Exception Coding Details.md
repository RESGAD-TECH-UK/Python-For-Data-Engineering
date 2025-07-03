## try statement

## raise statement

## assert statement

The `assert` statement is used to check **conditions during development**. If the condition is `False`, it raises an `AssertionError`.

```python
assert test_condition, "Optional error message"
```

This is shorthand for:

```python
if __debug__:
    if not test_condition:
        raise AssertionError("Optional error message")
```

**Key Points:**

* Used to **catch bugs early** by enforcing constraints (e.g., preconditions, invariants).
* Raises `AssertionError` when the test condition is `False`.
* You can add a custom message to help with debugging.


**Optimization and the `-O` Flag**

* Python **removes `assert` statements** when code is run with the `-O` (optimize) flag:

  ```bash
  python -O your_script.py
  ```

* In optimized mode:

  * `__debug__` is set to `False`.
  * Any code guarded by `if __debug__:` or `assert` is **ignored**.
  * Example: constraints won't be checked and errors won’t be raised.

**When to Use `assert`**

* Use for **development-only checks** (not essential to program correctness).
* Good for **debugging assumptions** and enforcing **internal constraints**.
* Don’t use `assert` for:

  * User input validation
  * Runtime error handling
  * Critical logic


## with statement