# Основы разработчика
<!-- position: 1 -->

Давайте начнем с того, что проверим переменные установленной Bludit. Для этого мы перейдем в зону разработчика, которая находится по адресу `https://www.example.com/admin/developers`; Данный раздел недоступен напрямую из админ панели.

В этом разделе, вы можете увидеть подробную информацию об установленной Bludit и настройки вашей PHP.Например, глобальная переменная `$_SERVER`, загруженные дополнения, языковые пакет, константы Bludit и некоторые другие свойства объектов.

## Порядок загрузки файлов для админ панели
Эти файлы загружаются при входе в админ панель:

```
index.php
	bl-kernel/boot/init.php
	bl-kernel/boot/admin.php
		bl-kernel/boot/rules/60.plugins.php
		bl-kernel/boot/rules/69.pages.php
		bl-kernel/boot/rules/99.header.php
		bl-kernel/boot/rules/99.paginator.php
		bl-kernel/boot/rules/99.themes.php
		bl-kernel/boot/rules/99.security.php
		bl-kernel/admin/themes/default/init.php
		bl-kernel/admin/controllers/{CONTROLLER}.php
		bl-kernel/admin/themes/default/index.php
			bl-kernel/admin/controllers/{VIEW}.php
```

## Порядок загрузки файлов для сайта
Эти файлы загружаются при заходе на любую страницу сайта:

```
index.php
	bl-kernel/boot/init.php
	bl-kernel/boot/site.php
		bl-kernel/boot/rules/60.plugins.php
		bl-kernel/boot/rules/69.pages.php
		bl-kernel/boot/rules/99.header.php
		bl-kernel/boot/rules/99.paginator.php
		bl-kernel/boot/rules/99.themes.php
		bl-kernel/boot/rules/99.security.php
		bl-themes/{THEME_NAME}/init.php
		bl-themes/{THEME_NAME}/index.php
```

## Переменные и константы среды
Bludit вызывает переменные из заготовленных файлов.

- [bl-kernel/boot/init.php](https://github.com/bludit/bludit/blob/master/bl-kernel/boot/init.php)
- [bl-kernel/boot/variables.php](https://github.com/bludit/bludit/blob/master/bl-kernel/boot/variables.php)

Еще одно место, где вы можете посмотреть переменные среды `bl-kernel/boot/rules/`. Например, переменные `content` and `pages` определены и берутся из [bl-kernel/boot/rules/69.pages.php](https://github.com/bludit/bludit/blob/master/bl-kernel/boot/rules/69.pages.php).
