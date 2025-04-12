### 🧭 Chapter 38: Expanding the Map — Modules and Imports 🎢  
*from* *Adventure in Python by Sergey Samoylov*

---

The world was growing.  
The terrain too vast to be held in one script.

The Companion pointed to the horizon.

> “Python is built on tools that come in boxes.  
> Not everything needs to be written from scratch.”

A glowing box appeared.

```python
import random
```

The box whispered:

> “I am a module.  
> I carry many powers within me.”

---

### 📦 What is a module?

A **module** is a file that contains Python code  
— functions, variables, classes — all reusable.

Think of it as a **toolbox**.  
Instead of reinventing a hammer, you just reach for one.

---

### 🧱 How to import

Use `import` to access built-in or custom modules.

```python
import math

print(math.sqrt(16))  # 4.0
```

You can also import specific parts:

```python
from math import pi

print(pi)  # 3.141592...
```

Or rename for convenience:

```python
import random as rng

print(rng.randint(1, 6))
```

---

### 🌐 Standard Library: a realm of built-in powers

Python comes with many built-in modules. Some favorites:

- `random` – randomness and dice rolls  
- `math` – advanced mathematical tools  
- `datetime` – working with dates and time  
- `os` – interacting with the operating system  
- `sys` – system-specific details  

Try:

```python
import this
```

You’ll be surprised.

---

### 🧰 Custom Modules

You can create your own module too!

If you have a file `tools.py`:

```python
def shout(text: str) -> str:
    return text.upper() + "!"
```

You can use it elsewhere:

```python
import tools

print(tools.shout("hello"))
```

Just make sure `tools.py` is in the same directory.

---

### 🗺️ Hero’s Insight

The Hero stepped back and saw:

> “I no longer walk blindly through the dark.  
> I carry a map… and I can draw new lands upon it.”

---

### 🎯 Challenge: Your Own Toolbox

Create your own module called `battle_utils.py`  
with at least two functions:

1. `roll_dice(sides: int) -> int`  
   Returns a random number from 1 to `sides`.

2. `announce_victory(name: str) -> None`  
   Prints a custom victory message.

Then import and use them in your main program!

You’re no longer limited to this chapter.  
You can build chapters of your own.

---

[Chapter 39](Chapter_39.md)?
