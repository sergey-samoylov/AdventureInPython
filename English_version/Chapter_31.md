### 🧩 Chapter 31: Zip the World 🌍  
*from *Adventure in Python* by Sergey Samoylov*

---

The path led to a giant tapestry.  
It was made of two threads, intertwined perfectly. 🪢 

> “Look,” said the Companion.  
> “Each element can be joined with its pair.”  

> “This is how you combine separate patterns into meaning.”

---

### 🖇️ Topic: The `zip()` Function

`zip()` lets you combine two or more iterables,  
element by element.

---

### 🔧 Syntax:

```python
zip(iterable1, iterable2, ...)
```

It returns an **iterator** of tuples.

Use `list()` to see the result.

---

### 🔬 Example:

```python
names: list[str] = ["Alice", "Bob", "Cleo"]
scores: list[int] = [85, 91, 78]

paired: list[tuple[str, int]] = list(zip(names, scores))

print(paired)
```

✅ Output:
```python
[('Alice', 85), ('Bob', 91), ('Cleo', 78)]
```

---

If the lengths don’t match, `zip()` stops at the shortest one.

---

### 🧪 Task: Combine Data

You have:

```python
titles = ["Beginner", "Intermediate", "Pro"]
levels = [1, 2, 3]
```

Create a list of tuples like:

```python
[("Beginner", 1), ("Intermediate", 2), ("Pro", 3)]
```

---

[Chapter 32](Chapter_32.md)
