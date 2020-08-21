# Файлы CSS
<!-- position: 3 -->

Bludit позволяет разработчикам использовать готовые методы и писать код чище, быстрее, красивее.

В этом уроке мы будем использовать следущие имена:
- Название темы `box`
- Адрес сайта `https://www.example.com`
- Путь к теме `/bl-themes/box/`
- Путь к файлу CSS `/bl-themes/box/style.css`

Давайте создадим файл с именем `style.css`. Этот файл будет находится по адресу `/bl-themes/box/style.css`. Вам не нужно будет беспокоиться о пути к CSS файлу, если вы используете `Theme::`.
```
<?php
	echo Theme::css('style.css');
?>
```

HTML вывод
```
<link rel="stylesheet" type="text/css" href="https://www.example.com/bl-themes/box/style.css">
```

<h2 id="example">Пример</h2>

Следующий фрагмент HTML и PHP-это полный пример того, как подключить два CSS-файла в тему.

```
<!DOCTYPE html>
<html>
	<head>
		<title>Hello</title>

		<?php
			echo Theme::css('style.css');
			echo Theme::css('buttons.css');
		?>
	</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```