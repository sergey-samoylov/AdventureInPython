### 🎁 Chapter 32: Unpacking the Unknown 🧞   
*from *Adventure in Python* by Sergey Samoylov*

---

The digital wind brought mysteries.  
The hero stood before gates of tuples.  
Each held many values. But how to open them?

> “Not all treasures are in boxes,”  
> said the Companion.  
> “Some just need to be unpacked.”

---

### 🪢 Topic: Unpacking Tuples and Lists

In Python, you can **unpack** values  
from tuples, lists, or other iterables  
into separate variables.

---

### 🔧 Basic Syntax:

```python
a, b = (1, 2)
```

Now `a` is `1`, `b` is `2`.

This works with lists, too:

```python
first, second = ["hi", "there"]
```

---

### 🧪 Useful in Loops:

```python
pairs: list[tuple[str, int]] = [
    ("Alice", 85),
    ("Bob", 91),
    ("Cleo", 78)
]

for name, score in pairs:
    print(f"{name} got {score} points")
```

---

### 🧪 Task: Unpack and Report

Given this list of pairs:

```python
data = [("Python", 1991), ("Java", 1995), ("Rust", 2010)]
```

Write a loop to print lines like:

```text
Python was created in 1991
Java was created in 1995
Rust was created in 2010
```

---

[Chapter 33](Chapter_33.md)
