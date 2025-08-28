---
title: [ GET ] List of models - Список моделей
type: docs
weight: 1
---

## Список моделей

``` http
GET /platform/models
```

Возвращает список доступных моделей.

## Заголовки
- `Authorization: Bearer YOUR_API_KEY`

## Пример ответа
``` json
{
  "data": [
    {
      "id": "google/gemini-2.5-pro",
      "object": "model",
      "created": 1692913639,
      "owned_by": "google"
    }
  ]
}
```

### Статус-коды

- `200 - OK`
- `401 - Unauthorized`
- `500 - Internal Server Error`