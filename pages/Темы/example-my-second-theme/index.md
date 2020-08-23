# Пример: Моя вторая тема
<!-- position: 101 -->

Сейчас мы создадим тему с поддержкой файлов CSS, JavaScript и плагинов.

Назовем нашу тему, например - `Mars`.

Если вы не желаете создавать все постепенно, то вы можете скачать исходные файлы темы <a href="https://github.com/bludit/examples/tree/master/themes/mars">Mars theme</a>.

<h2 id="folder-structure">Структура папок</h2>
Создадим папку с названием темы в папке `/bl-themes/`; Путь к ней должен выглядеть так: `/bl-themes/mars/`.

Далее, создадим папки - `languages`, `css`, `js`.
- Создайте папку `languages` внутри папки `/bl-themes/mars/`
- Создайте папку `css` внутри папки `/bl-themes/mars/`
- Создайте папку `js` внутри папки `/bl-themes/mars/`

```
/bl-themes/mars/
	css/
	js/
	language/
```

<h2 id="name-and-information">Название и информация о теме</h2>
Создадим файл с информацией о теме. Создадим файл `metadata.json` в корневой папке темы с содержимым:

```
{
	"author": "Bludit",
	"email": "",
	"website": "",
	"version": "1.0",
	"releaseDate": "2019-01-01",
	"license": "MIT",
	"compatible": "3.0",
	"notes": ""
}
```

Создадим файл `en.json`, который будет содержать название и описание темы. Создадим его в папке `/bl-themes/mars/languages/` с содержимым:

```
{
	"theme-data":
	{
		"name": "Mars",
		"description": "This is my second theme for Bludit."
	}
}
```
<h2 id="index">Index.php</h2>
Давайте поработаем над файлом `index.php`; Создайте такой файл в папке `/bl-themes/mars/` с содержимым:

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
</head>
<body>

</body>
</html>
```

<h2 id="css-files">CSS файл</h2>
Подключим CSS файл к теме:
- Используя метод `Theme::css()`
- Или используя html tag `<link href="..." rel="stylesheet" type="text/css" />`

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>
</head>
<body>

</body>
</html>
```

<h2 id="javascript-files">Javascript файл</h2>
Подключим JavaScript файл:
- Используя метод `Theme::js()`
- Или используя html tag `<script>...</script>`

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>
</head>
<body>

</body>
</html>
```

<h2 id="plugin-support">Добавим поддержку плагинов</h2>
Чтобы добавить поддержку плагинов мы будем использовать метод `Theme::plugins()`.

Hook'и плагинов для сайта таковы:
- `siteHead` взаимодействует с тегами `<head>...</head>` .
- `siteBodyBegin` взаимодйствует с тегами `<body>...</body>`; Вы можете использовать его для приветственного баннера или какой-нибудь панели инструментов в верхней части страницы..
- `siteBodyEnd` взаимодйствует с тегами `<body>...</body>`; Вы можете использовать для вывода, например, JavaScript кода.

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<!-- Here all the rest of HTML code -->

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```

<h2 id="site-logo-title-and-slogan">Лого заголовок и слоган сайта</h2>
Вы можете вызвать настройки для лого, заголовка, слогана из настроек Bludit.
```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<img src="<?php echo $site->logo() ?>" alt="" width="128">
	<h1><?php echo $site->title() ?></h1>
	<h2><?php echo $site->slogan() ?></h2>

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```

<h2 id="where-am-i">Где я?</h2>
Давайте поработаем над содержимым сайта.

Чтобы определить, где сейчас находится пользователь, можно вызвать переменную `$WHERE_AM_I`.Например, если пользователь просматривает начальную страницу, то переменная выдаст `home`. Если пользователь просматривает обычную страницу, то переменная выдаст `page`.

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<h1><?php echo $site->title() ?></h1>
	<h2><?php echo $site->slogan() ?></h2>

	<?php if ($WHERE_AM_I=='page'): ?>
		<p>The user is watching a particular page</p>
	<?php elseif ($WHERE_AM_I=='home'): ?>
		<p>The user is watching the homepage</p>
	<?php endif ?>

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```

<h2 id="main-content">Основное содержимое</h2>
Если пользователь находится на главной странице, Bludit генерирует глобальный массив `$pages` в котором находятся все опубликованные страницы. Каждая страница, это объект главной страницы.

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<h1><?php echo $site->title() ?></h1>
	<h2><?php echo $site->slogan() ?></h2>

	<?php if ($WHERE_AM_I=='page'): ?>
		<p>The user is watching a particular page</p>
	<?php elseif ($WHERE_AM_I=='home'): ?>
		<?php foreach ($content as $page): ?>
			<h3><?php echo $page->title(); ?></h3>
		<?php endforeach ?>
	<?php endif ?>

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```
В этом примере мы собираемся напечатать заголовок и содержимое.

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">

	<!-- CSS -->
	<?php echo Theme::css('css/style.css') ?>

	<!-- Javascript -->
	<?php echo Theme::js('js/mars.js') ?>

	<!-- Load plugins with the hook siteHead -->
	<?php Theme::plugins('siteHead') ?>
</head>
<body>
	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyBegin') ?>

	<h1><?php echo $site->title() ?></h1>
	<h2><?php echo $site->slogan() ?></h2>

	<?php if ($WHERE_AM_I=='page'): ?>
		<h3><?php echo $page->title(); ?></h3>
	<?php elseif ($WHERE_AM_I=='home'): ?>
		<?php foreach ($pages as $page): ?>
			<h3><?php echo $page->title(); ?></h3>
		<?php endforeach ?>
	<?php endif ?>

	<!-- Load plugins with the hook siteBodyBegin -->
	<?php Theme::plugins('siteBodyEnd') ?>
</body>
</html>
```

<div class="note">
<div class="title">Скачать</div>
Скачать искодный код темы <a href="https://github.com/bludit/examples/tree/master/themes/mars">Mars theme</a>.
</div>