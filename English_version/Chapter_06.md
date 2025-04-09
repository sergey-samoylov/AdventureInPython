## 📖 Chapter 6: Decisions and Branching  
*from Adventure in Python by Sergey Samoylov*

---

The system remembered.  
The scripts ran.  
The bots obeyed.  
The virus slept.

But something was wrong.  
Everything was the same.

Every launch — identical lines.  
Every outcome — predictable.

He realized:  
The world **reacts**.  
His code should too.

He must **make choices**.

> [Why "IF... ELSE..." explained here"](why_if.md)?

---

## 💡 Module 6: If, Elif, Else — Thinking Code

---

> 🎯 Goal: control logic flow using conditional branching

---

### 🔹 if / elif / else

```python
def analyze_temperature(temperature: int) -> None:
    """
    Analyze the temperature and react accordingly.
    """
    if temperature > 30:
        print(f"{temperature}°C — Too hot!")
    elif temperature > 10:
        print(f"{temperature}°C — Comfortable.")
    else:
        print(f"{temperature}°C — Cold.")


analyze_temperature(25)
```

---

### 🔹 Nested conditions

```python
def system_check(cpu_temp: int, disk_full: bool) -> None:
    """
    Check the system’s health and report status.
    """
    if cpu_temp > 70:
        print("⚠ CPU Overheating!")
        if disk_full:
            print("💾 Disk is full as well.")
    else:
        print("✅ System is stable.")


system_check(75, True)
```

---

### 🔹 Decisions from input

```python
def choose_path() -> None:
    """
    Prompt the user to choose a direction.
    """
    print("You stand at a digital crossroads.")
    direction: str = input("Where to? (left/right): ")

    if direction == "left":
        print("You enter the log archive.")
    elif direction == "right":
        print("You move toward the memory core.")
    else:
        print("Unknown path. You remain in place.")


choose_path()
```

---

## 🧠 Mission: Digital Hallways

Create a game called "Digital Hallway":
- The user chooses: forward / back / left / right.
- Each choice produces a unique result.
- After 3 moves, the game ends.

Use:
- `if/elif/else` for decisions
- `input()` for choices
- loops and counters to limit turns

---

> Conditionals give your code **a mind**.  
> Now your logic doesn’t just **run** —  
> it **decides**.

---

Ready for [**Chapter 7: Match and the Maze**](Chapter_07.md)?  
We’ll go deeper into branching logic —  
and build your first **interactive quest**.
