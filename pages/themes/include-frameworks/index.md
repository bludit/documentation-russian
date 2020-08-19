# Подключение Framework's
<!-- position: 7 -->

Темы в Bludit очень гибкие, при создании вы можете использовать любой framework ([Bootstrap](http://getbootstrap.com/), [Foundation](https://foundation.zurb.com/), [Bulma](https://bulma.io), [UIkit](https://getuikit.com/), [Semantic UI](https://semantic-ui.com), и т.д.), любой JavaScript код. Все, что захотите!

Мы подключим несколько фреймворков в документации, но не стесняйтесь добавлять их больше, редактируя эту страницу.

<h2 id="jquery">Подключение jQuery</h2>

Bludit по стандарту имеет последнюю версию jQuery в своей сборке.
```
<?php
	echo Theme::jquery();
?>
```

HTML вывод
```
<script src="https://www.example.com/bl-kernel/js/jquery.min.js"></script>
```

<h2 id="bootstrap">Подключение Bootstrap</h2>

Bludit по стандарту имеет последнюю версию Bootstrap в своей сборке..

Подключеине JavaScript для Bootstrap.
```
<?php
	echo Theme::jsBootstrap();
?>
```

HTML вывод
```
<script src="https://www.example.com/bl-kernel/js/bootstrap.bundle.min.js"></script>
```

Подключение CSS для Bootstrap.
```
<?php
	echo Theme::cssBootstrap();
?>
```

HTML вывод
```
<link rel="stylesheet" type="text/css" href="https://www.example.com/bl-kernel/css/bootstrap.min.css">
```

<h2 id="uikit">Подключеине UIkit</h2>

Этот framework, к сожалению, не входит в сборку Bludit. Однако, при желании, вы можете подключить, используя методы `Theme::css()` и `Theme::js()`. Можно использовать UIkit CDN или скачать файлы framework'a.

Слудущий пример подключает UIkit из UIkitCDN. Обратите внимание на `false`, это говорит методу, что мы используем внешний файл.
```
<?php
	echo Theme::css('https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/css/uikit.min.css', false);

	echo Theme::js('https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/js/uikit.min.js', false);
	echo Theme::js('https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/js/uikit-icons.min.js', false);
?>
```

HTML вывод
```
<link rel="stylesheet" type="text/css" href="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/css/uikit.min.css">

<script src="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/js/uikit.min.js"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/uikit/3.0.0-rc.26/js/uikit-icons.min.js"></script>