### 🧰 Chapter 35: Building Tools — Writing Our Own Modules 📱  
*from **Adventure in Python** by Sergey Samoylov*

---

The world around the hero had changed again.

The terminal, his old friend, glowed with a quiet pulse.  
But now — it was cluttered. Bits of code everywhere.  
Reusable parts… but scattered.

The Companion blinked into view and placed a hand on the code:

> — It’s time to clean this up.  
> Let’s give your tools a home.

---

### 📚 Topic: Writing Your Own Python Modules

A **module** is a Python file with functions, classes, or constants  
that you want to reuse.

You’ve been writing code in one file so far.  
Now we separate concerns — we create **toolkits**.

---

### 🧪 Step 1: Create a module file

Let’s say you want a module for math utilities:

📄 `utils.py`

```python
def square(number: int) -> int:
    """Returns the square of a number"""
    return number * number


def cube(number: int) -> int:
    """Returns the cube of a number"""
    return number * number * number
```

---

### 🧪 Step 2: Use your module in another file

📄 `main.py`

```python
import utils

print(utils.square(4))  # 16
print(utils.cube(3))    # 27
```

Now your functions live in their **own file**,  
ready to be reused anytime.

---

### 📦 Bonus: Custom Names

You can rename modules or functions on import:

```python
from utils import square as sq

print(sq(5))  # 25
```

Or import everything (not recommended in large projects):

```python
from utils import *
```

---

### 🧠 The Hero's Mind Expanded

As he created his own modules, something shifted.

This wasn’t just reuse.

This was **architecture**.  
A sign that he wasn’t just surviving.  
He was designing.

He looked at the Companion and said:

> — I want to build something that outlives this loop.  
> Something clean. Beautiful. Reusable.

And the digital world whispered back:  
**“You’re becoming a builder.”**

---

### 🎯 Task: Modularize Your Code

Create a module called `text_tools.py`  
with the following functions:

- `shout(text: str) -> str`: returns text in uppercase with `!`
- `whisper(text: str) -> str`: returns text in lowercase with `...`
- `title_case(text: str) -> str`: returns the title-cased text

Then create a file `demo.py` to test your functions  
by importing and printing their results.

---
[Chapter 36](Chapter_36.md)
