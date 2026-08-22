# ДЗ 11 — Simple Site на GitHub Pages

Ця папка містить чисту публікаційну версію домашнього завдання №11:
рефакторинг **Simple Site** з використанням SCSS.

Робоча сторінка:
<https://mila9393.github.io/hw_09-simple-site-pages/hw_11/>

## Виконання

- SCSS скомпільовано у фінальний `css/style.css`;
- `index.html` підключає фінальний файл стилів;
- файл `images/project.svg` додано до публікації;
- сторінку опубліковано та перевірено на GitHub Pages.

## Файли публікації

```text
hw_11/
├── index.html
├── README.md
├── css/
│   └── style.css
└── images/
    └── project.svg
```

- `index.html` — готова розмітка з адаптивним YouTube `iframe`;
- `css/style.css` — фінальний CSS, скомпільований зі SCSS;
- `images/project.svg` — іконка, яку браузер завантажує шість разів;
- `README.md` — пам'ятка про склад публікації.

## Посилання на вихідний код

Повний варіант ДЗ 11 зі `scss/style.scss` зберігається в закритому
навчальному репозиторії:

<https://github.com/Mila9393/hillel_fullstack_js_2026/tree/main/01_html_css/hw_11>

## ПАМ'ЯТКА СТУДЕНТУ:

## Що не публікується на GitHub Pages

- `scss/style.scss` і папка `scss/` — вихідний код зберігається в закритому
  репозиторії домашніх робіт;
- `style.css.map` та інші файли `*.css.map` — карти джерел призначені для
  активної розробки;
- коментар `/*# sourceMappingURL=... */` у фінальному CSS.

## Нові інструменти

Для роботи зі SCSS використано:

- `Node.js` — середовище для запуску інструментів розробки;
- `npm` — пакетний менеджер, який встановлюється разом із Node.js;
- `pnpm` — пакетний менеджер, через який встановлено Sass;
- `Sass` — компілятор SCSS у CSS.

## Source map: розробка і публікація

Під час розробки викладач рекомендував використовувати watcher із source
map, щоб DevTools показував вихідні рядки SCSS:

```bash
sass --watch scss/style.scss:css/style.css
```

Перед публікацією watcher зупиняється, а CSS компілюється без source map:

```bash
sass --no-source-map scss/style.scss css/style.css
```

Якщо карта була створена раніше, `style.css.map` потрібно видалити окремо й
перевірити відсутність `sourceMappingURL` у кінці `style.css`.
