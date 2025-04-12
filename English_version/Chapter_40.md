### ⚖️ Chapter 40: Understanding `is` and `==`  
*from **Adventure in Python** by Sergey Samoylov*

---

The path split in two.

One led to a mirror,  
the other to a reflection of the mirror.

The hero paused.

> “Which one is real?” he asked.  
> The Companion smiled.  
> “That depends on how you compare.”

---

### 🤔 Equality vs Identity

In Python, we have **two** main ways to compare values:

- `==` → **equality** (Do the values look the same?)  
- `is` → **identity** (Are they the exact same object?)

---

### 🎭 `==` — Value Equality

This checks *if values match*.

```python
a = [1, 2, 3]
b = [1, 2, 3]

print(a == b)  # ✅ True: same content
```

---

### 🔍 `is` — Identity

This checks *if both variables point to the same object*.

```python
print(a is b)  # ❌ False: different lists
```

Even if two objects look the same,  
they may not be the same object.

---

### 🔁 But... Sometimes They Are

For simple types like small integers and short strings,  
Python reuses objects for efficiency:

```python
x = "Hi"
y = "Hi"
print(x is y)  # ✅ True (interned string)

n = 5
m = 5
print(n is m)  # ✅ True
```

But don't rely on this!

---

### 🧠 Why It Matters

If you compare objects with `is`  
when you mean `==`, you may get surprises.

This matters a lot with:

- Lists  
- Dictionaries  
- Class instances

---

### 🧪 Quick Test

```python
def compare(a: object, b: object) -> None:
    print(f"a == b: {a == b}")
    print(f"a is b: {a is b}")
```

Try it with:

- `compare([1, 2], [1, 2])`  
- `compare("text", "text")`  
- `compare(True, 1)`

---

### 🧠 Challenge: Clone or Shadow?

Write a function `show_identity()`  
that takes two variables and prints:

- Their values  
- Whether they're equal (`==`)  
- Whether they’re identical (`is`)  
- Their `id()` values

Then try:

```python
a = [42]
b = a
c = [42]

show_identity(a, b)
show_identity(a, c)
```

What changes? What stays?

---

The hero stepped through the reflection.  
He had seen enough.

> "It’s not just about looking alike,"  
> he whispered.  
> "It’s about *being*."

[Chapter 41](Chapter_41.md)
