# Страницы после создания
<!-- position: 5 -->

После создания страницы, Bludit вызывает Hook `afterPageCreate`. Этот Hook также вызывается для запланированых страниц.

<div class="note">
Эта функция доступна начиная с Bludit v3.13
</div>

## Пример: Добавить строку к заголовку
Следующий плагин добавляет строку в начале страницы после ее создания.

```php
<?php

class TitleAppender extends Plugin {

	public function afterPageCreate($key)
	{
		$page = new Page($key);
		$currentTitle = $page->title();
		$newTitle = 'Summer: '.$currentTitle;

		global $pages;
		$pages->edit(array(
				'key'=>$key,
				'title'=>$newTitle
		));
	}

}

?>
```

Вы можете скачать исходный код плагина:
- https://github.com/bludit/examples