# Favicon
<!-- position: 5 -->

Bludit позволяет разработчикам использовать готовые методы и писать код чище, быстрее, красивее.

В этом уроке мы будем использовать следущие имена:
- Название темы `box`
- Адрес сайта `https://www.example.com`
- Путь к теме `/bl-themes/box/`
- Путь к файлу CSS `/bl-themes/box/favicon.png``

Слудущий метод `Theme::` позволяет подключить favicon на сайт, добавляя мета-тег в описании страниц; По умолчанию MIME возвращает тип `image/png`.
```
<?php
	echo Theme::favicon('favicon.png');
?>
```

HTML вывод
```
<link rel="shortcut icon" href="https://www.example.com/bl-themes/box/favicon.png" type="image/png">
```

Кроме того, вы можете указать тип MIME, если хотите использовать другой тип favicon, например `.ico`.
```
<?php
	echo Theme::favicon('favicon.ico', 'image/x-icon');
?>
```

HTML вывод
```
<link rel="shortcut icon" href="https://www.example.com/bl-themes/box/favicon.ico" type="image/x-icon">
```

<h2 id="example">Пример</h2>

Пример подключения Favicon на сайт.

```
<!DOCTYPE html>
<html>
	<head>
		<title>Hello</title>

		<?php
			echo Theme::favicon('favicon.png');
		?>
	</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```