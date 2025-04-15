### 🧱 Chapter 53: Enter the Class (with Docstrings)

The Hero stepped through the shimmering doorway.

Before him stretched a vast new domain — where **blueprints shaped reality**, and logic wore the robes of identity.

A glowing sigil pulsed with power:

```python
class Hero:
    """A brave hero with a name and a level in the future :-)."""
    pass
```

At first glance, it looked like a mere structure.  
But it held something more — the power to create **your own kind of value**.

---

### 🧬 What Is a Class?

A **class** is a blueprint for creating **objects**.  
It lets you define your **own data types**, just like `str`, `int`, or `list`.

You decide:
- What data the object should carry (attributes)
- What it can do (methods)

> A class is not a thing — it's a *recipe* for making things.

---

### 🔨 Creating a Class and an Object

Let’s build a `Hero` of our own:

```python
class Hero:
    """A class representing a hero with a name and a level."""

    def __init__(self, name: str, level: int):
        """Initialize a new Hero with a name and level."""
        self.name = name
        self.level = level

    def speak(self) -> None:
        """Make the hero speak their name and level."""
        print(f"I am {self.name}, level {self.level}!")
```

This is how we **use** the class — by creating an *instance* of it:

```python
knight = Hero("Galahad", 3)
knight.speak()
# Output: I am Galahad, level 3!
```

---

### 🧩 Let’s break it down

- `class Hero`: defines a new blueprint called `Hero`.
- `__init__`: this special method runs **when you initialize(create)** an object.
- `self`: refers to the *specific instance* being created.
- `self.name`, `self.level`: these are **attributes** that store data.
- `speak`: a method, a function **inside** the class.

---

### 🔁 You can create as many heroes as you like

```python
rogue = Hero("Nyx", 5)
rogue.speak()
```

Each object is unique, based on the same class.

---

### 🧠 Why Classes?

Think of classes like tools for:
- Grouping related data and behavior
- Creating organized, reusable structures
- Managing complexity in large programs

---

### 🎯 Your Turn: Challenge

Write a class `Spell`, with:

- An `__init__()` method that takes `name: str` and `power: int`
- A method `cast()` that prints something like:
  ```
  Casting Fireball! (Power: 50)
  ```

With **docstrings**:

```python
class Spell:
    """A magical spell with a name and power."""

    def __init__(self, name: str, power: int):
        """Initialize a spell with its name and power level."""
        self.name = name
        self.power = power

    def cast(self) -> None:
        """Cast the spell and display its effect."""
        print(f"Casting {self.name}! (Power: {self.power})")
```

Now try:

```python
fireball = Spell("Fireball", 50)
fireball.cast()
```

---

Next stop: 🧙‍♂️ **[Chapter 54](Chapter_53.md): Object Magic — Understanding `self`**

Ready to continue?
