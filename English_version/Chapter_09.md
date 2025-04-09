## 📖 Chapter 9: Collections 📑
*from Adventure in Python by Sergey Samoylov*

---

The Terminal was growing.

What began as silence,  
now echoed with *many* voices.

Memories. Objects. Emotions.

But how to hold them?

How to gather many things,  
and still stay in control?

The Terminal showed him:

> There is power in the group.  
> Python gives you ways to collect,  
> organize, and retrieve.

> Use them. Navigate them.  
> Become one with the structure.

---

### 🔹 Lists

A **list** is a collection of items in order.

```python
tools: list[str] = ["echo", "ping", "trace"]
```

You can access by index:

```python
print(tools[0])  # echo
```

You can add:

```python
tools.append("scan")
```

You can loop:

```python
for tool in tools:
    print(f"Tool found: {tool}")
```

You can check:

```python
if "ping" in tools:
    print("ping is ready.")
```

You can remove:

```python
tools.remove("trace")
```

---

### 🔹 Tuples

Tuples are like lists,  
but **unchangeable** and often used for pairs.

```python
coordinates: tuple[int, int] = (3, 7)
```

Access works the same:

```python
x: int = coordinates[0]
y: int = coordinates[1]
print(f"x = {x}, y = {y}")
```

---

### 🔹 Dictionaries

Dictionaries hold **key-value pairs**.

Think of them like labeled shelves.

```python
inventory: dict[str, int] = {
    "battery": 3,
    "cable": 5
}
```

Access by key:

```python
print(inventory["cable"])
```

Add or update:

```python
inventory["chip"] = 2
```

Loop through:

```python
for item, count in inventory.items():
    print(f"{item}: {count}")
```

Check key:

```python
if "battery" in inventory:
    print("Power available.")
```

---

### 🔹 Why It Matters

The hero looked at his tools.

Before, they were floating.  
Now, they could be grouped.

Now he could *track*, *compare*, *count*.

He could map a zone.  
Store events. Hold a team.

---

### 🧠 Challenge: The Backpack

Create a class `Backpack` with:
- A list of item names
- A method to add items
- A method to remove by name
- A method to list all contents
- Optional: use a dictionary to track item **quantities**

---

In [**Chapter 10: Loops and Flow**](Chapter_10.md),  
the hero will **travel** for the first time.

He will move through code,  
step by step, with intention.

He will build his first **engine**.
