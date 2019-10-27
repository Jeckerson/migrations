# Phalcon Migrations

Generate or migrate database changes via migrations.

## Requirements

* PHP >= 7.2
* Phalcon >= 4.0.0.rc-2
* PHP ext-posix

## Installing via Composer

```
composer require --dev phalcon/migrations
```

## Usage

```
use Phalcon\Migrations\Migrations;

$migration = new Migrations();
$migration::run([
    'migrationsDir' => [
        __DIR__ . '/migrations',
    ],
    'config' => [
        'database' => [
            'adapter' => 'Mysql',
            'host' => 'phalcon-db-mysql',
            'username' => 'root',
            'password' => 'root',
            'dbname' => 'vokuro',
        ],
    ]
]);
```
