### 🌐 Chapter 29: Map and Transformations 🗺️  
*from **Adventure in Python** by Sergey Samoylov*

---

The land shimmered like flowing code.

The air smelled like loops and change.  
The hero stepped into a stream of data,  
and it began to twist and reshape around him.

> “This stream,” whispered the Companion,  
> “will change anything it touches.”

> “What does it change things into?”  
> asked the hero.

> “Whatever you command it to become.”

---

### 🧠 Topic: The `map()` function

Sometimes, we want to apply **a function**  
to every element in a sequence.

This is called **mapping**.

The built-in function `map()` does just that.

---

### 🔧 Syntax:

```python
map(function, iterable)
```

It returns an **iterator**, not a list.

You usually wrap it in `list()`.

---

### 🔬 Example:

```python
def double(x: int) -> int:
    return x * 2

numbers: list[int] = [1, 2, 3, 4]
doubled: list[int] = list(map(double, numbers))

print(doubled)
```

✅ Output:
```python
[2, 4, 6, 8]
```

---

### ⚡ Using `lambda` with `map`:

```python
words: list[str] = ["Adventure", "Python"]
lengths: list[int] = list(map(lambda w: len(w), words))

print(lengths)
```

✅ Output:
```python
[9, 6]
```

---

### 🧪 Task: First Letters

Given a list of names:

```python
names = ["Alice", "Bob", "Clara"]
```

Use `map()` and a lambda to extract  
only the **first letter** of each name.

Expected result:

```python
['A', 'B', 'C']
```

---

[Chapter 30](Chapter_30.md)
