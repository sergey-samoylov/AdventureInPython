## 🐍 Chapter 22: The Truth Behind False 🪞  
*from Adventure in Python by Sergey Samoylov*

---

The hallway flickered with strange signs.

The Terminal whispered:  
> “Not everything that exists is True.  
> Not everything empty is gone.”

The hero stopped.

> “What does that even mean?”

> “You must learn the *truthiness* of things.”

---

### ✅ Truthy and Falsy

In Python, some values **evaluate as True**,  
others as **False**, even without being `True` or `False`.

Let’s explore that:

```python
if "hello":
    print("This string is True")
```

Now try:

```python
if "":
    print("This won't be printed")
```

---

### 🔎 The Falsy Club

These values are **considered False**:

- `None`
- `False`
- `0`, `0.0`, `0j`
- `""` (empty string)
- `[]` (empty list)
- `{}` (empty dict)
- `set()`, `tuple()`, `range(0)`

Everything else is **True**.

---

### 🔍 Why It Matters

This lets us write code like:

```python
user_input: str = input("Enter something: ")

if not user_input:
    print("You entered nothing!")
```

Instead of:

```python
if user_input == "":
    print("You entered nothing!")
```

Same logic, cleaner code.

---

### 🧪 Bonus: `bool()` Function

Want to test truthiness?

```python
print(bool(0))       # False
print(bool("text"))  # True
```

---

### 🧠 Challenge: Filter Truth

Create a list of mixed values:  
some `None`, some empty, some valid.

Then use a list comprehension  
to filter only the **truthy** ones:

```python
mixed_values: list = ["text", "", None, 0, 42, [], [1]]

# Your filtered list should be: ['text', 42, [1]]
```

---

### 🧠 Reflection

> “So... truth is not always a value?”  
> asked the hero.

> “Correct,” said the Terminal.  
> “It’s what a value means  
> when tested under pressure.”

> “Like in life,” whispered the shadows.

---

To bool or not to bool?

True / False is in question.

[Chapter 23](Chapter_23.md) awaits!
