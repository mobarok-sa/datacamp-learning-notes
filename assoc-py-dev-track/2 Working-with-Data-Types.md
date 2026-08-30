# Working-with-Data-Types.md

# Python Chapter 2 — Cheat Sheet

## Strings, Lists, Dictionaries, Sets & Tuples

This chapter is about **working with collections of data** and manipulating strings. The examples mainly use a recipe/ingredients theme. 

---

# 1. Strings

A **string (`str`)** is text.

Strings are used everywhere in programming, for example:

* Messages
* User input
* File names
* Output formatting
* Data/text processing 

### Single or double quotes

Both are valid:

```python
ingredient_name = 'San Marzano tomatoes'

ingredient_name = "San Marzano tomatoes"
```



### When text contains `'`

Use double quotes:

```python
ingredient_name = "Chef's special seasoning"
```

Using single quotes incorrectly:

```python
ingredient_name = 'Chef's special seasoning'
```

causes:

```text
SyntaxError: invalid syntax
```



### Easy rule

```text
"Hello"       → string
'Hello'       → string
"Chef's food" → useful when text contains '
```

---

# 2. Multi-line Strings

Use **triple quotes** `"""` when the string covers multiple lines.

```python
recipe_instructions = """1. Bring a large pot of salted water to boil and cook pasta
2. Heat olive oil in a pan and sauté minced garlic until fragrant
3. Add chopped tomatoes and simmer for 10 minutes
4. Toss cooked pasta with tomato sauce and fresh basil leaves
"""
```

Useful for:

* Long text
* Instructions
* Documentation
* Error messages



### Remember

```python
"""text"""
```

→ **multi-line string**

---

# 3. String Methods

A **method** is a function available for a particular data type.

Basic structure:

```python
string_variable.method()
```

String methods are commonly used to **transform or standardize text**. 

---

## `.replace()`

Used to replace part of a string.

Syntax:

```python
string.replace(old, new)
```

Example:

```python
welcome_message = "Welcome to the recipe scaler, George"

welcome_message = welcome_message.replace("George", "John")

print(welcome_message)
```

Output:

```text
Welcome to the recipe scaler, John
```



### Remember

```python
text.replace("old", "new")
```

---

## `.lower()`

Converts text to lowercase.

```python
ingredient_name = "Basil Leaves"

ingredient_name = ingredient_name.lower()

print(ingredient_name)
```

Output:

```text
basil leaves
```

---

## `.upper()`

Converts text to uppercase.

```python
ingredient_name = "Basil Leaves"

ingredient_name = ingredient_name.upper()

print(ingredient_name)
```

Output:

```text
BASIL LEAVES
```

These methods can be useful when standardizing user input, such as email addresses. 

### String methods quick table

| Method       | What it does |
| ------------ | ------------ |
| `.lower()`   | lowercase    |
| `.upper()`   | UPPERCASE    |
| `.replace()` | Replace text |

---

# 4. Lists

## Why lists?

Imagine storing ingredients separately:

```python
ingredient_one = "pasta"
ingredient_two = "tomatoes"
ingredient_three = "garlic"
ingredient_four = "basil"
ingredient_five = "olive oil"
ingredient_six = "salt"
```

This becomes difficult to manage. 

A **list** lets you store multiple values in **one variable**.

```python
ingredients = [
    "pasta",
    "tomatoes",
    "garlic",
    "basil",
    "olive oil",
    "salt"
]
```

A list can contain different data types. 

---

# 5. List Indexing

Lists are:

* **Ordered**
* **Indexed**
* Start counting from **0**

Example:

```python
ingredients = [
    "pasta",
    "tomatoes",
    "garlic",
    "basil",
    "olive oil",
    "salt"
]
```

Index positions:

```text
Index:       0          1          2        3        4           5
             ↓          ↓          ↓        ↓        ↓           ↓
Value:     pasta    tomatoes    garlic    basil   olive oil    salt
```



### Access an element

Syntax:

```python
list[index]
```

Examples:

```python
print(ingredients[0])
```

Output:

```text
pasta
```

```python
print(ingredients[3])
```

Output:

```text
basil
```



---

# 6. Getting the Last List Element

You can use the actual index:

```python
ingredients[5]
```

or, much easier:

```python
ingredients[-1]
```

Both return:

```text
salt
```



### Important

```text
[0]  → first
[1]  → second
[2]  → third
[-1] → last
```

---

# 7. List Slicing

Slicing lets you get **multiple elements**.

Syntax:

```python
list[start:stop]
```

⚠️ The `stop` index is **not included**.

Example:

```python
print(ingredients[1:3])
```

Result:

```python
["tomatoes", "garlic"]
```

Why?

```text
index:     0          1          2          3
                    ↑          ↑
                  start       stop
                              NOT included
```



### More examples

From index 3 onward:

```python
ingredients[3:]
```

Result:

```python
["basil", "olive oil", "salt"]
```

First three elements:

```python
ingredients[:3]
```

Result:

```python
["pasta", "tomatoes", "garlic"]
```



### Remember

```text
list[start:stop]

start → included
stop  → NOT included
```

---

# 8. Step in List Slicing

You can add a third number:

```python
list[start:stop:step]
```

Example:

```python
ingredients[::2]
```

Means:

> Start from the beginning and take every 2nd element.

Result:

```python
["pasta", "garlic", "olive oil"]
```

Indexes:

```text
0 → pasta
2 → garlic
4 → olive oil
```

Another example:

```python
ingredients[1::3]
```

Result:

```python
["tomatoes", "olive oil"]
```

Indexes:

```text
1 → tomatoes
4 → olive oil
```



### Slicing cheat sheet

```python
items[:]       # all
items[2:]      # index 2 → end
items[:3]      # beginning → before index 3
items[::2]     # every 2nd item
items[1::3]    # every 3rd item starting at index 1
```

---

# 9. Dictionaries

A **dictionary** stores data as:

```text
key → value
```

Think of it like a real dictionary:

```text
word → definition
```



### Why dictionaries?

They are useful when you want to connect related information.

For example:

```text
ingredient → quantity
```

Instead of having two separate lists:

```python
ingredients = ["pasta", "tomatoes", ...]
quantities = [500, 400, ...]
```

you can connect them directly in a dictionary. 

---

# 10. Creating a Dictionary

Syntax:

```python
dictionary = {
    "key": value
}
```

Example:

```python
recipe = {
    "pasta": 500,
    "tomatoes": 400,
    "garlic": 15,
    "basil": 20,
    "olive oil": 30,
    "salt": 5
}
```



Think:

```text
"pasta"     → 500
"tomatoes"  → 400
"garlic"    → 15
```

---

# 11. Accessing Dictionary Values

With a list:

```python
ingredients[0]
```

With a dictionary, use the **key**:

```python
recipe["pasta"]
```

Output:

```text
500
```



### Easy comparison

```python
# List
ingredients[0]

# Dictionary
recipe["pasta"]
```

**List → index**

**Dictionary → key**

---

# 12. Dictionary `.values()`

Get all values:

```python
recipe.values()
```

Example:

```python
print(recipe.values())
```

Output:

```text
dict_values([500, 400, 15, 20, 30, 5])
```



---

# 13. Dictionary `.keys()`

Get all keys:

```python
recipe.keys()
```

Output:

```text
dict_keys(['pasta', 'tomatoes', 'garlic', 'basil', 'olive oil', 'salt'])
```



---

# 14. Dictionary `.items()`

Get **key-value pairs**:

```python
recipe.items()
```

Example output:

```text
[
    ('pasta', 500),
    ('tomatoes', 400),
    ('garlic', 15),
    ('basil', 20),
    ('olive oil', 30),
    ('salt', 5)
]
```



### Dictionary methods

| Code              | Meaning           |
| ----------------- | ----------------- |
| `recipe.keys()`   | All keys          |
| `recipe.values()` | All values        |
| `recipe.items()`  | Key + value pairs |

---

# 15. Adding to a Dictionary

Simply assign a new key:

```python
recipe["parmesan"] = 50
```

Now the dictionary contains:

```python
"parmesan": 50
```



### Pattern

```python
dictionary["new_key"] = value
```

---

# 16. Updating a Dictionary Value

If the key already exists, assigning a new value **updates** it.

```python
recipe["pasta"] = 1000
```

The old value:

```text
pasta → 500
```

becomes:

```text
pasta → 1000
```



### Important difference

```python
recipe["parmesan"] = 50
```

→ adds a new key if it doesn't exist.

```python
recipe["pasta"] = 1000
```

→ updates the existing key.

---

# 17. Duplicate Dictionary Keys

A dictionary should have unique keys.

Example:

```python
recipe = {
    "pasta": 500,
    "garlic": 5,
    "garlic": 15
}
```

There are two `"garlic"` keys.

The resulting value is:

```python
recipe["garlic"]
```

```text
15
```

The later value replaces the earlier one. 

### Remember

```text
Duplicate key → later value wins
```

---

# 18. Sets

A **set** is useful when you need **unique values**.

Main characteristics from the chapter:

* Contains unique data
* Doesn't support changing individual elements
* You can add/remove values
* Useful for removing duplicates
* Fast for searching compared with structures such as lists 

### Example

```python
ingredients = {
    "pasta",
    "tomatoes",
    "pasta",
    "basil",
    "garlic",
    "olive oil",
    "salt"
}
```

Notice:

```text
"pasta"
"pasta"
```

appears twice.

But the set stores it only once.



---

# 19. Creating a Set

A set uses `{}` **without key-value pairs**:

```python
ingredients = {"pasta", "tomatoes", "garlic"}
```

A dictionary uses:

```python
recipe = {"pasta": 500}
```

### Easy distinction

```text
{"pasta", "tomatoes"}     → set

{"pasta": 500}            → dictionary
          ↑
        colon
```

The chapter specifically highlights this distinction. 

---

# 20. Converting a List to a Set

Use:

```python
set()
```

Example:

```python
ingredients_list = [
    "pasta",
    "tomatoes",
    "garlic",
    "basil",
    "olive oil",
    "pasta",
    "salt"
]

unique_ingredients = set(ingredients_list)
```

Now duplicate `"pasta"` is removed.



Result:

```python
{
    "pasta",
    "tomatoes",
    "garlic",
    "basil",
    "olive oil",
    "salt"
}
```

---

# 21. Set Limitations

Sets don't have indexes.

Therefore, this doesn't work:

```python
unique_ingredients[0]
```

It produces:

```text
TypeError: 'set' object is not subscriptable
```



### Therefore

```text
List  → indexed → items[0] works

Set   → no index → items[0] doesn't work
```

Also, sets cannot contain duplicates.

---

# 22. Sorting a Set

You can use:

```python
sorted()
```

Example:

```python
print(sorted(ingredients))
```

Result:

```python
[
    "basil",
    "garlic",
    "olive oil",
    "pasta",
    "salt",
    "tomatoes"
]
```

Important:

> `sorted()` returns a **list**.



So:

```python
sorted(my_set)
```

→ **list**

---

# 23. Tuples

A **tuple** is an ordered collection that **cannot be changed**.

It is **immutable**.

You cannot:

* Add values
* Remove values
* Change values

But tuples:

* Are ordered
* Can be accessed using indexes
* Are useful for information such as locations or identifiers. 

---

# 24. Creating a Tuple

Use parentheses:

```python
serving_sizes = (1, 2, 4, 6, 8)
```

You can also convert another data structure into a tuple:

```python
ingredients_tuple = tuple(ingredients_list)
```



---

# 25. Accessing a Tuple

Tuples use indexes like lists:

```python
serving_sizes = (1, 2, 4, 6, 8)

print(serving_sizes[1])
```

Output:

```text
2
```



### But...

This works:

```python
serving_sizes[1]
```

This does **not**:

```python
serving_sizes[1] = 10
```

because tuples are immutable.

---

# 🧠 Lists vs Dictionaries vs Sets vs Tuples

This is probably the **most important table to remember from this chapter**:

| Structure      | Main idea            | Ordered? |    Index? | Duplicates? |            Change values? |
| -------------- | -------------------- | -------: | --------: | ----------: | ------------------------: |
| **List**       | Collection of values |        ✅ |         ✅ |           ✅ |                         ✅ |
| **Dictionary** | Key → value          |        ✅ | Key-based | Keys unique |                         ✅ |
| **Set**        | Unique values        | No index |         ❌ |           ❌ | Elements can't be changed |
| **Tuple**      | Fixed collection     |        ✅ |         ✅ |           ✅ |                         ❌ |

### Easy mental model

```text
LIST
"I have a bunch of things."
        ↓
["pasta", "garlic", "salt"]


DICTIONARY
"I want to connect a name to a value."
        ↓
{"pasta": 500, "garlic": 15}


SET
"I only want unique things."
        ↓
{"pasta", "garlic", "salt"}


TUPLE
"I have things that should stay fixed."
        ↓
("Riyadh", 24.7, 46.7)
```

---

# 📌 Chapter 2 Quick Cheat Sheet

```python
# STRING
name = "Basil Leaves"

name.lower()              # "basil leaves"
name.upper()              # "BASIL LEAVES"
name.replace("Basil", "Mint")


# LIST
ingredients = ["pasta", "tomatoes", "garlic"]

ingredients[0]            # first
ingredients[-1]           # last
ingredients[1:3]          # slice
ingredients[::2]         # every 2nd


# DICTIONARY
recipe = {
    "pasta": 500,
    "tomatoes": 400
}

recipe["pasta"]            # 500
recipe["salt"] = 5         # add
recipe["pasta"] = 1000     # update

recipe.keys()              # keys
recipe.values()            # values
recipe.items()             # key-value pairs


# SET
unique = set(ingredients)

sorted(unique)             # returns a list


# TUPLE
sizes = (1, 2, 4, 6, 8)

sizes[1]                   # 2
```

---

# 📦 Raw Data from the PDF Examples

Since you specifically want the **raw example data** preserved for your GitHub notes, here are the actual values shown in this chapter.

### Ingredients

```python
ingredients = [
    "pasta",
    "tomatoes",
    "garlic",
    "basil",
    "olive oil",
    "salt"
]
```

### Quantities — grams

```python
quantities = [500, 400, 15, 20, 30, 5]
```

The PDF explicitly labels these quantities as **grams**. 

| Ingredient | Quantity (g) |
| ---------- | -----------: |
| pasta      |          500 |
| tomatoes   |          400 |
| garlic     |           15 |
| basil      |           20 |
| olive oil  |           30 |
| salt       |            5 |

### Recipe dictionary

```python
recipe = {
    "pasta": 500,
    "tomatoes": 400,
    "garlic": 15,
    "basil": 20,
    "olive oil": 30,
    "salt": 5
}
```

Later, the PDF adds:

```python
recipe["parmesan"] = 50
```

So the updated data includes:

```python
recipe = {
    "pasta": 500,
    "tomatoes": 400,
    "garlic": 15,
    "basil": 20,
    "olive oil": 30,
    "salt": 5,
    "parmesan": 50
}
```



### Serving sizes

```python
serving_sizes = (1, 2, 4, 6, 8)
```

The PDF uses these as a tuple example. 

---

# ⭐ What You Should Remember

If you only have **2 minutes to review Chapter 2**, remember these:

```text
STRING
→ Text
→ .lower(), .upper(), .replace()


LIST
→ Multiple values
→ Ordered
→ Starts at index 0
→ Can use [index] and slicing


DICTIONARY
→ key : value
→ Access using ["key"]
→ .keys(), .values(), .items()


SET
→ Unique values
→ Removes duplicates
→ No indexing


TUPLE
→ Ordered
→ Indexed
→ Cannot be changed
```

### The biggest difference

```text
Need an ordered collection?
        ↓
      LIST

Need key → value?
        ↓
   DICTIONARY

Need unique values?
        ↓
      SET

Need a fixed/unchangeable collection?
        ↓
     TUPLE
```

This chapter's progression is essentially **String → List → Dictionary → Set → Tuple**, with each structure solving a different data-storage problem.   
