EasyAdmin + Mercure Demo Application
====================================

This project is a demo showcasing the integration of [Mercure protocol][1] into [EasyAdmin][2]

Features
--------

  * While I edit an entity which gets updated on the server by another user, I get a notification and a button for updating the page I'm looking at
  * While I am looking at an entity list, if a an entity on the page gets updated on the server by another user, I get a notification, a button for updating the page I'm looking at and the outdated entity gets highlighted


Requirements
------------

  * [Mercure Server][1]
  * PHP 8.1 or higher;
  * PDO-SQLite PHP extension enabled;
  * and the [usual Symfony application requirements][3].

Installation
------------

Make sure you have access to a Mercure server ([Install and Configure](https://mercure.rocks/docs/hub/install))

Clone this repo

```bash
$ git clone https://github.com/slim/easyadmin-mercure-demo.git
```

Install with [Composer][4]:

```bash
$ cd easyadmin-mercure-demo
$ composer install
```

Create the database

```bash
$ php bin/console doctrine:schema:create
```

Require mercure bundle in the project to activate mercure support:

```bash
$ composer require mercure
```

Update your .env with adequate [MERCURE variable values](https://symfony.com/doc/current/mercure.html#configuration)

That's it!


Usage
-----

There's no need to configure anything to run the application. If you have
[installed Symfony CLI][5], run this command:

```bash
$ cd easyadmin-mercure-demo
$ symfony serve
```

Then access the application in your browser at the given URL (<https://localhost:8000> by default).

If you don't have the Symfony binary installed, run `php -S localhost:8000 -t public/`
to use the built-in PHP web server or [configure a web server][6] like Nginx or
Apache to run the application.

[1]: https://mercure.rocks
[2]: https://github.com/EasyCorp/EasyAdminBundle
[3]: https://symfony.com
[4]: https://getcomposer.org
[5]: https://symfony.com/download
[6]: https://symfony.com/doc/current/cookbook/configuration/web_server_configuration.html
