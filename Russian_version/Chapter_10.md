## 📖 Глава 10: Циклы и поток ➿  
*from Adventure in Python by Sergey Samoylov*

---

Он пошёл.

Впервые с момента пробуждения  
он почувствовал направление.

Влево. Вперёд. Вперёд. Снова вперёд.

Терминал пульсировал:

> Теперь ты понимаешь объекты.  
> Теперь ты понимаешь память.  
> Но движение — это *поток*.

> Циклы — это пульс живого кода.

Герой сделал ещё шаг —  
уже внутри цикла.

---

### 🔹 Цикл `for`

Чтобы повторить что-то заданное число раз:

```python
for step in range(3):
    print(f"Step {step + 1}: moving forward")
```

Вывод:

```
Step 1: moving forward  
Step 2: moving forward  
Step 3: moving forward
```

---

### 🔹 Перебор списков

```python
tools: list[str] = ["echo", "ping", "scan"]

for tool in tools:
    print(f"Tool activated: {tool}")
```

---

### 🔹 Цикл `while`

Цикл `while` работает, пока условие — истина.

```python
energy: int = 5

while energy > 0:
    print(f"Energy left: {energy}")
    energy -= 1
```

Вывод:

```
Energy left: 5  
Energy left: 4  
...  
Energy left: 1
```

Будь осторожен:  
если условие не меняется, цикл может быть бесконечным.

---

### 🔹 Прерывание цикла

`break` останавливает цикл досрочно:

```python
for step in range(10):
    if step == 3:
        print("Obstacle found!")
        break
    print(f"Step {step}")
```

---

### 🔹 Пропуск шага

`continue` пропускает текущую итерацию:

```python
for tool in tools:
    if tool == "ping":
        continue
    print(f"Using {tool}")
```

---

### 🔹 Цикл + логика

Сочетай списки, условия и циклы:

```python
inventory: list[str] = ["map", "flashlight", "codebook"]

for item in inventory:
    if item == "flashlight":
        print("You see the path ahead.")
    else:
        print(f"You carry the {item}.")
```

---

Герой шёл по кругу.

Он учился двигаться, повторять,  
и выбирать с контролем.

Каждый цикл стал решением.

Каждый проход — логичным и чётким.

---

### 🧠 Задание: Энергия пути

Создай класс `Walker` с:
- Атрибутом `energy` (int)
- Методом `walk()` с циклом while
- На каждом шаге — вывод текущей энергии
- Остановка, когда энергия станет 0

Дополнительно:
- Метод `rest()` для восстановления энергии
- Проверка энергии перед ходьбой

---

В **Главе 11: Взаимодействие 🗣️**  
герой больше не будет один.  
Он встретит первое **цифровое существо** —  
и научится **разговаривать**.
