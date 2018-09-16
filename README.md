### Документация к [W3BS][root_url] – Официальной платформы с элементами социальной сети

[![license](https://img.shields.io/npm/l/steam-user.svg)](https://github.com/w3bsme/lazy-site/blob/master/LICENSE)
[![Build Status](https://travis-ci.org/telegramdesktop/tdesktop.svg?branch=dev)](https://travis-ci.org/telegramdesktop/tdesktop)
[![Build status](https://ci.appveyor.com/api/projects/status/uiw2y768iy4i5bu8/branch/dev?svg=true)](https://ci.appveyor.com/project/telegramdesktop/tdesktop)

![preview][preview]

### Небходимые требования к ПО

* `HTTP` Apache-PHP-7.2/x64 или выше
* `PHP` PHP-7.2/x64 или выше
* `MySQL / MariaDB` MySQL-5.7/x64 или выше

---

### Содержание
- [Настройки платформы на серверной стороне](#Настройки-платформы-на-серверной-стороне-)
    - [Константы](#Константы-)
- [PHP сессии](#php-сессии-)
- [API](#api-)
    - [API методы](#Методы-)

---

### Настройки платформы на серверной стороне [^](#Содержание)

#### Константы [^](#Настройки-платформы-на-серверной-стороне-)
* `DEBUG` — Debug mode
* `EXPIRE_KEY` — Секунды истечения срока действия пользовательской сессии
* `NO_ACCESS_LOCATION` — Расположение, если доступ запрещен
* `MYSQLI_SERVER` — Сервер для подключения к MySQLi
* `MYSQLI_LOGIN` — Имя пользователя для подключения к MySQLi
* `MYSQLI_PASSWORD` — Пароль для подключения к MySQLi
* `MYSQLI_DATABASE` — Имя базы данных для подключения к MySQLi
* `CURRENT_VERSION` — Версия платформы
* `ROOT_DOMAIN` — Корневой домен платформы

### PHP сессии [^](#mysqli-сервер-)

Старт новой сессии, либо возобновление существующей:
**не стоит использовать**
```php
<?=PHPSession::PHPSession_Start();?>
```
чтобы начинать новую сессию или же возраждать существующую сессию, **всегда** необходимо вызывать
```php
<?=PHPSession::PHPSession_GetInstance();?>
```

### API [^](#api-)

Платформа обрабатывает пользовательские запросы через собственный набор  API-методов взаимодействия с ней

#### Методы [^](#Методы-)
* `Auth.login` — Авторизация
* `Auth.logout` — Закончить активную сессию пользователя
* `User.getSex` — Получить пол пользователя
* `User.getOnline` — Получить дату последнего входа пользователя на сайт
* `Account.Freeze` — Временная заморозка собственного аккаунта в случае его взлома
* `Account.getJoinDate` — Получить дату собственной регистрации
* `Account.getBalance` — Получить данные баланса собственного аккаунта


[//]: # (LINKS)
[root_url]: https://t.me/w3bsme
[preview]: https://raw.githubusercontent.com/w3bsme/social_engine/master/preview.jpg
