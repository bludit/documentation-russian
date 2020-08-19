# Основы плагина
<!-- position: 1 -->

Плагины в Bludit находятся в папке `bl-plugins`, и они имеют предопределенную структуру. Каждый плагин является объектом в Bludit, с различными hook'ами (методами).

<h2 id="structure">Структура папок и файлов</h2>
Это обязательная структура папок и файлов для плагина:

```
/bl-plugins/{PLUGIN_NAME}/
	languages/en.json
	metadata.json
	plugin.php
```

<h2 id="name-and-description">Название и описание</h2>
Название и описание плагина хранится в файле формата JSON, `languages/en.json`.

```
{
	"plugin-data":
	{
		"name": "Hello World",
		"description": "Print Hello World in the sidebar"
	}
}
```

<h2 id="information">Информация</h2>
Мета информация плагина хранится в файле формата JSON, `metadata.json`.

```
{
	"author": "Bludit",
	"email": "",
	"website": "https://plugins.bludit.com",
	"version": "1.0",
	"releaseDate": "2020-06-01",
	"license": "MIT",
	"compatible": "3.0",
	"notes": ""
}
```

<h2 id="hello-world">Привет, Мир!</h2>
Создадим плагин `Hello, World!` (Привет, Мир!). Приведенный ниже код, должен находится в файле `plugin.php`.

```
<?php
	class pluginHello extends Plugin {
		public function siteSidebar() {
			echo 'Hello world';
		}
	}
?>
```

<div class="note">
<div class="title">Примечание</div>
Скачать исходный код плагина <a href="https://github.com/bludit/examples/tree/master/plugins/hello-world">Hello World</a>.
</div>