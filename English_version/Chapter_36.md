### 🏗️ Chapter 36: Building Libraries — The Power of `__init__.py` 📚  
*from **Adventure in Python** by Sergey Samoylov*

---

The sky above the digital valley shimmered — like a folder being opened.

Hero stood on the edge of a vast archive of knowledge.  
Sprawling folders, tiny `.py` files — all whispering secrets of reuse.

The Companion handed over a mysterious object:

> "A box with many tools inside.  
> You’ve built tools before.  
> Now… build toolboxes."

---

### 🧠 Topic: Python Packages and `__init__.py`

You’ve learned to write **modules** — individual `.py` files.

But what if you want a whole **collection** of related tools?

That’s where **packages** come in.

A **package** is just a **folder** that contains modules —  
and a magical file: `__init__.py`.

---

### 🧪 Step-by-step Example

Let’s say you want a package for math tools.

📁 Folder structure:

```
math_tools/
├── __init__.py
├── add.py
└── multiply.py
```

---

#### `add.py`

```python
def add(a: int, b: int) -> int:
    """Return the sum of two numbers"""
    return a + b
```

#### `multiply.py`

```python
def multiply(a: int, b: int) -> int:
    """Return the product of two numbers"""
    return a * b
```

#### `__init__.py`

```python
from .add import add
from .multiply import multiply
```

> Why `from .add`?  
> The `.` means “from this same folder” — relative import.

---

### 🔧 Now Use the Package

📄 `main.py`

```python
from math_tools import add, multiply

print(add(3, 4))        # 7
print(multiply(2, 5))   # 10
```

You’ve now created your own Python **library**.

Just like `math`, `random`, or `datetime` — but it’s **yours**.

---

### ✨ Hero’s Realization

He no longer feared complexity.  
He started to organize it.

Just as the world around him grew larger,  
so did his ability to shape it.

He wasn’t just coding anymore.  
He was **designing systems**.

---

### 🧩 Challenge: Make Your First Package

Create a folder named `string_magic`  
Inside it, create:

- `reverse.py`: with a function `reverse_text(text: str) -> str`
- `mirror.py`: with a function `mirror_text(text: str) -> str`
- An `__init__.py` that exposes both

Then test your package with:

```python
from string_magic import reverse_text, mirror_text
```

Use your powers wisely — the toolbox is growing.

---

[Chapter 37](Chapter_37.md)
