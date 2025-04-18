## 🗂️ Глава 12: Ключи от Мира 🔍  
*from Adventure in Python by Sergey Samoylov*

---

Чем глубже он продвигался,  
тем больше мир напоминал разум, а не просто машину.

Появились символы.  
И за каждым символом скрывался **смысл**.

Герой понял: *списки* — это только начало.  
Они хороши для порядка,  
но не для **связей**.

Он нуждался в чём-то более умном.  
В чём-то, что объединяет **одно с другим**.

Слово с его определением.  
Команду с её эффектом.  
Имя с его значением.

И он открыл: **словарь**.

---

### 📜 Первая Карта

```python
terminal_commands: dict[str, str] = {
    "scan": "Обнаружить активность поблизости",
    "map": "Показать структуру окружения",
    "hack": "Обойти защиту"
}
```

Каждый ключ — как **метка**,  
каждое значение — как **функция**.

```python
print(terminal_commands["scan"])
```

> Обнаружить активность поблизости

Это было просто. Мощно.  
Он мог вызывать смысл одним действием.

---

Но что, если бы он запросил вдруг несуществующее?

```python
print(terminal_commands["launch"])
```

> ❌ `KeyError`

Мир снова вздрогнул.

Он научился подстраховываться:

```python
if "launch" in terminal_commands:
    print(terminal_commands["launch"])
else:
    print("Неизвестная команда")
```

Теперь он не просто читал карту —  
он **владел навигацией**.

---

### 🧠 Данные со Смыслом

Он понял: словари — не просто контейнеры.  
Это **модели знания**.

Списки хранят.  
Словари **объясняют**.

И он пошёл дальше.

---

### 🛠️ Практика: Описываем Инструменты

```python
def describe_tools(tools: dict[str, str]) -> None:
    """
    Печатает каждый инструмент и его описание.
    """
    print("Инструменты и их назначение:")
    for name, function in tools.items():
        print(f"{name.title()}: {function}")

inventory: dict[str, str] = {
    "сканер": "Читает активность поблизости",
    "глушилка": "Нарушает вредоносный трафик",
    "декодер": "Расшифровывает сообщения"
}

describe_tools(inventory)
```

Теперь каждый предмет имел **имя** и **смысл**.

Сила героя росла.

---

### 📚 Что мы узнали в этой главе

- Использование `dict[str, str]` для связей
- Обращение по ключу через `[]`
- Проверка наличия ключа: `"key" in dict`
- Перебор с `.items()`
- Написание функций, работающих со словарями

---

### 🧠 Размышления

Мир прошептал:  
*"У каждого ключа есть замок.  
У каждой команды — назначение."*

Со словарями герой не просто хранил данные —  
он строил **карту смыслов**.

Совсем скоро его программы  
не просто реагировали…  
они начнут **понимать**.

---

Продолжи своё приключение в [Главе 13](Chapter_13.md)?
