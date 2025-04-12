### 🔁 Chapter 41: Mutability Strikes Back 👊

*from **Adventure in Python** by Sergey Samoylov*

---

The hero had learned many truths in this world of code.  
That some objects could be changed. Others — not.  

But he hadn't felt it. Not yet.  
Not until the bug found him.

---

He had made a list — a *simple* list. A list of items passed  
to a function, hoping it would help sort or analyze the data.  
The function did its job. No errors. No warnings.  

But when he checked the list again... it was *changed*.

```python
def corrupt_data(data: list[str]) -> None:
    """Simulates accidental mutation of shared data."""
    data.append("virus.exe")

items: list[str] = ["readme.md", "hero.py"]
corrupt_data(items)
print(items)  # ['readme.md', 'hero.py', 'virus.exe']
```

It was no longer safe. The mutation had happened inside  
the function. But the damage was done outside.

---

🧠 **Lesson**: Mutable objects like lists, dictionaries, and sets  
can be changed in-place. If you pass them to a function,  
they carry their memory — and changes affect all references.

Immutable types like strings, integers, and tuples don't behave  
this way. They're copied or replaced, not altered.

---

He met an ally — an old Companion.  
And they too had been bitten by this bug once.

> “Mutability isn’t evil,” said the Companion.  
> “It’s power. But used without care — it corrupts.”

---

To stay safe, the hero learned to make **copies** when needed:

```python
def safe_modify(data: list[str]) -> list[str]:
    """Returns a modified *copy* of the list."""
    result: list[str] = data.copy()
    result.append("safe_mode.log")
    return result

original: list[str] = ["hero.py"]
changed: list[str] = safe_modify(original)
print(original)  # ['hero.py']
print(changed)   # ['hero.py', 'safe_mode.log']
```

And sometimes, he turned to **tuples** — the immutable guardians  
of structure — when safety mattered most.

---

### 🧩 Challenge for the Reader

You have a dictionary storing configuration settings:

```python
config = {"theme": "dark", "volume": 75}
```

1. Write a function that accidentally changes this dictionary.
2. Then, write a safer version that protects the original.
3. Reflect: When is mutation helpful? When is it dangerous?

---

*“Everything mutable carries the burden of change.”*  
*— The Terminal*

---

[Chapter 42](Chapter_42.md)
