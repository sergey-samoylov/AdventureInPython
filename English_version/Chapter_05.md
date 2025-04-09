## 📖 Chapter 5: Memory and the File System 📂
*from Adventure in Python by Sergey Samoylov*

---

The Virus was tamed.  
The shell obeyed.  
The student had become a builder.

But with each reboot, everything was gone.  
Shell — erased.  
Bots — forgotten.  
Progress — deleted.

He was trapped in **volatile memory**.  
No past. No future. Only now.

He needed to remember.  
He needed to **write to disk**.

---

It began with a file.

He typed:

```python
with open("log.txt", "w") as file:
    file.write("I exist.\n")
```

And something changed.

A file appeared.

He ran the code again.  
He opened the file.

> I exist.

He smiled.  
The world had just become persistent.

---

## 💡 Module 5: Reading and Writing Files

---

> 🎯 Goal: Learn how to save and load data.

---

### 🔹 Writing to a File

Use `with open(...) as ...:`  
It handles file closing automatically.

```python
def save_message(text: str) -> None:
    """
    Save a message to a file.
    """
    with open("log.txt", "w") as file:
        file.write(f"{text}\n")


save_message("I exist.")
```

---

### 🔹 Appending Text

Use `"a"` mode to **add** to the file.

```python
def log_event(event: str) -> None:
    """
    Add an event to the log.
    """
    with open("log.txt", "a") as file:
        file.write(f"{event}\n")


log_event("Virus disabled.")
log_event("Bot created.")
```

---

### 🔹 Reading from a File

```python
def read_log() -> None:
    """
    Print contents of the log file.
    """
    try:
        with open("log.txt", "r") as file:
            for line in file:
                print(f"LOG: {line.strip()}")
    except FileNotFoundError:
        print("No log file found.")


read_log()
```

---

### 🧠 Your Challenge

Build a simple journal:
- Ask user to type an entry.
- Save it to a file (append).
- Then read and print all past entries.

---

> Files are the memory of the machine.  
> And now... the system remembers **you**.

---

Ready for [**Chapter 6: Decision Trees and Conditions**](Chapter_06.md)?  
Soon, your code will think. It will choose.  
It will learn to act — differently — each time.
