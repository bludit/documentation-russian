# Восстановление пароля
<!-- position: 4 -->

Вы можете восстановить пароль для пользователя `admin` используя скрипт `recovery.php`.

<h2 id="how-to-recover-the-password">Как изменить пароль</h2>

1. Скачайте файл[recovery.php](https://raw.githubusercontent.com/bludit/password-recovery-tool/master/recovery.php).
2. Загрузите файл `recovery.php` в каталог в котором находится Bludit.
3. Откройте данный скрипт в браузере: https://example.com/recovery.php, замените `example.com` на ваш домен.
4. Автоматически сгенерируется новый пароль для пользователя `admin` и будет отображен на открытой странице.
5. Войдите как пользователь `admin` с новым сгенерированным паролем.

Файл recovery.php должен будет удалиться автоматически, если этого не произошло, то удалите его вручную.

---

<h2 id="how-to-recover-the-password-via-command-line">Как восстановить пароль с помощью командной строки</h2>

Вы можете выполнить файл `recovery.php` из командной строки.

```
# Перейдите в директорию с установленным Bludit.
cd /var/html/bludit

# Скачайте файл
curl -o recovery.php https://raw.githubusercontent.com/bludit/password-recovery-tool/master/recovery.php

# Выполните команду
php recovery.php
```

```
Bludit Password Recovery Tool

Username: admin
New password: 00bef4566011d2015df2786dbd094003

>> The file recovery.php was deleted automatically for security reasons. <<
```