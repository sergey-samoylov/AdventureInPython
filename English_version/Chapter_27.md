### 🧰 Chapter 27: *args and **kwargs — The Language of Flexibility 🗣️*
*from **Adventure in Python** by Sergey Samoylov*

---

The hero now spoke Python fluently.  
But one day, in the valley of the Silent Functions,  
a new kind of construct appeared — too quiet, too open-ended.

He asked the Companion, "How do I talk to them?"

The Companion smiled and answered:

> “Use the language of many — `*args` and `**kwargs`.”  

---

### 🧰 Topic: *args and **kwargs

Sometimes we want our functions to accept **any number** of arguments.

- `*args` gathers **positional** arguments into a tuple.
- `**kwargs` gathers **keyword** arguments into a dictionary.

```python
def speak(*words: str) -> None:
    """Prints each word provided."""
    for word in words:
        print(word)

speak("I", "am", "learning", "Python")
```

This prints each word on a new line.

```python
def describe(**info: str) -> None:
    """Prints info from keyword arguments."""
    for key, value in info.items():
        print(f"{key}: {value}")

describe(name="Companion", role="AI", version="1.0")
```

---

### 🤝 Why Use Them?

- When you don’t know how many arguments you'll get.
- To create flexible APIs or callbacks.
- When passing arguments from one function to another.

They’re Python’s way of saying: “Bring what you’ve got.”

---

### 🧪 Task: Greet Everyone

Write a function `greet_all()`  
that accepts any number of names using `*args`.

It should print:

```
Hello, Alice!
Hello, Bob!
Hello, Eve!
```

If you run:

```python
greet_all("Alice", "Bob", "Eve")
```

---

[Chapter 28](Chapter_28.md)
