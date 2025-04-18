## 📖 Глава 2: Дом на Командной Строке 🏡

*from Adventure in Python by Sergey Samoylov*

---

Темнота стала холоднее.  
Он умел говорить с системой.  
Но она не говорила с ним. Пока что.

Он смотрел в мигающий курсор и думал:

> «А что если бы она задала вопрос?»  
> «А если бы я мог ответить?»

Он написал:

```python
name = input("Как тебя зовут? ")
print("Привет,", name)
```

Пустота дрогнула.  
Появился вопрос.  
Он ввёл: `Алекс`.

```
Привет, Алекс
```

Терминал откликнулся.  
Он спросил. Система ответила.

Он улыбнулся. Впервые он не просто наблюдал.  
Он *создавал*.

---

Он решил построить убежище.  
Не из камня и дерева, а из логики и решений.

Ему нужно было, чтобы система **реагировала на ввод**.

Он написал:

```python
if name == "Алекс":
    print("Добро пожаловать, Оператор.")
else:
    print("Доступ ограничен.")
```

Код **слушал**, **решал**, **отвечал**.

Это было немного. Но это было *его*.

Первые стены были воздвигнуты.  
Строка терминала - мой дом. Это - начало!

---

## 💡 Модуль 2: Ввод и Логика — Решения

---

> 🛠️ Цель: создать простой интерактивный скрипт.

---

### 🔹 `input()` — Голос пустоты

Функция `input()` задаёт вопрос и ждёт ответа:

```python
name: str = input("Кто ты? ")
print(f"Привет, {name}")
```

⚠️ Всё, что возвращает `input()`, — это строка.

---

### 🔹 `if`, `else`, `elif` — Путь выбора

Условия позволяют системе принимать решения:

```python
code: str = input("Введите код доступа: ")

if code == "42":
    print("Доступ разрешён.")
elif code == "admin":
    print("Права администратора.")
else:
    print("Ошибка доступа.")
```

---

### 🔹 `def` — Создание команд

Функции помогают структурировать и переиспользовать код.

```python
def greet(name: str) -> None:
    """
    Приветствие пользователя.
    """
    print(f"Добро пожаловать, {name}!")


user: str = input("Введите имя: ")
greet(user)
```

---

### 🧠 Задание

Создай скрипт, который:
1. Спрашивает имя и код.
2. Проверяет код.
3. Позволяет войти или отказывает.

💡 Пример вывода:

```
Имя: Нео
Код: 1337
Привет, Нео.
Уровень доступа: Хакер.
```

---

🧱 Теперь у тебя есть:
- **ввод** — чтобы слушать,  
- **условия** — чтобы выбирать,  
- **функции** — чтобы строить.

В следующей главе ты столкнёшься с первым врагом.  
С багом.  
Сбойным элементом системы.

---

Готов перейти к [**главе 3: Зверь отладчика**](Chapter_03.md)?

Там будет цикл, исключения и ловушка из кода.
