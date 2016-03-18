Laravel UPS Api
=================

## For Laravel 5.1 & 5.2

[![Build Status](https://travis-ci.org/rooferz/Laravel-UPS-Api.svg?branch=master)](https://travis-ci.org/rooferz/Laravel-UPS-Api)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/rooferz/Laravel-UPS-Api/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/rooferz/Laravel-UPS-Api/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/rooferz/Laravel-UPS-Api/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/rooferz/Laravel-UPS-Api/?branch=master)
[![StyleCI](https://styleci.io/repos/54156171/shield)](https://styleci.io/repos/54156171)

Laravel UPS Api was created by, and is maintained by [Pierre Tondereau](https://github.com/rooferz), and PHP UPS Api was created by, and is maintained by [Gabriel Bull](https://github.com/gabrielbull) at [PHP UPS API](https://github.com/gabrielbull/php-ups-api). Feel free to check out the [change log](CHANGELOG.md), [releases](https://github.com/rooferz/Laravel-UPS-Api/releases), [license](LICENSE), and [contribution guidelines](CONTRIBUTING.md).

## Installation

Either [PHP](https://php.net) 5.5+ or [HHVM](http://hhvm.com) 3.6+ are required.

To get the latest version of Laravel UPS Api, simply require the project using [Composer](https://getcomposer.org):

```bash
$ composer require rooferz/laravel-ups-api
```

Instead, you may of course manually update your require block and run `composer update` if you so choose:

```json
{
    "require": {
        "rooferz/laravel-ups-api": "^1.0"
    }
}
```

Once Laravel UPS Api is installed, you need to register the service provider. Open up `config/app.php` and add the following to the `providers` key.

* `'Rooferz\LaravelUpsApi\UpsApiServiceProvider'`

You can register the all or some Ups facade in the `aliases` key of your `config/app.php` file if you like.

* `'UPSAddressValidator' => 'Rooferz\LaravelUpsApi\Facades\UpsAddressValidator'`
* `'UPSLocator' => 'Rooferz\LaravelUpsApi\Facades\UpsLocator'`
* `'UPSQuantumView' => 'Rooferz\LaravelUpsApi\Facades\UpsQuantumView'`
* `'UPSRate' => 'Rooferz\LaravelUpsApi\Facades\UpsRate'`
* `'UPSTimeInTransit' => 'Rooferz\LaravelUpsApi\Facades\UpsTimeInTransit'`
* `'UPSTracking' => 'Rooferz\LaravelUpsApi\Facades\UpsTracking'`
* `'UPSTradeability' => 'Rooferz\LaravelUpsApi\Facades\UpsTradeability'`


## Configuration

Laravel UPS Api requires connection configuration.

To get started, you'll need to publish all vendor assets:

```bash
$ php artisan vendor:publish --provider="Rooferz\LaravelUpsApi\UpsApiServiceProvider"
```

This will create a `config/ups.php` file in your app that you can modify to set your configuration. Also, make sure you check for changes to the original config file in this package between releases.

You also need to add env variables into your .env with your credentials:

```text
UPS_ACCESS_KEY=key
UPS_USER_ID=userId
UPS_PASSWORD=password
```

## Usage

This package only inject and provide Facades for each class of [PHP UPS API](https://github.com/gabrielbull/php-ups-api).
You just have read its documentation.


##### Further Information

There are other classes in this package that are not documented here. This is because they are not intended for public use and are used internally by this package.


## Security

If you discover a security vulnerability within this package, please send an e-mail to Pierre Tondereau at pierre@doers.fr. All security vulnerabilities will be promptly addressed.


## License

Laravel Ups Api is licensed under [The MIT License (MIT)](LICENSE).
