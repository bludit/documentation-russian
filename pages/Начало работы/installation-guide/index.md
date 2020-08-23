# Процесс установки
<!-- position: 3 -->

<h2 id="installation-from-zip-file">Установка из zip-архива</h2>

1. Скачайте последнюю версию Bludit с [официального сайта](https://www.bludit.com).
2. Распакуйте zip-архив.
3. Загрузите содержимое папки разархивированного архива к себе на сервер или хостинг. Вы можете загрузить содержимое в корневой каталог или подкаталог, например `/bludit/`.
4. Для загрузки, вы можете использовать любой FTP клиент. Например, File Zilla.
4. Зайдите на сайт по своему адресу. Если вы загрузили файлы в корневой католог - `https://www.example.com`, если вы загрузили файлы в подкаталог - `https://www.example.com/bludit/`.
5. Следуйте инструкции установщика для дальнейшей настройки и установки Bludit.

---

<h2 id="php-built-in-web-server">PHP Built-in web server</h2>

Вы можете быстро установить Bludit с помощью комманд [PHP Built-in web server](https://www.php.net/manual/en/features.commandline.webserver.php).

```
$ git clone https://github.com/bludit/bludit.git
$ cd bludit
$ php -S localhost:8000
```

После выполнения команд перейдите по ссылке `http://localhost:8000`

---

<h2 id="docker">Docker</h2>
Установка из [Docker Image](https://hub.docker.com/r/bludit/docker/).

```
$ docker run --name bludit -p 8000:80 -d bludit/docker:latest
```

После выполнения команды перейдите по ссылке `http://localhost:8000`

---

<h2 id="vagrant">Vagrant</h2>
Установка из [Vagrant Build](https://pilab.dev/bludit-vagrant).

```
$ git clone https://github.com/mhancoc7/Bludit-Vagrant.git
$ cd Bludit-Vagrant
$ vagrant up
```

После выполнения команд перейдите по ссылке `http://localhost:8080`
