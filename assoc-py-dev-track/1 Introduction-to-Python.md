# Introduction to Python for Developers

# Python — Chapter 1 Cheat Sheet

## What is Python? + Variables + Data Types


---

## 1. What is Python?

**Python** is a **general-purpose programming language**.

It can be used for:

* Apps
* Automation
* Websites
* Data science
* Many other tasks

Why is Python popular?

* Easy-to-read syntax
* Large developer community
* Free and open-source
* Used by companies such as Facebook, Netflix, and Spotify. 

### Basic Python code

```python
print("Hello!")
```

Output:

```text
Hello!
```

---

# 2. Python Scripts

A **Python script** is a file containing Python code that we can run.

Usually, Python files use:

```text
.py
```

Example:

```text
recipe_scaler.py
```

The chapter introduces a recipe scaler as an example and emphasizes four development practices: **start small, iterate, test, and document**. 

### Good development habits

```text
Start small
    ↓
Iterate
    ↓
Test
    ↓
Document
```

---

# 3. `print()`

`print()` is a **built-in Python function** used to display results.

```python
print("Hello, world!")
```

Output:

```text
Hello, world!
```

Both single and double quotes can be used:

```python
print("Hello, world!")
print('Hello, world!')
```

Both produce:

```text
Hello, world!
```



### Remember

```python
print(value)
```

means:

> **Display `value` on the screen.**

---

# 4. Comments

A **comment** explains what the code does.

Comments start with:

```python
#
```

Example:

```python
# This is a comment
# The below is a print function
print("Hello, world!")
```

Python ignores comments when running the code. 

### Quick rule

```python
# comment
```

**`#` → Python comment**

---

# 5. Variables

A **variable** stores information so that we can reuse it later.

Instead of repeatedly typing the same value:

```python
ingredient_name = "Tomatoes"
```

We can use:

```python
print(ingredient_name)
```

Output:

```text
Tomatoes
```

Variables make code:

* Easier to read
* Easier to update
* Reusable
* Less repetitive



---

# 6. Creating a Variable

Basic syntax:

```python
variable_name = value
```

Example:

```python
ingredient_name = "Tomatoes"
```

Here:

| Part              | Meaning       |
| ----------------- | ------------- |
| `ingredient_name` | Variable name |
| `=`               | Assignment    |
| `"Tomatoes"`      | Value         |

### Naming variables

DataCamp uses **lowercase letters + underscores** for spaces:

```python
ingredient_name
ingredient_quantity
new_ingredient_quantity
```

Not:

```python
ingredient name
```



---

# 7. Main Data Types

A **data type** tells Python what kind of value something is.

The chapter introduces four important types:

| Data type | Meaning        | Example      |
| --------- | -------------- | ------------ |
| `str`     | Text           | `"Tomatoes"` |
| `int`     | Whole number   | `2`          |
| `float`   | Decimal number | `1.5`        |
| `bool`    | True/False     | `True`       |

Python automatically assigns a data type to a value. 

---

# 8. Strings — `str`

A **string** is text.

Strings can contain:

* Letters
* Numbers
* Punctuation

Examples:

```python
"Hello, world!"
"20-minute pasta recipe"
```



### Quotes

You can use either:

```python
"Hello"
```

or:

```python
'Hello'
```

If the text contains an apostrophe, double quotes can make the code easier:

```python
"Chef's secret seasoning"
```



### Important

This is a string:

```python
"20"
```

This is **not** a string:

```python
20
```

The quotes make the difference.

---

# 9. Integers — `int`

An **integer** is a whole number.

Examples:

```python
2
10
100
-5
```

No quotation marks are needed.

Example from the chapter:

```python
ingredient_quantity = 2
```



---

# 10. Floats — `float`

A **float** is a number containing a decimal.

Example:

```python
new_ingredient_quantity = 1.5
```

Other examples:

```python
3.14
10.5
0.25
```

No quotation marks are needed. 

---

# 11. Booleans — `bool`

A **Boolean** has only two possible values:

```python
True
False
```

Useful for **yes/no** or **on/off** information.

Example:

```python
is_in_stock = True
```

or:

```python
is_in_stock = False
```

### Important

`True` and `False` start with **capital letters** and do **not** use quotation marks. 

Correct:

```python
is_in_stock = True
```

Wrong:

```python
is_in_stock = "True"
```

The second one is a **string**, not a Boolean.

---

# 12. Printing Variables

You can pass a variable to `print()`:

```python
ingredient_name = "Tomatoes"
ingredient_quantity = 2

print(ingredient_name)
print(ingredient_quantity)
```

Output:

```text
Tomatoes
2
```



---

# 13. Changing a Variable

Variables can be reassigned.

Initially:

```python
ingredient_quantity = 2

print(ingredient_quantity)
```

Output:

```text
2
```

Then change it:

```python
ingredient_quantity = 1

print(ingredient_quantity)
```

Output:

```text
1
```

The variable now contains `1` instead of `2`. 

### Think of it like a box

```text
ingredient_quantity
       ↓
      [ 2 ]
```

After:

```python
ingredient_quantity = 1
```

It becomes:

```text
ingredient_quantity
       ↓
      [ 1 ]
```

---

# 14. `type()` — Find the Data Type

Use:

```python
type()
```

to find the type of a value or variable. 

### Examples

```python
ingredient_name = "tomatoes"

print(type(ingredient_name))
```

Output:

```text
<class 'str'>
```

---

```python
ingredient_quantity = 2

print(type(ingredient_quantity))
```

Output:

```text
<class 'int'>
```

---

```python
new_ingredient_quantity = 1.5

print(type(new_ingredient_quantity))
```

Output:

```text
<class 'float'>
```

---

```python
is_in_stock = True

print(type(is_in_stock))
```

Output:

```text
<class 'bool'>
```



### Easy memory trick

```text
"Hello"  → str
2        → int
1.5      → float
True     → bool
```

---

# 15. Operators

**Operators** are symbols used to perform calculations.

The chapter introduces:

| Operator | Meaning        | Example  |
| -------- | -------------- | -------- |
| `+`      | Addition       | `2 + 3`  |
| `-`      | Subtraction    | `5 - 2`  |
| `*`      | Multiplication | `3 * 4`  |
| `/`      | Division       | `10 / 2` |



### Numbers

Numbers work like normal mathematics:

```python
print(2 + 1.5)
```

Output:

```text
3.5
```

---

# 16. Operators with Strings

For strings, the chapter shows that `+` and `*` can be used.

### `+` → Join strings

```python
"Hi" + "There"
```

Result:

```text
"HiThere"
```

### `*` → Repeat a string

```python
"Hi" * 3
```

Result:

```text
"HiHiHi"
```



---

# 🧠 Quick Review

```python
# String
name = "Tomatoes"

# Integer
quantity = 2

# Float
price = 1.5

# Boolean
is_available = True
```

Check the types:

```python
print(type(name))          # <class 'str'>
print(type(quantity))      # <class 'int'>
print(type(price))         # <class 'float'>
print(type(is_available))  # <class 'bool'>
```

Print values:

```python
print(name)
print(quantity)
print(price)
print(is_available)
```

---

# ⚡ One-Minute Cheat Sheet

| Concept   | Remember                          |
| --------- | --------------------------------- |
| `print()` | Display something                 |
| `#`       | Comment                           |
| `=`       | Assign a value to a variable      |
| Variable  | Stores/reuses information         |
| `str`     | Text                              |
| `int`     | Whole number                      |
| `float`   | Decimal number                    |
| `bool`    | `True` / `False`                  |
| `type()`  | Check data type                   |
| `+`       | Add numbers / join strings        |
| `-`       | Subtract                          |
| `*`       | Multiply numbers / repeat strings |
| `/`       | Divide                            |

### Most important examples

```python
name = "Tomatoes"     # str
quantity = 2          # int
price = 1.5           # float
available = True      # bool
```

```python
print(name)
print(type(name))
```

---

## 📦 Example: Recipe Data

The chapter's examples revolve around ingredients, so here's the **raw data represented directly in Python**:

```python
ingredient_name = "Tomatoes"
ingredient_quantity = 2
new_ingredient_quantity = 1.5
is_in_stock = True
```

| Variable                  |    Raw value | Type    |
| ------------------------- | -----------: | ------- |
| `ingredient_name`         | `"Tomatoes"` | `str`   |
| `ingredient_quantity`     |          `2` | `int`   |
| `new_ingredient_quantity` |        `1.5` | `float` |
| `is_in_stock`             |       `True` | `bool`  |

These are the example values actually shown in the PDF.  

---

## 🔑 The Big Picture

Think of Python like this:

```text
VALUE
  ↓
DATA TYPE
  ↓
STORE IT IN A VARIABLE
  ↓
USE THE VARIABLE
  ↓
PRINT / CALCULATE / MODIFY
```

Example:

```python
ingredient_quantity = 2

ingredient_quantity = 1

print(ingredient_quantity)
```

Output:

```text
1
```

**Core idea of this chapter:**
Python variables let you **store information**, data types tell you **what kind of information it is**, `print()` lets you **see it**, `type()` lets you **check its type**, and operators let you **work with the values**. 
