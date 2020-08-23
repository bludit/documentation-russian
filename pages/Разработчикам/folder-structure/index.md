# Структура папок
<!-- position: 2 -->

Это базовая структура папок
```
/bl-content/	<-- Базы данных и весь загруженный контент на сайт
/bl-kernel/		<-- Ядро Bludit
/bl-languages/	<-- Языковые пакеты/файлы
/bl-plugins/	<-- Плагины
/bl-themes/		<-- Темы
```

## bl-content
Это одна из важных папок Bludit. Именно в ней хранятся базы данных и весь загруженный контент на сайт. (Статьи, изображения, пользователи и т.п.)
```
/bl-content/

	databases/
		plugins/		<-- База данных плагинов
		pages.php		<-- База данных страниц
		security.php	<-- База данных настроек безопасности
		site.php		<-- База данных настроек сайта
		tags.php		<-- База данных тегов
		users.php		<-- База данных пользователей

	pages/				<-- Содержимое: страницы
		about/index.txt
		food/index.txt

	tmp/				<-- Временные файлы

	uploads/			<-- Загруженные файлы
		profiles/		<-- Изображения профилей
		thumbnails/		<-- Изображения обложек страниц
		photo1.jpg
		photo2.png

	workspaces/			<-- Рабочее место для плагинов
```

## bl-kernel
Эта папка содержит ядро Bludit.

## bl-languages
Эта папка содержит языковые пакеты, хранящиеся в формате JSON и имеющие кодировку UTF-8.

```
/bl-languages/
	bg_BG.json
	cs_CZ.json
	de_CH.json
	en.json
	es.json
	...
```

## bl-plugins
Эта папка содержит плагины. В нее загружаются все новые плагины.

```
/bl-plugins/
	about/
	disqus/
	rss/
	sitemap/
	tinymce/
	...
```

## bl-themes
Эта папка содержит темы. В нее загружаются темы.

```
/bl-themes/
	alternative/
	blogx/
	...
```
