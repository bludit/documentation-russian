# Название и описание
<!-- position: 2 -->

Bludit позволяет разработчикам использовать готовые методы и писать код чище, быстрее, красивее.

<h2 id="title">Заголовок</h2>

Вывести `<title>` тег в head с динамическим текстом, можно воспользовавшись(Заголовок принимает конфигурацию, определенную в настройках Вашего сайта.):
```
<?php
	echo Theme::metaTags('title');
?>
```

HTML Вывод
```
<title>Page title | Title site</title>
```

<h2 id="description">Описание</h2>
Вывести `<description>` тег в head с динамическим текстом, можно воспользовавшись (Описание принимает конфигурацию, определенную в настройках Вашего сайта.):
```
<?php
	echo Theme::metaTags('description');
?>
```

HTML Вывод
```
<meta name="description" content="Description about your site">
```

<h2 id="example">Пример</h2>

Вот полный пример того, как использовать заголовок и описание в теме.

```
<!DOCTYPE html>
<html>
	<head>
		<?php
			echo Theme::metaTags('title');
			echo Theme::metaTags('description');
		?>
	</head>
<body>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

</body>
</html>
```