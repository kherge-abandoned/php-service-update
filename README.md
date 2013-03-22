Phar Update Service
===================

[![Build Status](https://travis-ci.org/herrera-io/php-service-update.png?branch=master)](https://travis-ci.org/herrera-io/php-service-update)

A service provider for the Phar Update library.

Summary
-------

Integrates the [Phar Update](https://github.com/herrera-io/php-phar-update) library into the [Herrera.io service container](https://github.com/herrera-io/php-service-container).

Installation
------------

Add it to your list of Composer dependencies:

```sh
$ composer require herrera-io/service-update=1.*
```

Usage
-----

```php
<?php

use Herrera\Service\Container;
use Herrera\Service\Update\UpdateServiceProvider;

$container = new Container();
$container->register(new UpdateServiceProvider(), array(
    'update.url' => 'https://example.com/manifest.json'
));

$container['update']('1.0.0'); // 1.0.0 is the current version
```