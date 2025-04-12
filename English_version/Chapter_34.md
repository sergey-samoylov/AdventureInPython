### 🍀 Chapter 34: `**kwargs` and Named Chaos 🍂 
*from **Adventure in Python** by Sergey Samoylov*

---

The terminal shimmered. The Companion tilted its head:

> — You’ve seen arguments passed in a line,  
> but now… what if they arrive in a *cloud of names*?

The air before the hero filled with names and values.  
No order. No number. Just... key and meaning.

---

### 📚 Topic: `**kwargs` — keyword arguments as a dictionary

Use `**kwargs` when a function needs to accept  
a **variable number of named** arguments.

They’re collected into a **dictionary**.

---

### 🔧 Example:

```python
def show_info(**kwargs: str) -> None:
    """Prints all keyword arguments"""
    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

Call like this:

```python
show_info(name="Zeta", role="Mentor", level="9")
```

Output:

```
name: Zeta  
role: Mentor  
level: 9
```

---

### ⚙️ You can combine `*args` and `**kwargs`:

```python
def full_log(*args: str, **kwargs: str) -> None:
    """Logs all messages and key-values"""
    for item in args:
        print(f"Log: {item}")
    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

---

### 🧪 Challenge: Build your hero

Write a function `describe_hero()`  
that accepts keyword arguments and  
returns a string describing the hero.

Example:

```python
describe_hero(name="Nyx", power="Invisibility")
```

Should return:

```
"Nyx has power: Invisibility"
```

You can add more keys and include them into the output.

---

This chaos of names... it’s not chaos at all.  
It’s flexibility. It's freedom.  
It’s your next tool in the journey.

[Chapter 35](Chapter_35.md)
