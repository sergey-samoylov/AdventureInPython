### 🧬 Chapter 42: Shared DNA — Aliases in Python
*from **Adventure in Python** by Sergey Samoylov*

---

The hero was debugging a subtle error.  
Two variables were supposed to hold *different* lists.  
But changing one… changed the other.

He stared at the code.

```python
companions = ["Bit", "Byte"]
team = companions
team.append("Bug")
print(companions)  # ['Bit', 'Byte', 'Bug']
```

But *why*?

---

🧠 **Insight**:  
In Python, variables don't hold values directly.  
They *refer* to objects in memory.

When we write:

```python
team = companions
```

We’re not copying the list.  
We’re creating an **alias** — a second name for the same object.

---

🧪 The hero experimented:

```python
a = [1, 2]
b = a
a.append(3)
print(b)  # [1, 2, 3]
```

He tried to protect the second list by making a copy:

```python
a = [1, 2]
b = a.copy()
a.append(3)
print(b)  # [1, 2]
```

It worked.

---

> “Beware of shadow names,” said Terminal.  
> “They carry your data — and your consequences.”

---

### 🧩 Task for the reader

You are given a list of sensor readings:

```python
readings = [0.95, 1.01, 0.99]
```

1. Create a function that modifies this list (e.g., adds a new reading).
2. Observe what happens if you pass the list directly.
3. Then create a safe version that copies the list inside the function.

**Bonus**: Can you think of a case where aliasing might be *useful*?

---

*“An alias isn’t a twin — it’s your own shadow.”*  
— Terminal

---

[Chapter 43](Chapter_43.md)
