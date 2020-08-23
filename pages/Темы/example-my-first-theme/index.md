# Пример: Моя первая тема
<!-- position: 101 -->

Давайте создадим новую тему и дадим ей название `Coffee`.

- Создайте тему в каталоге `/bl-themes/`; Путь должен выглядеть вот так: `/bl-themes/coffee/`.
- Создайте папку с именем `languages`, внутри папки `/bl-themes/coffee/`.
- Создайте файл `en.json` вунтри папки `/bl-themes/coffee/languages/`.
- Создайте файл `metadata.json` вунтри папки `/bl-themes/coffee/`.
- Создайте файл `index.php`, вунтри папки `/bl-themes/coffee/`.

Когда это будет сделано, у вас должна быть следующая структура папок и файлов:

```
/bl-themes/coffee/
	languages/en.json
	metadata.json
	index.php
```

Следующим шагом является создание содержимого файлов.  Давайте начнем с `index.php` и добавьте следующий HTML и PHP код:

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="UTF-8">
	<title>Bludit</title>
</head>
<body>
	<?php foreach ($content as $page): ?>

		<h1><?php echo $page->title(); ?></h1>
		<div><?php echo $page->content(); ?></div>
		<hr>

	<?php endforeach; ?>
</body>
</html>
```

Отредактируем файл `languages/en.json` и добавим в него следущий JSON код.

```
{
	"theme-data":
	{
		"name": "Coffee",
		"description": "This is my first theme for Bludit."
	}
}
```

Отредактируем файл `metadata.json` и напишем подробную информацию о теме.

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

Поздравляю! Вы создали первую свою тему для Bludit. Теперь вы можете зайти в настройки и активировать ей.