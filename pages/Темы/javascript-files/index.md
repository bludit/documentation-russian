# Файлы Javascript
<!-- position: 4 -->

Bludit позволяет разработчикам использовать готовые методы и писать код чище, быстрее, красивее.

В этом уроке мы будем использовать следущие имена:
- Название темы `box`
- Адрес сайта `https://www.example.com`
- Путь к теме `/bl-themes/box/`
- Путь к Javascript файлу `/bl-themes/box/main.js`

Давайте создадим файл с именем `main.js`. Этот файл будет находится по адресу `/bl-themes/box/main.js`. Вам не нужно будет беспокоиться о пути к JS файлу, если вы используете `Theme::`.
```
<?php
	echo Theme::js('main.js');
?>
```

HTML вывод
```
<script src="https://www.example.com/bl-themes/box/main.js"></script>
```

<h2 id="example">Пример</h2>

Вот полный пример того, как подключить два файла Javascript в тему.

```
<!DOCTYPE html>
<html>
	<head>
		<title>Hello</title>
	</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

<?php
	echo Theme::js('main.js');
	echo Theme::js('buttons.js');
?>

</body>
</html>
```