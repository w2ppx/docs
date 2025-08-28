---
title: Интеграция с Cursor
type: docs
weight: 2
---

# Интеграция с Cursor

VibeRouter предоставляет эксклюзивную возможность использовать все возможности Cursor гораздо дешевле. Вы платите только за фактическое использование, без необходимости покупки подписок.

## Настройка интеграции

1. Откройте меню `File → Preferences → Cursor Settings`

![Откройте Cursor Settings](/images/integrations/cursor_go_to_cursor_settings.png)

2. Перейдите в раздел `Models`

![Откройте Models](/images/integrations/cursor_select_models.png)

3. В блоке `API Keys` укажите:

- `API Key`: ваш ключ из [личного кабинета](https://viberouter.dev/dashboard/api-keys)
- `API Endpoint`: `https://api.viberouter.dev/v1`

![Проверьте API endpoint и ключ](/images/integrations/cursor_api_endpoint_check.png)

Cursor автоматически сохранит настройки и начнет использовать VibeRouter API.

## Рекомендации по использованию

- Указывайте полный адрес endpoint включая `/v1` и `https://`
- Расход токенов напрямую зависит от объема контекста/индексации в проекте - контролируйте баланс и использование в [личном кабинете](https://viberouter.dev/dashboard)


## Решение проблем

Если автодополнение не работает:
1. Проверьте правильность endpoint и API ключа
2. Убедитесь, что аккаунт подтвержден
3. Проверьте баланс в личном кабинете (обратите внимание, что бонусный баланс поддерживает использование не всех моделей)

Нужна помощь? [Свяжитесь с нами](https://viberouter.dev/support)

