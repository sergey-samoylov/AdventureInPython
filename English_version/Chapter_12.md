## 🗂️ Chapter 12: Dictionaries and Meaning 🔍  
*from Adventure in Python by Sergey Samoylov*

---

The deeper he went,  
the more the world resembled a mind — not just a machine.

There were symbols.  
And behind each symbol: **meaning**.

The hero began to understand that *lists* were only the beginning.  
They were good for order,  
but not for **associations**.

He needed something smarter.  
Something that connected **one thing to another**.

A word to its definition.  
A command to its effect.  
A name to a value.

He discovered: **the dictionary**.

---

### 📜 The First Map

```python
terminal_commands: dict[str, str] = {
    "scan": "Detect nearby activity",
    "map": "Visualize terrain",
    "hack": "Bypass firewalls"
}
```

Each key was like a **label**,  
each value — its **function**.

```python
print(terminal_commands["scan"])
```

> Detect nearby activity

It was simple. Powerful.  
He could look up meaning in a single step.

---

But what if he asked for something that didn’t exist?

```python
print(terminal_commands["launch"])
```

> ❌ `KeyError`

The world shuddered again.

He adjusted, and learned to check first:

```python
if "launch" in terminal_commands:
    print(terminal_commands["launch"])
else:
    print("Unknown command")
```

Now he could read the map —  
but also navigate it safely.

---

### 🧠 Data with Meaning

He realized: dictionaries were more than containers.  
They were **models of knowledge**.

Lists stored things.  
Dictionaries **explained** them.

And he could go further.

---

### 🛠️ Practice: Describe Your Toolkit

```python
def describe_tools(tools: dict[str, str]) -> None:
    """
    Print each tool with its description.
    """
    print("Tools and their functions:")
    for name, function in tools.items():
        print(f"{name.title()}: {function}")

inventory: dict[str, str] = {
    "scanner": "Reads nearby code activity",
    "jammer": "Disrupts hostile packets",
    "decoder": "Cracks message formats"
}

describe_tools(inventory)
```

Now each item had **a name** *and* a **meaning**.

And the hero’s power grew.

---

### 📚 Concepts in This Chapter

- `dict[str, str]` for mapping keys to values
- Accessing values with `[]`
- Checking keys with `if "key" in dict`
- Iterating with `.items()`
- Designing functions that process dictionaries

---

### 🧠 Reflection

The world whispered:  
*"Every key must have a lock.  
Every command must have a purpose."*

With dictionaries, the hero wasn't just storing data —  
he was creating a **semantic map** of the world.

Soon, he would write programs  
that didn't just react —  
they would *understand*.

---

Continue your adventure in [Chapter 13](Chapter_13.md).
