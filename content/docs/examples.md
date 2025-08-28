---
title: SDK и примеры использования
next: integrations
---

## Примеры с различными параметрами

### Настройка температуры

```python
completion = client.chat.completions.create(
    model="gemini-2.5-flash",
    messages=[
        {"role": "user", "content": "Напиши креативную историю"}
    ],
    temperature=1.5
)
```

### Ограничение длины ответа

```python
completion = client.chat.completions.create(
    model="gemini-2.5-flash",
    messages=[
        {"role": "user", "content": "Напиши длинную историю"}
    ],
    max_tokens=100
)
```

### Потоковый режим

```python
stream = client.chat.completions.create(
    model="gemini-2.5-flash",
    messages=[
        {"role": "user", "content": "Расскажи длинную историю"}
    ],
    stream=True
)

for chunk in stream:
    print(chunk.choices[0].delta.content, end="")
```

### Контекстный диалог

```python
messages = [
    {"role": "system", "content": "Ты - эксперт по Python"},
    {"role": "user", "content": "Как создать виртуальное окружение?"},
    {"role": "assistant", "content": "Используйте команду `python -m venv env`"},
    {"role": "user", "content": "А как его активировать?"}
]

completion = client.chat.completions.create(
    model="gemini-2.5-flash",
    messages=messages
)
```

### Использование функций

```python
functions = [
    {
        "name": "get_weather",
        "description": "Получить погоду в городе",
        "parameters": {
            "type": "object",
            "properties": {
                "city": {
                    "type": "string",
                    "description": "Название города"
                }
            },
            "required": ["city"]
        }
    }
]

completion = client.chat.completions.create(
    model="gemini-2.5-flash",
    messages=[
        {"role": "user", "content": "Какая погода в Москве?"}
    ],
    tools=functions,
    tool_choice="auto"
)
```

## Работа с ошибками

```python
try:
    completion = client.chat.completions.create(
        model="gemini-2.5-flash",
        messages=[
            {"role": "user", "content": "Hello"}
        ]
    )
except Exception as e:
    if "429" in str(e):
        print("Превышен лимит запросов")
    elif "401" in str(e):
        print("Неверный API ключ")
    else:
        print(f"Ошибка: {e}")
```
