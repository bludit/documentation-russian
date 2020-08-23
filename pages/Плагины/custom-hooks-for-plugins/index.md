# Пользовательские Hook'и для плагинов
<!-- position: 4 -->

Bludit поддерживает пользовательские Hook'и, вы можете создать собственный Hook.

<div class="note">
Эта функция доступна начиная с Bludit v3.13
</div>

## Пример
В следущем примере создаются два пользовательски hook'a `select` и `insert`.

Чтобы плагин начала работать, не забудьте указать их внутри массива `$this->customHooks` внутри метода `init()`.

```php
<?php

class MyHooks extends Plugin {

	public function init()
	{
        $this->customHooks = array(
            'select',
            'insert'
        );
	}

	public function select()
	{
		echo 'Custom hook select';
	}

	public function insert()
	{
		echo 'Custom hook insert';
	}
}

?>
```

После активации плагина, вы можете вызывать Hook'и как обычно `Theme::plugins`.

```php
<?php
	...
	Theme::plugins('select');
	...
	Theme::plugins('insert');
?>
```