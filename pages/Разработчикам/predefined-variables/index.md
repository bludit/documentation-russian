# Зарезервированные переменные
<!-- position: 3 -->

Bludit имеет несколько зарезервированных переменных.

<h2 id="content">$content</h2>

Переменная `$content` представляет массив, который содержит все опубликованные страницы(кроме статических страниц).Каждая страница в массиве является [объектом страницы](https://github.com/bludit/bludit/blob/master/bl-kernel/pagex.class.php).

Массив может быть отсортирован по `дате` или по `позиции`, это можно настроитьва в настройках Bludit.

Взгляните как работать с этой переменной:
- https://docs.bludit.com/en/dev-snippets/content-pages

<h2 id="staticContent">$staticContent</h2>

Переменная `$staticContent` представляет массив, который содержит все опубликованные `статические` страницы. Каждая страница в массиве является [объектом страницы](https://github.com/bludit/bludit/blob/master/bl-kernel/pagex.class.php).

Массив может быть отсортирован по `позиции` темой Bludit.

Взгляните как работать с этой переменной:
- https://docs.bludit.com/en/dev-snippets/content-static

<h2 id="page">$page</h2>

Переменная `$page` отображает любую страницу,которую просматривает пользователь. Эта переменная является [объектом страниц](https://github.com/bludit/bludit/blob/master/bl-kernel/pagex.class.php).

Например, если пользователь просматривает страницу - `https://www.example.com/my-dog-rules`, переменная `$page` передаст ключ, например: `my-dog-rules`.

<h2 id="pages">$pages</h2>

Переменная `$pages` является [объектом страниц](https://github.com/bludit/bludit/blob/master/bl-kernel/pages.class.php). Этот объект используется для управления базой данных страниц.

<h2 id="tags">$tags</h2>

Переменная `$tags`является [объектом тегов](https://github.com/bludit/bludit/blob/master/bl-kernel/tags.class.php). Этот объект используется для управления базой данных тегов.

<h2 id="categories">$categories</h2>

Переменная `$categories` является [объектом категорий](https://github.com/bludit/bludit/blob/master/bl-kernel/categories.class.php). Этот объект используется для управления базой данных категорий.
