## 📖 Chapter 10: Loops and Flow ➿
*from Adventure in Python by Sergey Samoylov*

---

He moved.

For the first time since his awakening,  
he felt direction.

Left. Right. Forward. Forward again.

The Terminal pulsed:

> Now you understand objects.  
> Now you understand memory.  
> But movement... that is *flow*.

> Loops are the heartbeat  
> of all living code.

The hero stepped again —  
this time inside a loop.

---

### 🔹 The `for` Loop

To repeat something a number of times:

```python
for step in range(3):
    print(f"Step {step + 1}: moving forward")
```

Output:

```
Step 1: moving forward  
Step 2: moving forward  
Step 3: moving forward
```

---

### 🔹 Looping Through Lists

```python
tools: list[str] = ["echo", "ping", "scan"]

for tool in tools:
    print(f"Tool activated: {tool}")
```

---

### 🔹 The `while` Loop

The `while` loop repeats **while a condition is true**.

```python
energy: int = 5

while energy > 0:
    print(f"Energy left: {energy}")
    energy -= 1
```

Output:

```
Energy left: 5  
Energy left: 4  
...  
Energy left: 1
```

Be careful — if the condition never ends,  
the loop will run *forever*.

---

### 🔹 Breaking a Loop

Use `break` to stop early:

```python
for step in range(10):
    if step == 3:
        print("Obstacle found!")
        break
    print(f"Step {step}")
```

---

### 🔹 Continue a Loop

Use `continue` to skip this round:

```python
for tool in tools:
    if tool == "ping":
        continue
    print(f"Using {tool}")
```

---

### 🔹 Combining Loops and Logic

You can combine lists, loops, and decisions:

```python
inventory: list[str] = ["map", "flashlight", "codebook"]

for item in inventory:
    if item == "flashlight":
        print("You see the path ahead.")
    else:
        print(f"You carry the {item}.")
```

---

The hero walked in loops.

He learned to move, to repeat,  
to react with control.

Each loop became a choice.

Each cycle — a pulse of logic.

---

### 🧠 Challenge: Energy Trek

Create a class `Walker` with:
- An `energy` attribute (int)
- A method `walk()` that reduces energy
- Inside it, use a while-loop
- Print each step with current energy
- Stop when energy reaches zero

You can also add:
- A `rest()` method to recharge
- A way to check energy level before walking

---

In [**Chapter 11: Interaction**](Chapter_11.md),  
the hero will no longer walk alone.  
He will meet his first **digital being** —  
and begin to **talk**.
