# Админ Панель: контроллер и просмотр через плагины.
<!-- position: 3 -->

Bludit позволяет легко кастоимизировать админ панель с помощью плагинов.

<div class="note">
Эта функция реализована, начиная с Bludit v3.13
</div>

## Notes
- Bludit по умолчанию использует [Bootstrap](https://getbootstrap.com/) для стилизации, вы можете его использовать в админ панели.
- Просмотр плагина для админ панели - `/admin/plugin/<plugin-name>`

## Пример: Привет, Мир!
Данный плагин изменить тег `<title>` и выведет `Hello world!`.

После активации плагина, перейдем по адресу `https://www.example.com/admin/plugin/hello`.

```php
<?php

class Hello extends Plugin {

	public function adminController()
	{
		global $layout;
		$layout["title"] = "Hello Plugin | Bludit";
	}

	public function adminView()
	{
		return 'Hello world!';
	}

	public function adminSidebar()
	{
		$pluginName = Text::lowercase(__CLASS__);
		$url = HTML_PATH_ADMIN_ROOT.'plugin/'.$pluginName;
		$html = '<a id="current-version" class="nav-link" href="'.$url.'">Hello world</a>';
		return $html;
	}
}
?>
```

## Пример: изменение настрое с помощью формы
Следующий плагин имеет возможность изменять настройки Bludit. Визуально отображается форма, а контроллер управляется методом `POST`.

После активации плагина, перейдем по адресу `https://www.example.com/admin/plugin/settings`

```php
<?php

class CustomAdmin extends Plugin {

	public function adminController()
	{
		// Check if the form was sent
		if ($_SERVER['REQUEST_METHOD'] == 'POST') {
			global $site;
			$site->set(array('title'=>$_POST['title']));
		}
	}

	public function adminView()
	{
		// Token for send forms in Bludit
		global $security;
		$tokenCSRF = $security->getTokenCSRF();

		// Current site title
		global $site;
		$title = $site->title();

		// HTML code for the form
		$html = '
			<h2>Settings</h2>
			<form method="post">
			<input type="hidden" id="jstokenCSRF" name="tokenCSRF" value="'.$tokenCSRF.'">
			<div class="form-group">
				<label for="title">Site title</label>
				<input type="text" class="form-control" id="title" name="title" value="'.$title.'">
			</div>
			<button type="submit" class="btn btn-primary">Submit</button>
			</form>
		';
		return $html;
	}

	public function adminSidebar()
	{
		$pluginName = Text::lowercase(__CLASS__);
		$url = HTML_PATH_ADMIN_ROOT.'plugin/'.$pluginName;
		$html = '<a id="current-version" class="nav-link" href="'.$url.'">Custom Admin Form</a>';
		return $html;
	}
}
```

Вы можете скачать исходный код плагина:
- https://github.com/bludit/examples/tree/master/plugins/custom-controller-view-admin-panel