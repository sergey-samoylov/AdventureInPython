### 🧪 Chapter 44: Testing the Future — Writing Simple Tests

*from* **Adventure in Python** by Sergey Samoylov*

---

The terminal flickered. A new message appeared:

> "Before you go further… can you *prove* that your code works?"

The hero looked puzzled. “I ran it. It seemed fine.”

> "Seeming is not knowing."

---

🧭 **Why Testing Matters**

You don’t always know when something breaks.  
A simple change in one place might affect another.

That’s why we write **tests** — code that checks other code.

---

⚙️ **The Simplest Test: assert**

```python
def double(x: int) -> int:
    return x * 2

assert double(3) == 6
assert double(0) == 0
```

If the condition after `assert` is false, Python raises an error.

```python
assert double(-2) == -4  # ✅
assert double("A") == "AA"  # ✅, but surprising?
```

---

🛠️ **Catching the Unexpected**

The hero tried something unexpected:

```python
assert double([1, 2]) == [1, 2, 1, 2]
```

It passed!

> "Tests don’t just check for errors. They check for *intentions*."

---

📜 **Organizing Your Tests**

You can place all your tests in a separate file, like:

```
project/
│
├── main.py
└── test_main.py
```

Then run the test file and check what passes.

---

🧠 **What Does It Mean to “Test” Something?**

It means:

- You define what *should* happen.
- You make sure it *does* happen.
- You stay confident, even when changing code later.

> “A good adventurer doesn’t just fight… they *prepare*.”

---

### 🧩 Challenge for You

1. Write a small function (like `add`, `multiply`, or `reverse_string`).  
2. Add 3–5 `assert` statements to test different cases.  
3. Break the function on purpose — do your tests catch it?

---

Ready for more adventures?  
Let’s keep going! 😊

---

[Chapter 44](Chapter_44.md)
