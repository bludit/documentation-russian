# Основы стилизации
<!-- position: 1 -->

Темы в Bludit очень гибкие, при создании вы можете использовать любой framework ([Bootstrap](http://getbootstrap.com/), [Foundation](https://foundation.zurb.com/), [Bulma](https://bulma.io), [UIkit](https://getuikit.com/), [Semantic UI](https://semantic-ui.com), и т.д.), любой JavaScript код. Все, что захотите!

Все темы находятся в папке `bl-themes` и имею предопределенную структуру.

<h2 id="structure">Струкутура папок и файлов</h2>
Это простая (и обязательная) структура папок и файлов для тем.

```
/bl-themes/{THEME_NAME}/
	languages/en.json
	metadata.json
	index.php
```

<h2 id="name-description">Название и описание</h2>
Название и описание темы хранится в языковом пакете темы `languages/en.json`.

```
{
	"theme-data":
	{
		"name": "Hello World",
		"description": "My new theme"
	}
}
```

<h2 id="information">Информация</h2>
Основаная информация о теме хранится в `metadata.json`.

```
{
	"author": "Bludit",
	"email": "",
	"website": "https://themes.bludit.com",
	"version": "1.0",
	"releaseDate": "2020-06-01",
	"license": "MIT",
	"compatible": "3.0",
	"notes": ""
}
```

<h2 id="examples">Примеры тем</h2>
У нас есть два примера, один простой, а второй более сложный с файлами CSS и Javascript.

- [My First Theme](https://docs.bludit.com/en/themes/example-my-first-theme)
- [My Second Theme](https://docs.bludit.com/en/themes/example-my-second-theme)