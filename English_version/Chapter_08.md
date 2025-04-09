## 📖 Chapter 8: Memory and Objects 🧠
*from Adventure in Python by Sergey Samoylov*

---

He stood still.

Everything was fading.

The hallway. The sounds. Even time.

He needed to **remember**.  
To keep something from vanishing.

And he already knew how.

Back in the early days, he’d built structures.  
Classes. Data-holders.

But now, it was different.

He no longer needed a container.  
He needed a **mind**.

Something that could **remember**, **change**, and **feel**.

Python whispered:

> You’ve built classes before.  
> Now build them with meaning.

> Give them *behavior*.  
> Let them *respond*.

And the hero began.

---

### 🔹 A Class for Memory

```python
class Memory:
    """
    A simple memory container that stores a string value.
    """

    def __init__(self, value: str) -> None:
        self.value: str = value

    def recall(self) -> str:
        """
        Returns the stored memory value.
        """
        return f"Memory says: {self.value}"
```

```python
core_memory: Memory = Memory("I exist.")
print(core_memory.recall())
```

---

### 🔹 Giving Memory Behavior

```python
class Memory:
    """
    Memory that can be recalled, cleared, or rewritten.
    """

    def __init__(self, value: str) -> None:
        self.value: str = value

    def recall(self) -> str:
        """
        Returns the memory if it exists.
        """
        return f"Memory says: {self.value}"

    def erase(self) -> None:
        """
        Clears the memory value.
        """
        self.value = ""

    def rewrite(self, new_value: str) -> None:
        """
        Updates the memory with a new string.
        """
        self.value = new_value
```

```python
memory_cell: Memory = Memory("System initialized.")
print(memory_cell.recall())

memory_cell.rewrite("Terminal is alive.")
print(memory_cell.recall())

memory_cell.erase()
print(memory_cell.recall())
```

---

### 🔹 The Companion

```python
class Companion:
    """
    Digital being that stores a name and mood.
    """

    def __init__(self, name: str) -> None:
        self.name: str = name
        self.mood: str = "neutral"

    def greet(self) -> None:
        """
        Prints a greeting message based on mood.
        """
        print(f"{self.name} says hello. Mood: {self.mood}")

    def cheer_up(self) -> None:
        """
        Changes mood to happy.
        """
        self.mood = "happy"
```

```python
bot: Companion = Companion("Echo")
bot.greet()

bot.cheer_up()
bot.greet()
```

---

### 🔹 Optional: Make It Printable with `__repr__()`

Sometimes you want your object to show something  
useful when printed or logged. A **repr**esentation.

Python uses the method `__repr__()` for this.

```python
class Companion:
    """
    Digital being that stores a name and mood.
    """

    def __init__(self, name: str) -> None:
        self.name: str = name
        self.mood: str = "neutral"

    def __repr__(self) -> str:
        """
        Returns a debug-friendly string about the object.
        """
        return f"<Companion name={self.name} mood={self.mood}>"
```

```python
bot: Companion = Companion("Echo")
print(bot)
```

This will output:

```
<Companion name=Echo mood=neutral>
```

A good `__repr__()` helps you debug and understand your code.  
You’ll see it more as you build larger systems.

---

### 🧠 Challenge: Object Builder

Create your own object:
- Give it **at least two attributes**
- Write **three methods** to interact with those attributes
- Add an optional `__repr__()` method to describe the object

You're not just writing code anymore.  
You're modeling behavior.

Soon, these objects will form networks.  
They’ll hold data, pass messages, evolve.

---

Ready to continue to [**Chapter 9: Collections**](Chapter_09.md)?

There, the hero will learn how to gather —  
how to hold **many things at once** —  
and navigate the **maps and lists**  
that structure the digital world.
