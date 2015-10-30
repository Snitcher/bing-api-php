bing-api-php
============

A modified version of the original package (scragg0x/bing-api-php) to work with the Bing web-only search API rather than the full search.

## Install

The recommended way is [through
composer](http://getcomposer.org). Just create a `composer.json` file and
run the `php composer.phar install` command to install it:

    {
        "require": {
            "snitcher/bing-api-php": "dev-master"
        }
    }

## API Reference

http://datamarket.azure.com/dataset/bing/search

## Example

```php
<?php

require_once __DIR__ . "/vendor/autoload.php";

use Bing\Client;

// You need to obtain a key
$key = '';

$c = new Client($key, 'json');

$res = $c->get('Web', ['Query' => 'Snitcher.com']);

$res = json_decode($res, true);

print_r($res);
```