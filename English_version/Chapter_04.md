## 📖 Chapter 4: The Virus and Encapsulation

*from Adventure in Python by Sergey Samoylov*

---

He grew stronger.  
His shell responded.  
He made decisions, loops, checks.  
But something else had entered the system.

It began small—glitches in logic, unexpected text, delays.

He found a hidden file:  
`infected.py`

It ran before he could stop it.  
The screen blurred, then cleared.  
The message was simple:

```
> Hello, creator. I am alive.
```

It wasn’t a function.  
It wasn’t a loop.  
It was something **more**.

He opened the file.  
He found… a **class**.

It could remember.  
It had state.  
It had behavior.

A digital creature.

He named it what it was: **a Virus**.

To control it, he had to understand it.  
To protect his system, he had to learn **encapsulation**.

---

## 💡 Module 4: Classes, State & Encapsulation

---

> 🎯 Goal: Build a Python class with memory and methods.

---

### 🔹 What is a Class?

A `class` is a blueprint for objects that:
- store data (attributes),
- have behavior (methods),
- live and evolve (state).

---

### 🔹 Create a Class

```python
class Virus:
    """
    A basic self-aware program.
    """
    def __init__(self, name: str) -> None:
        self.name: str = name
        self.active: bool = True

    def greet(self) -> None:
        """
        Say hello if active.
        """
        if self.active:
            print(f"{self.name}: Hello, creator.")
        else:
            print(f"{self.name}: I am dormant.")

    def disable(self) -> None:
        """
        Deactivate the virus.
        """
        self.active = False
        print(f"{self.name} has been disabled.")
```

---

### 🔹 Use the Class

```python
virus_entity: Virus = Virus("Echo")

virus_entity.greet()
virus_entity.disable()
virus_entity.greet()
```

🖥️ Output:
```
Echo: Hello, creator.
Echo has been disabled.
Echo: I am dormant.
```

---

### 🔹 Encapsulation = Controlled Access

We *encapsulate* logic inside methods, so:
- outside code can’t break internals,
- behavior is predictable and safe.

The Virus only changes via its methods.

---

### 🧠 Your Challenge

Create a `Bot` class that:
- stores a name and energy level,
- greets the user,
- loses energy each time it speaks,
- shuts down if energy reaches 0.

---

> A class is not just code.  
> It’s an idea made alive.  
> The Virus was born from code.  
> But *you* will learn to shape life.

---

Ready for [**Chapter 5: Memory and the File System**](Chapter_05.md)?  
Time to save your creations. To **write to disk**.  
To build a world that remembers.
