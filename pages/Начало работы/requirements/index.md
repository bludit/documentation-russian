# Требования
<!-- position: 2 -->

Вам нужен лишь сервер с поддержкой PHP.

- PHP v5.6 и выше.
- PHP [mbstring](https://www.php.net/manual/en/book.mbstring.php) модуль для полной поддержки UTF-8.
- PHP [gd](https://www.php.net/manual/en/book.image.php) модуль для обработки изображений.
- PHP [dom](https://www.php.net/manual/en/book.dom.php) модуль для управление DOM.
- PHP [json](https://www.php.net/manual/en/book.json.php) модуль для управления JSON.
- Bludit поддерживает все попоулярные сервера
  * [PHP Built-in web server](https://www.php.net/manual/en/features.commandline.webserver.php)
  * Nginx c модулем [ngx_http_rewrite_module](http://nginx.org/en/docs/http/ngx_http_rewrite_module.html)
  * Apache с модулем [mod_rewrite](http://httpd.apache.org/docs/current/mod/mod_rewrite.html)
  * Lighttpd с модулем [mod_rewrite](https://redmine.lighttpd.net/projects/1/wiki/docs_modrewrite)
  * Hiawatha, [rewrite rules](https://www.hiawatha-webserver.org/howto/url_rewrite_rules)
  * H2O, см. пост [H2O HTTP/2 web server and Bludit](https://forum.bludit.org/viewtopic.php?f=6&t=1015) на форуме поддержки.
  * IIS с модулем[URL Rewrite](https://www.iis.net/downloads/microsoft/url-rewrite), see [this](https://forum.bludit.org/viewtopic.php?f=6&t=1420) post in the Support Forum