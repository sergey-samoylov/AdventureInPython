## ⏳ Chapter 21: Time and Timing 🕒  
*from Adventure in Python by Sergey Samoylov*

---

The digital cave was silent.  
Even the code had stopped whispering.

> "Why is nothing happening?"  
> the hero asked aloud.

> “Because you haven’t learned  
> to **control time** yet,”  
> came the voice of the Terminal.

---

### ⏱ Meet the `time` Module

Python has a built-in module  
that lets you pause, track, or measure time.

Let’s import it:

```python
import time
```

---

### 😴 Sleep to Pause

Want your program to wait before continuing?

```python
import time

print("Loading...")
time.sleep(2)
print("Ready!")
```

💡 `sleep()` takes seconds. You can use decimals too: `1.5`

---

### 🧮 Measuring Execution Time

You can measure how long something takes:

```python
import time

start: float = time.time()

for number in range(1000000):
    _ = number * number

end: float = time.time()

print(f"Done in {end - start:.2f} seconds")
```

---

### 📆 Current Time and Date

To get human-readable time:

```python
current_time: str = time.ctime()
print(f"Now: {current_time}")
```

This prints something like:  
`Now: Mon Apr 7 17:45:12 2025`

---

### 🧠 Challenge: Create a Countdown

Write a script that asks the user  
to enter a number of seconds  
and counts down to zero like this:

```
Enter seconds to count down: 5
5...
4...
3...
2...
1...
Time's up!
```

Use a `while` loop and `time.sleep()`.

---

### 🧠 Reflection

> “Time is not just something you endure,”  
> thought the hero,  
> “It’s a tool. A rhythm. A strategy.”

> “Well said,” replied the Machine,  
> “Master timing,  
> and your code becomes alive.”

---

Time to read next [Chapter 22](Chapter_22.md)⏲️
