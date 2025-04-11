## 🧊 Chapter 25: Immutable Truth – Tuples 🔐  
*from *Adventure in Python* by Sergey Samoylov*

---

> “It looks like a list,”  
> the Hero muttered, poking the new data object.  
> “But it feels... different.”

The Terminal pulsed one word:  
```python
tuple
```

---

### 🧱 What’s a Tuple?

A **tuple** is like a list, but **immutable**.

That means: **you can’t change it** after creation.

---

### 📦 Tuple Syntax

```python
colors: tuple[str, str, str] = ("red", "green", "blue")
```

✅ Uses parentheses  
✅ Can hold values of any types  
✅ Items are ordered  
✅ Can contain duplicates

---

### 🚫 No Modification

```python
colors[0] = "yellow"  # ❌ Error!
```

Python will raise:

```text
TypeError: 'tuple' object does not support item assignment
```

That’s the whole point.

---

### 🛡 Why Use Tuples?

- Tuples are **faster** than lists  
- They **guarantee stability**  
- Perfect for **constants** or unchanging data  
- They can be **used as dictionary keys**

---

### 🔍 One-Element Tuples

This is tricky:

```python
lonely: tuple[str] = ("single",)  # ← Comma is key!
```

Without the comma, it’s just a string in parentheses.

---

### 🧙‍♂️ Wisdom in Immutability

The Hero leaned back.

> “Maybe the value of something…  
> comes from not being able to change it.”

The Companion nodded slowly.  
Not everything needs to be flexible.

---

### 🎯 Challenge: Tuple Translator

Create a tuple of command keywords.  
Ask the user to enter a command.

If it matches something in the tuple, print "OK".  
Otherwise, print "Unknown command".

Don't use a list.  
Make the tuple immutable on purpose.

---

The Terminal flickered in approval.

> “When data is final, logic becomes clear.”

Another shard of truth, unlocked.

---

[Chapter 25](Chapter_25.md), which is a quarter of 100, is waiting for you.
