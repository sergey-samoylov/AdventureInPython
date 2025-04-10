## 💬 Chapter 13: Input and Dialogue 🎙️  
*from Adventure in Python by Sergey Samoylov*

---

The terminal pulsed.  
Something — *someone* — was trying to speak.

Until now, the hero had typed blindly,  
but the world had been silent.

Now… it asked a question.

```python
name = input("Identify yourself: ")
print(f"Welcome, {name}.")
```

For the first time, it felt like a **conversation**.

Why input() here? Good question. Check the [answer](why_input.md).

---

### 🔁 Programs That Listen

Before, programs only **spoke**.  
Now, they could **listen** and **respond**.

```python
tool = input("Which tool will you use? ")
print(f"{tool.title()} activated.")
```

Each command felt like a choice.  
Each input — a voice in the story.

The hero wasn’t just navigating the code.  
He was **interacting with it**.

---

### 🎭 Choose Your Role

The system had more to ask:

```python
role = input("Choose your path (hacker, mapper, scout): ")

if role == "hacker":
    print("Firewalls will fall before you.")
elif role == "mapper":
    print("You will reveal the hidden terrain.")
elif role == "scout":
    print("You’ll see what others miss.")
else:
    print("Unknown path. Proceed with caution.")
```

The hero realized:  
**input** made the code personal.  
Every run of the program became a different story.

---

### 🛠️ Practice: Terminal Registration

Write a program that:

1. Asks for the user’s codename  
2. Asks what skill they want to train (choose from 3)  
3. Responds with a personalized confirmation

Example:

```text
Codename: Neo
Skill to train: stealth
=> Training stealth, Neo. Stay hidden.
```

---

### 🎯 Challenge: Build a Welcome Console

Create an interactive terminal sequence that:

- Greets the user
- Asks three questions (your choice)
- Gives a summary of their “profile”

Try adding formatting with line breaks and spacing.  
Use `.title()` or `.upper()` for style!

---

### 📚 Concepts in This Chapter

- `input()` for reading user input
- Storing input in variables
- Using conditions to branch based on input
- Personalizing program output

---

### 🧠 Reflection

*"To command is one thing,"* the terminal whispered,  
*"But to ask… that opens doors."*

With input, the code was no longer a wall.  
It became a **dialogue** — a two-way channel.

And the world was ready to answer.

---

Rested a bit?

Now, let's explore [Chapter 14](Chapter_14.md)
