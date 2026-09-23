---
type: term
topic:
date_created:
tags:
---
**CORS** (Cross-Origin Resource Sharing) — это ==[механизм безопасности браузера](https://www.google.com/goto?url=CAESVgHrOzAVS_Y6ukHp178dMLl6se-ZhJnmJHNOHFymsr9-iLhiatesAmVduQL5Ia6lNjinQym6GdxUHtG3lJSjwN2k_fXhorbpslxeaK2zAf-mhsoWbO9-), который позволяет разрешать или запрещать веб-страницам запрашивать ресурсы с другого домена==. 

По умолчанию браузеры используют правило одного источника (_Same-Origin Policy_). Оно запрещает сайту на одном домене (например, `site.com`) получать данные через JavaScript от другого домена (`api.com`). CORS расширяет эти возможности и дает безопасно обмениваться данными между разными источниками. 

#### Как работает CORS
- **Запрос:** Когда сайт делает междоменный запрос, браузер добавляет специальный заголовок `Origin` с именем вашего домена.
- **Ответ сервера:** Сервер проверяет этот домен и возвращает ответ с разрешающими заголовками (например, `Access-Control-Allow-Origin`).
- **Проверка:** Если домен разрешен, браузер показывает данные скрипту. Если разрешения нет — браузер блокирует ответ и выдает ошибку.

Подробную техническую спецификацию можно изучить на странице [MDN Web Docs](https://www.google.com/goto?url=CAEScgHrOzAVE3erKnfJy3B_20SN185wkT186_myJ4S3I5oCVzsyrzNkaSwpJvFx8652WoI7jWmBrVybiotIzot_7jelRoBLukOG-tlbQ6lO43NFSXyKCHbGJwfyW8Bdet9MvcAnVaOJL-BNXohTh2Mf67rAtA). 

#### Зачем нужен CORS
- Защищает пользователей от кражи личных данных и вредоносных скриптов.
- Позволяет фронтенд-приложениям (например, на React или Vue) легально обращаться к внешним API на других серверах.
