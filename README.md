# LocalChat.NotificationService

Сервис уведомлений: email/push о решении по заявке на доступ и offline-уведомления о новых сообщениях (без plaintext).

## Назначение

- подписаться на события Identity (`AccessApproved` / `AccessRejected`);
- уведомлять о новых сообщениях, если пользователь offline (P1+);
- шаблоны и провайдеры (SMTP, Web Push, FCM и т.д.).

## Стек

- .NET 10
- очереди / outbox (по мере внедрения)
- провайдеры доставки (конфиг через env)

## Документация

- [Обзор](docs/overview.md)
- [TODO](docs/todo.md)

## Запуск

Фаза **P1**. Плановый порт: **5104**.

## Связанные репозитории

| Репозиторий | Роль |
|---|---|
| [LocalChat.IdentityService](https://github.com/MuskatGroup/LocalChat.IdentityService) | События доступа |
| [LocalChat.ChatService](https://github.com/MuskatGroup/LocalChat.ChatService) / Realtime | Триггеры offline |
| [LocalChat.Web](https://github.com/MuskatGroup/LocalChat.Web) | Подписка на Web Push |

## Лицензия

Apache-2.0 — см. [LICENSE](LICENSE).
