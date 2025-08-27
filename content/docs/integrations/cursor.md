---
title: Интеграция с Cursor
type: docs
weight: 2
---

В vibeRouter доступна интеграция с Cursor через OpenAI‑совместимый endpoint. Ниже — короткая инструкция по настройке внутри Cursor.

## Шаги настройки

1) Откройте меню `File → Preferences → Cursor Settings`.

![Откройте Cursor Settings](/images/integrations/cursor_go_to_cursor_settings.png)

2) Перейдите в раздел `Models`.

![Откройте Models](/images/integrations/cursor_select_models.png)

3) Пролистайте вниз до блока `API Keys` и укажите параметры:

- `API Key`: введите ваш API‑ключ из личного кабинета vibeRouter
- `API Endpoint`: `https://api.viberouter.dev/v1`

![Проверьте API endpoint и ключ](/images/integrations/cursor_api_endpoint_check.png)

После этого Cursor начнёт отправлять запросы через шлюз vibeRouter. Настройки сохраняются автоматически.

## Примечания

- Важно указывать полный адрес с `/v1` и схемой `https://`.
- Если автодополнение или ответы не приходят, перепроверьте endpoint и актуальность ключа.
- Расход токенов зависит от объёма контекста/индексации в проекте — контролируйте лимиты в личном кабинете.

