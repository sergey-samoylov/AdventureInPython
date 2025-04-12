### 🧬 Chapter 39: Mutability — The Power to Change  
*from **Adventure in Python** by Sergey Samoylov*

---

The air shimmered.  
The Companion raised a curious object.

It looked like a coin…  
but when he touched it — it turned into a blade.

> "Not everything in Python stays the same,"  
> the Companion said.  
> "Some things... can be changed."

---

### 🔁 Mutable vs Immutable

In Python, **data** comes in two kinds:

- **Immutable** — cannot be changed in place  
- **Mutable** — can be changed after creation

---

### 🧊 Immutable examples

- `int`
- `float`
- `bool`
- `str`
- `tuple`

You cannot change these once they’re made.

```python
name = "Ada"
name[0] = "E"  # ❌ Error!
```

Changing a string means creating a new one:

```python
name = "Ada"
new_name = "E" + name[1:]
```

---

### 🧪 Mutable examples

- `list`
- `dict`
- `set`
- custom classes (usually)

These can be changed in place:

```python
inventory = ["key", "map"]
inventory.append("torch")
```

No need to create a new list — the same object changes.

---

### 🧭 How to check mutability?

Ask yourself:

- Does it support `.append()`, `.remove()`, `.update()`?
- Can I change it without making a new one?

Or use `id()` to track identity:

```python
items = [1, 2]
print(id(items))  # Some number

items.append(3)
print(id(items))  # Same number
```

Immutable values get a new ID when changed.

---

### 🧠 Why does it matter?

Mutability changes how your program behaves.

Example:

```python
def add_item(bag: list, item: str) -> None:
    bag.append(item)

player_bag = ["potion"]
add_item(player_bag, "elixir")

print(player_bag)  # ['potion', 'elixir']
```

The original list is changed!

---

### ⚔️ The hero’s revelation

The blade in the hero’s hand twisted again —  
this time into a mirror.

He saw himself in it.

> "I, too, am mutable…  
> My thoughts. My skills.  
> That’s how I grow."

---

### 🧪 Task: Test for mutability

Write a function `test_identity_change()`  
that takes a variable, modifies it if possible,  
and prints whether its `id()` changed.

Try it with:

- a string  
- a list  
- a dictionary

What did you learn?

---

The path forward shimmers.  
Will you change it — or will it change you?

[Chapter 40](Chapter_40.md)
