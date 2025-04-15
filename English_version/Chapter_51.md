Let’s bring our Hero back to the physical world of data —  
where paths hide secrets and files tell stories…

---

### 📁 Chapter 51: Files and Paths — The Scrolls of the System

The digital wind carried whispers…

Something was hidden.  
Not in memory. Not in code.  
But in files, scattered across the System’s dark corridors.

Our Hero stumbled upon a glowing directory — `/home/hero/journey/`.  
Inside it, ancient scrolls.  
`.txt`, `.log`, `.dat` — all waiting to be read.

---

### 🧪 Learning: Working with Files in Python

Python can open, read, write, and manage files — just like a digital librarian.

#### 🔓 Opening a file
```python
with open("scroll.txt", "r") as file:
    text = file.read()
    print(text)
```

- `"r"` — read mode.
- The `with` block auto-closes the file.
- `file.read()` returns the whole content as a string.

#### 📝 Writing to a file
```python
with open("journal.txt", "w") as file:
    file.write("The Hero has entered the Archive.")
```

- `"w"` — write mode. Be careful: it overwrites the file!
- Use `"a"` (append mode) to add new lines instead.

#### 🔁 Reading line by line
```python
with open("scroll.txt") as file:
    for line in file:
        print(line.strip())
```

Great for logs, lists, or secrets written line by line.

---

### 🧭 Paths: Navigating the System

Python’s `pathlib` module makes dealing with paths *elegant and safe*.

```python
from pathlib import Path

home = Path("/home/hero")
scroll = home / "journey" / "scroll.txt"

if scroll.exists():
    print("Scroll found:", scroll.name)
```

- `/` is overloaded here to join paths.
- `.exists()` checks if the file is really there.
- `.name`, `.suffix`, `.parent`, `.stem` give useful info.

---

### 🧠 The Hero’s Insight

_"Not all knowledge is coded in logic.  
Some is written… hidden… stored by the elders."_

Files carry messages.  
Logs carry traces.  
Paths lead to artifacts.

Our Hero knew — to decode this world, they needed to **read between the lines**.

---

### 🎯 Your Challenge

1. Create a file named `inventory.txt` and write three items inside.
2. Read it line by line and print: `"You carry: <item>"`
3. Modify your code to:
   - Skip empty lines
   - Capitalize each item

> ✨ Bonus: Try using `Path.home()` and create your file inside a custom folder.

---

Ready for a secret tip?  
In [Chapter 52](Chapter_52), our Hero realizes: every step so far… has been training.

Shall we [continue](Chapter_52)?
