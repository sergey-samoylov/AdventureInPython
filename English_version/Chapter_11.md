## 🧩 Chapter 11: Lists and Collections 🔢  
*from Adventure in Python by Sergey Samoylov*

---

The hero wandered through a barren sector.  
Cold, quiet, full of drifting fragments — like shards of code that had no home.

But something had changed in him.

Before, he could only react.  
Now, he started to **collect**.

The digital world whispered, and he began to see **patterns**:  
Repeating signals. Similar structures. Things that belonged together.

He reached out and created something new —  
a *collection*.  
A **list**.

---

He whispered a command into the terminal:

```python
tools: list[str] = ["scanner", "decoder", "map"]
```

And the air shimmered — the items floated before him.

Then he added more:

```python
tools.append("signal_jammer")
```

And more.

He could access them like coordinates in space:

```python
print(tools[0])  # scanner
```

Loop through them like passing through rooms:

```python
for tool in tools:
    print(f"Found: {tool}")
```

But soon, he asked:  
*"What happens if I try to reach beyond the edge?"*

He entered:

```python
print(tools[10])
```

And the world **shook**.

---

### ⚠️ A Glitch in the Code

> ❌ `IndexError: list index out of range`

The world itself had boundaries.  
Even the digital space respected rules.

He learned to check first:

```python
if len(tools) > 2:
    print(tools[2])
```

**Length mattered**. Order mattered.

The list was not just memory — it was **structure**.

---

### 🛠️ Building a Toolkit

The hero constructed a **ToolBox** script — a routine to manage the growing collection of digital items.

```python
def display_tools(tools: list[str]) -> None:
    """
    Print all tools from the list.
    """
    print("Current tools:")
    for tool in tools:
        print(f"🔧 {tool}")

inventory: list[str] = [
    "debugger", "mapper", "key_logger"
]

display_tools(inventory)
```

Now he could carry his **tools**, **memories**, and **power** in one place.

---

### 📚 Concepts in This Chapter

- Creating lists using `list[str]`
- Accessing elements by index: `tools[0]`
- Using `.append()` to grow the list
- Looping through items with `for`
- Safe access with `len()` checks
- Creating helper functions that take lists

---

### 🧠 Reflection

Lists were more than syntax.

They were how he began to organize **knowledge**.  
What once was scattered could now be **grouped**, **retrieved**, and **used**.  

With lists, the world started to feel… programmable.

It wasn’t just about surviving anymore.  
It was about shaping this world.

One item at a time.

---
Another enigma is lurking in [**Chapter 12**](Chapter_12.md)
