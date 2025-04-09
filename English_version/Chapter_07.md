## 📖 Chapter 7: Match and the Maze 🧩
*from Adventure in Python by Sergey Samoylov*

---

He walked.

The hallway split.  
Left? Right? Up? Loop?

Every path looked the same —  
until he realized something new:

A way to **match patterns**,  
a way to simplify **choices**.

No more tangled `if` nests.  
Just clean, clear **match-case**.

It felt... elegant.

Python whispered:  
> Use `match`, and read the world as it is.

---

## 💡 Module 7: Pattern Matching with `match`

---

> 🎯 Goal: use `match-case` to organize many options

---

### 🔹 Basic match

```python
def respond_to_command(command: str) -> None:
    """
    Reacts to a system command using match-case.
    """
    match command:
        case "status":
            print("System stable.")
        case "reboot":
            print("Rebooting...")
        case "shutdown":
            print("Shutting down.")
        case _:
            print(f"Unknown command: {command}")


respond_to_command("status")
```

---

### 🔹 Numeric matching

```python
def difficulty_message(level: int) -> None:
    """
    Prints a message based on difficulty level.
    """
    match level:
        case 1:
            print("Easy: Practice mode.")
        case 2:
            print("Medium: Prepare yourself.")
        case 3:
            print("Hard: Danger ahead.")
        case _:
            print(f"No such level: {level}")


difficulty_message(2)
```

---

### 🔹 Mini Quest: The Maze

```python
def maze_game() -> None:
    """
    Simulates a short maze using match-case.
    """
    print("You enter the Data Maze.")
    for move_count in range(3):
        choice: str = input("Move? (left/right/forward): ")

        match choice:
            case "left":
                print("A wall of code blocks your way.")
            case "right":
                print("You step onto a bridge of loops.")
            case "forward":
                print("You advance deeper into memory.")
            case _:
                print(f"{choice}? No such direction.")

    print("The maze resets. Try again?")


maze_game()
```

---

## 🧠 Mission: Build Your Maze

Create your own multi-step digital maze:
- Use `match-case` to handle user moves
- Include at least 4 directions
- Add a secret exit only if user types it exactly
- Limit steps with a counter

Let the player explore. Let the system respond.

---

> With `match`, your code reads **clean**.  
> Your logic becomes **poetry**.  
> And your world becomes **modular and wise**.

---

Coming up:  
[**Chapter 8: Memory and Objects**](Chapter_08.md) —  
The protagonist learns to persist not just data,  
but entire **entities** in the system.
