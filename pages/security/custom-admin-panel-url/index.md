# Пользовательский URL админ панели
<!-- position: 3 -->

По умолчанию, админ панель находится в папке `/admin/`.

Вы можете изменить адрес в переменных - `/bl-kernel/boot/variables.php`. Измените значение`ADMIN_URI_FILTER`  на ваш адрес.

<pre><code data-language="php">define('ADMIN_URI_FILTER', 'admin');</code></pre>