# Клиентский кеш

```sh
pnpm install
pnpm dev
pnpm build
```

## GitHub Pages

`.github/workflows/deploy-pages.yml` собирает презентацию и публикует её при
push в `main`; также доступен ручной запуск `workflow_dispatch`.
В Settings → Pages источником публикации должен быть GitHub Actions.
Для приватного репозитория Pages требует GitHub Pro; публичный репозиторий
можно публиковать на GitHub Free.

Адрес публикации: `https://nz-web.github.io/server-state-holy-speech/`.
Сборка использует путь репозитория и hash-навигацию, поэтому прямые ссылки
на слайды работают без серверных перенаправлений.

```sh
pnpm build --base /server-state-holy-speech/ --router-mode hash
pnpm exec vite preview --base /server-state-holy-speech/
```

`PublicImage` автоматически учитывает путь публикации для изображений из
`public/`, включая динамические картинки и SVG. Локальный `pnpm dev`
продолжает работать по обычным адресам `/1`, `/2`, …

Slidev использует полотно 1920×1080 и сам масштабирует его под экран.
Шрифты и изображения находятся в `public/`; внешняя загрузка не нужна.
Все слайды описаны в одном `slides.md`, без подключений других Markdown-файлов.

Глобальный `styles/index.css` содержит только шрифты и базовые сбросы.
Оформление слайдов и компонентов задаётся Tailwind-подобными классами UnoCSS.
Общие цвета, шрифтовые семейства и отступ `gutter` находятся в `uno.config.ts`.
Точные размеры из Figma задаются классами вроде `text-[128px]`, `top-[168px]`.

## Обычный слайд

```md
---
layout: default
variant: right
showLogo: true
showNumbers: true
---

# Содержимое слайда
```

`showLogo` и `showNumbers` по умолчанию включены. Номер берётся из контекста
слайда Slidev и форматируется как `01`, `02`, …; пропа для замены номера нет.
Скрытый номер не меняет нумерацию следующих слайдов.

Варианты фона: `right`, `top-right`, `bottom-right`, `diagonal`, `diagonal-left`, `none`.
Координаты, размеры, цвет и прозрачность каждого пятна редактируются в
`config/gradients.ts`. `diagonal` содержит два пятна, `none` — ни одного.
Фон выполнен CSS-градиентами, без звёзд и шума.

У `default` контейнер имеет отступы 88 px сверху, 80 px по бокам и 72 px
снизу. На полотне 1920×1080 его размер — 1760×920; координаты контента
задаются относительно этого контейнера.

Для обложек и полноэкранных композиций доступен именованный слот `::canvas::`:
он занимает всю высоту и сохраняет боковые отступы 80 px. Логотип и номер
остаются поверх контента. Лейауты `store-code` и `image-center` используют
свои прежние контейнеры.

## Картинка по центру

```md
---
layout: image-center
image: /images/frontend-meme.png
alt: Описание картинки
showLogo: false
showNumbers: false
---

<MemeLabel>Редактируемая подпись поверх картинки</MemeLabel>
```

Фон — увеличенная размытая копия `image`. Необязательный `backgroundImage`
заменяет изображение фона. Оба лейаута поддерживают одинаковые `variant`,
`showLogo`, `showNumbers`. Слот этого лейаута накладывается на центральную
картинку; подписи третьего слайда остаются HTML, а не частью изображения.

Источники изображений и логотипа — три макета Figma:
[обложка](https://www.figma.com/design/txP6i6i8DKeFWEFoSv9zk2/Untitled?node-id=1-135),
[спикер](https://www.figma.com/design/txP6i6i8DKeFWEFoSv9zk2/Untitled?node-id=1-142),
[мем](https://www.figma.com/design/txP6i6i8DKeFWEFoSv9zk2/Untitled?node-id=1-158).
Шрифты взяты из локального набора `slidev-theme-magnit-tech`.
