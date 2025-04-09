## 📖 Chapter 2: A Shell of a Home 🏡

*from Adventure in Python by Sergey Samoylov*

---

The black void began to feel colder.

He could speak to the system—but the system didn’t speak back.  
Not yet.

He stared into the blinking prompt, wondering:  
> “What if the system could ask me something?”  
> “What if I could respond?”

And so, he typed:

```python
name: str = input("What is your name? ")
print("Hello, {name}")
```

The void pulsed.  
The question appeared.  
He typed: `Alex`.

```
Hello, Alex
```

The terminal responded.  
It asked. He answered.

He grinned. For the first time, he wasn’t just observing.  
He was *building*.

---

He decided to build a shell, a home—not made of walls and windows, but logic and choices. A digital structure to survive in.

He needed the system to behave *differently* depending on input.  
That meant: **conditions**.

He wrote:

```python
if name == "Alex":
    print("Welcome back, Operator.")
else:
    print("Access restricted.")
```

The code *listened*, *decided*, *reacted*.

It wasn’t much, but it was *his*.

The first bricks of his home had been placed—inside a shell, running on logic and will.

---

## 💡 Python Module 2: Making Decisions — Input & Logic

---

> 🛠️ Goal: Build a basic interactive script with conditions.

---

### 🔹 `input()` — Hear the Void

`input()` lets you ask questions. It pauses, waits, and returns what the user types.

```python
name: str = input("Who are you? ")
print(f"Hello,{name}")
```

All values from `input()` are strings by default.

---

### 🔹 `if`, `else`, `elif` — Choose Your Path

Python makes decisions with these keywords:

```python
code: str = input("Enter access code: ")

if code == "42":
    print("Access granted")
elif code == "admin":
    print("Admin access enabled")
else:
    print("Access denied")
```

---

### 🔹 `def` — Define Your Own Commands

Use `def` to group logic into reusable blocks: functions.

```python
def greet(name: str) -> None:
    """
    Greets the user by name.
    """
    print(f"Welcome, {name}")


username: str = input("Enter your name: ")
greet(username)
```

---

### 🧠 Challenge

Create an interactive script that:
1. Asks the user for their name and code.
2. Grants or denies access based on the code.
3. Greets them if access is granted.

Example output:

```
Name: Neo
Code: 1337
Welcome, Neo.
Access level: Hacker.
```

---

🧱 You are now building foundations:
- Input: to listen.
- Conditions: to choose.
- Functions: to shape.

You have a voice *and* a brain.  
Next, you'll [meet your first enemy: a bug](Chapter_03.md).

---
