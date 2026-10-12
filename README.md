# Клиентский кеш

```sh
pnpm install
pnpm dev
pnpm build
```

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

Общий компонент `SlideFrame` содержит горизонтальный контейнер с отступами
80 px с обеих сторон. Слот занимает всю высоту; контент может заходить
в область футера. Логотип и номер остаются поверх контента.

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
