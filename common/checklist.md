## Чек-лист фронтенда

Чек-лист может отличаться от специфики проекта, но есть обязательные практики, которые подойдут почти ко всем проектам. Некоторые задачи являются только для фронтенд разработчика, другие можно делегировать или обратиться за помощью к бэкенд разработчику, тестировщику или дизайнеру. При составлении чек-листа для конкретного проекта можно брать за основу следующее:

### Общее

- html валиден
- html, css, js минимизирован
- нет ошибок в консоли
- изображения, которые не попадают в первый экран грузятся отложено
- размер изображений и svg иконок указан для предотвращения скачков
- изображения минимизированы, рекомендуемый формат webp
- шрифт грузится в формате woff2, скорее всего единственный формат для проекта ([поддержка caniuse](https://caniuse.com/?search=woff2))
- нет ошибок eslint, typescript, stylelint
- тесты проходят без ошибок
- применены рекомендации с помощью lighthouse, по возможности быть в зелёной зоне
- кэширование запросов работает (обсудить с бэкендом, как работает сейчас и как должно)

### Рендринг страниц

- статические страницы/компоненты собираются с помощью технологии SSG
- динамические страницы/компоненты, которые нужны для индексации в SEO собираются с помощью технологии SSR
- динамические страницы/компоненты, которые не нужны для индексации и являются персонализированными для пользователя собираются с помощью CSR

### Дизайн

- сайт выглядит одинаково и не ломается в требуемых браузерах
- сайт адаптивен под разные устройства
- блоки с фоновыми изображениями имеют заливку (если цвет текста белый и пока картинка не загрузится без фона текст невозможно будет прочитать)

### SEO

- на страницах правильные заголовки, описания, мета теги
- используются семантические теги (header, footer, main и тд)
- соблюдена иерархия заголовков h1, h2 и тд.
- ссылки являются ссылками, кнопки кнопками. Не должно быть, чтобы кнопка делала переход на другую страницу или раздел

### Доступность

- интерактивные элементы имеют hover, active, focus состояние