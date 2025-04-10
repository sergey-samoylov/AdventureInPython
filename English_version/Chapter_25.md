## 🧱 Chapter 20: Modules and Files 📂  
*from Adventure in Python by Sergey Samoylov*

---

The Machine buzzed.  
A humming sound filled the digital air.

> "You have learned to write code,"  
> said the voice,  
> "but now, you must learn to **organize** it."

---

### 📚 Why Break Code Into Files?

Our hero had been living in the terminal,  
writing small bits of code, running them, tweaking them.

But real programs grow.  
They become **too big** to handle in one place.

> “You don’t build a castle from one stone.”

You split your project into **modules**.

---

### 📦 What Is a Module?

A module is simply a `.py` file  
that contains Python code.

You can **import** it into another file  
and reuse its functions, classes, or variables.

---

### ✍️ Writing Your First Module

Create a file named `tools.py`:

```python
def greet(name: str) -> None:
    """
    Prints a friendly greeting.
    """
    print(f"Hello, {name}!")
```

Now in a new file:

```python
import tools

tools.greet("Companion")
```

Simple.  
Elegant.  
Modular.

---

### 🧭 The Power of Imports

There are different ways to import:

```python
from tools import greet

greet("Hero")
```

But be careful:

- Avoid `from x import *`
- Keep names clear
- Think in terms of long-term structure

---

### 📁 Folders Become Packages

As code grows, you’ll need folders.

Create a folder: `utilities/`  
Inside it, place `math_utils.py`.

Make sure to include an empty file:  
`__init__.py`

Now `utilities` is a **package**.

You can import with:

```python
from utilities import math_utils
```

Or:

```python
from utilities.math_utils import multiply
```

---

### 🧠 Challenge: Create Your Toolkit

Create a folder called `mymodule`.

Inside, create:

- `text_utils.py`
- `math_utils.py`

In `text_utils.py`, write a function  
that counts words in a string.

In `math_utils.py`, write a function  
that multiplies two numbers.

Test them from a separate file called `main.py`.

---

### 🧠 Reflection

> “At first, I thought code was just commands,”  
> whispered the hero,  
> “but now I see — it's **architecture**.”

> “Indeed,” the Machine replied,  
> “And well-structured code is the foundation  
> of powerful creation.”

---

Should we check [Chapter 21](Chapter_21.md)
