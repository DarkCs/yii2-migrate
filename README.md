Yii2 Migrate
========================
Console Migration Command with multiple paths/aliases support

Installation
------------
The preferred way to install this extension is through [composer](http://getcomposer.org/download/).

```
php composer.phar require --prefer-dist "darkcs/yii2-migrate" "*"
```

Usage
-----
Add a new controller map in `controllerMap` section of your application's configuration file, for example:

```php
'controllerMap' => [
    'migrate' => [
        'class' => 'darkcs\migrate\controllers\MigrateController',
        'migrationPaths' => [
            '@modules/news/migrations',
            '@modules/page/migrations',
            ...
        ],
    ],
],
```
