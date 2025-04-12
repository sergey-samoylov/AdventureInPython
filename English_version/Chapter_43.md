### 🛡️ Chapter 43: Guarding Secrets — Privacy and Conventions 👛
*from **Adventure in Python** by Sergey Samoylov*

---

The hero found a hidden chamber in the code.  
Inside, variables were marked with a strange symbol — a single underscore.

```python
class Core:
    def __init__(self) -> None:
        self._power_level = 9000
```

"What’s this?" he whispered.

---

🕵️ **Python’s Secret Code**

Unlike other languages, Python doesn’t have true *private* variables.  
Instead, it uses **conventions** to *suggest* that a name is private:

- `_name`: Internal use only. Please don’t touch.
- `__name`: Name mangling. Harder (but not impossible) to access.
- `__name__`: Special names used by Python itself (like `__init__`).

---

🔐 **Why Privacy Matters**

Imagine a magical crystal:

```python
class Crystal:
    def __init__(self) -> None:
        self._energy = 100

    def drain(self) -> None:
        self._energy -= 10
```

It works fine — until someone tampers with it:

```python
gem = Crystal()
gem._energy = -9999  # Whoops!
```

Privacy protects objects from misuse and bugs.

---

🎭 **Name Mangling Example**

```python
class Vault:
    def __init__(self) -> None:
        self.__code = "42"

safe = Vault()
print(safe.__code)  # AttributeError!
print(safe._Vault__code)  # '42'
```

Name mangling doesn’t make it private,  
but hides it from casual access.

---

> "We trust the reader," said the Terminal.  
> "But we leave signs: here be dragons."

---

### 🧩 Challenge for the Reader

1. Create a class with a “secret” attribute.
2. Use `_` and `__` to mark different levels of privacy.
3. Try accessing these attributes from outside the class. What happens?
4. Bonus: Think of a real-world reason to *hide* data in a class.

---

*"To guard your code is to guard your story."*  
— Terminal

---

[Chapter 44](Chapter_44.md)
