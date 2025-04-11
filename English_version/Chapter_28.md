### 🧩 Chapter 28: Anonymous Power — The Lambda 🔦
*from **Adventure in Python** by Sergey Samoylov*

---

They arrived at a land of whispers.

Small, fleeting constructs flickered in the distance,  
used once, then gone. No name, no trace — just action.

The Companion leaned in:

> “Not every function needs a name.  
> Sometimes, one moment is enough.”

---

### 🧩 Topic: Lambda Functions

Lambda functions are **anonymous** functions.

They’re useful when you want a quick function  
without the formality of `def`.

```python
square = lambda x: x * x
print(square(5))  # Output: 25
```

This is **equivalent** to:

```python
def square(x: int) -> int:
    return x * x
```

---

### 📌 Syntax:

```python
lambda parameters: expression
```

- You can have **any number of parameters**.
- But only **one expression**, no statements.
- The result is **automatically returned**.

---

### 🧠 Where to Use Lambda?

- With `sorted()`, `map()`, `filter()`, `reduce()`.
- As short functions for callbacks or configuration.

```python
names = ["Zoe", "Alice", "Bob"]
names.sort(key=lambda name: len(name))
print(names)
```

---

### 🧪 Task: Sort by Last Letter

You’re given a list of strings:

```python
words = ["tree", "sky", "apple", "wind"]
```

Use `sort()` and a lambda function  
to sort them by **last letter**.

Expected output:

```python
['wind', 'tree', 'apple', 'sky']
```

---

[Chapter 29](Chapter_29.md)
