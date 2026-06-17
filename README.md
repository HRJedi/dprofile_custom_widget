# Dprofile contact widget

Минимальная заготовка для публикации через GitHub Pages и вставки в Dprofile через iframe.

## Что внутри

- `index.html` — готовый виджет с кнопками:
  - Telegram
  - WhatsApp
  - Email
  - Телефон
- `.nojekyll` — чтобы GitHub Pages не пытался обрабатывать проект как Jekyll-сайт.

## Как настроить контакты

Откройте `index.html` и замените значения в блоке `CONTACTS`:

```js
const CONTACTS = {
  telegramUsername: "username",
  whatsappPhone: "79990000000",
  email: "hello@example.com",
  phone: "+79990000000",
  whatsappText: "Здравствуйте! Хочу обсудить проект.",
  emailSubject: "Обсуждение проекта",
  emailBody: "Здравствуйте! Хочу обсудить проект."
};
```

Важно:

- `telegramUsername` — без `https://t.me/`, можно с `@` или без.
- `whatsappPhone` — только номер в международном формате, без пробелов и скобок.
- `phone` — номер для обычного звонка через `tel:`.
- `email` — адрес для `mailto:`.

## Публикация на GitHub Pages

1. Создайте публичный репозиторий, например `dprofile-contact-widget`.
2. Загрузите в него `index.html` и `.nojekyll`.
3. Откройте настройки репозитория: `Settings` → `Pages`.
4. В разделе `Build and deployment` выберите:
   - Source: `Deploy from a branch`
   - Branch: `main`
   - Folder: `/root`
5. Сохраните настройки.
6. После публикации GitHub выдаст ссылку вида:

```text
https://<github-username>.github.io/dprofile-contact-widget/
```

## Вставка в Dprofile

В проекте Dprofile добавьте блок «Встроенный код» и вставьте iframe:

```html
<iframe
  src="https://<github-username>.github.io/dprofile-contact-widget/"
  width="100%"
  height="520"
  frameborder="0"
  style="border: 0; width: 100%; border-radius: 28px; overflow: hidden;"
></iframe>
```

Высоту `height="520"` можно менять под фактический размер блока.
