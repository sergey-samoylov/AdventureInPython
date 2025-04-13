## 🧩 Chapter 49: Composition over Inheritance
*from **Adventure in Python** by Sergey Samoylov*

---

> “Don’t become what you extend,”  
> the Companion warned.  
> “Become what you build.”

The Hero had seen inheritance.  
One class becomes another.  
But now he notices a pattern even more flexible.

> “Instead of inheriting behavior,”  
> the Companion said,  
> “you *compose* behavior from parts.”

---

### 🧱 What Is Composition?

**Composition** is building complex behavior  
by assembling smaller parts —  
just like LEGO bricks.

Instead of saying "I am a Dog, and a Dog is an Animal",  
you say "I have a tail, and I can bark."

```python
class Tail:
    def wag(self) -> None:
        print("Wagging...")

class Bark:
    def bark(self) -> None:
        print("Woof!")

class Dog:
    def __init__(self) -> None:
        self.tail = Tail()
        self.voice = Bark()

my_dog = Dog()
my_dog.tail.wag()
my_dog.voice.bark()
```

Now `Dog` uses behavior from other classes.  
If you want to change how barking works — change only `Bark`.  
No need to rewrite `Dog`.

---

### 🤔 When to Use Composition?

Inheritance is great for "is-a" relationships:  
A Cat *is* an Animal.

Composition shines for "has-a" relationships:  
A Robot *has* a battery.  
A Game *has* a player and an enemy.  
A Wizard *has* spells.

Composition allows more **flexibility and reuse**.

---

### 🛠 Challenge

Create a `Vehicle` class that uses composition.  
You can define parts like:

- `Engine` class with a `start()` method  
- `Wheels` class with a `roll()` method

Then combine them in your `Vehicle` like this:

```python
class Vehicle:
    def __init__(self):
        self.engine = ...
        self.wheels = ...
```

Try using your vehicle in action!

---

The Hero now understands:  
sometimes, true power is not in inheritance,  
but in careful assembly.  
In building machines from *well-made parts.*

And the world of code opens new doors of design.

[Chapter 50](Chapter_50.md)
