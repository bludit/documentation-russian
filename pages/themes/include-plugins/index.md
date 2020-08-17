# Подключение плагинов
<!-- position: 6 -->

Bludit позволяет разработчикам использовать готовые методы и писать код чище, быстрее, красивее.

Лист с hooks:
- https://docs.bludit.com/en/plugins/hooks-list

Например, чтобы выполнить все плагины с hook'ом `siteHead`, вы можете использовать метод `Theme::plugins()`.
```
<?php
	Theme::plugins('siteHead');
?>
```

<h2 id="example">Пример</h2>

Вот полный пример того, как подключить 3 типа hook'ов и выполнить их в правильном месте в теме.

```
<!DOCTYPE html>
<html>
	<head>
		<title>Hello</title>

		<?php
			Theme::plugins('siteHead');
		?>
	</head>
<body>

<?php
	Theme::plugins('siteBodyBegin');
?>

<h1>This is a Heading</h1>
<p>This is a paragraph.</p>

<?php
	Theme::plugins('siteBodyEnd');
?>

</body>
</html>
```