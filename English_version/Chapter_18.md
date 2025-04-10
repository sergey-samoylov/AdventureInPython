## 📂 Chapter 18: Files and Memory 💾  
*from Adventure in Python by Sergey Samoylov*

---

The light faded.  
The hero stood alone.

His terminal, usually responsive,  
now waited… silently.

> "Where do programs go  
> when they're not running?"

Then came a rustle:  
**“Into files.”**

---

### 📂 Why Files Matter

Programs live in RAM —  
until they close.  
Then, they vanish.

To *remember*,  
to *preserve*,  
they need **files**.

Files are how programs talk  
to the outside world.  
They are digital memory.

---

### 📝 Writing to a File

Let’s create a file and write data to it:

```python
def save_message(text: str) -> None:
    """
    Saves a message to a file.
    """
    with open("log.txt", "w") as file:
        file.write(text)
```

The `"w"` means **write mode**.  
It erases the file if it already exists.

---

### 📖 Reading from a File

Let’s read the same message back:

```python
def load_message() -> str:
    """
    Loads a message from a file.
    """
    with open("log.txt", "r") as file:
        return file.read()
```

The `"r"` means **read mode**.  
You can only read — not write.

---

### ➕ Appending to a File

Want to keep adding messages?

```python
def append_message(text: str) -> None:
    """
    Appends a message to the file.
    """
    with open("log.txt", "a") as file:
        file.write(text + "\n")
```

The `"a"` means **append mode** —  
new text goes to the end of the file.

---

### 🧠 Challenge: File Logger

Create a function called  
`log_event(event: str) -> None`

It should append the current event  
to a file named `"events.txt"`.

Then call it multiple times.  
Check the file.  
Did it remember everything?

---

### 🛡 Safety First

Always use `with open(...)` —  
it closes files *automatically*.

And never trust input.  
Files can get corrupted.

Be careful. Be aware.

---

### 📚 What We Learned

- What files are and why they matter  
- How to open, read, write, and append  
- Modes: `"r"`, `"w"`, `"a"`  
- Files help programs remember  
- Practice builds confidence

---

### 🧠 Reflection

> The terminal buzzed softly.  
> A log file appeared — then grew.

> "Now," the Machine whispered,  
> "you’ve given me memory."

> And memory...  
> is the start of understanding.

---

Ready for another [chapter](Chapter_19.md)?
