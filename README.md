# Constant Contact PHP SDK

## About

The original project appears to be abandoned. This is our solution to get some of the dependencies upgraded to more usable versions. We have only upgraded the methods that we use, it is possible we have not upgraded the methods you use. Please feel free to upgrade any methods we have not and provide a pull request.

Original project is [located here](https://github.com/constantcontact/php-sdk).

### This library utilizes [Guzzle 6](http://guzzle.readthedocs.org/)

## Installing via Composer
[Composer](https://getcomposer.org/) is a dependency management tool for PHP that allows you to declare the dependencies your project needs and installs them into your project. In order to use the Constant Contact PHP SDK through composer, you must add "constantcontact/constantcontact" as a dependency in your project's composer.json file.
```javascript
 "repositories": [
         {
             "type": "vcs",
             "url": "git@bitbucket.org:sitecrafting/constant-contact-sdk.git"
         }
     ],
     "require": {
         "sitecrafting/constant-contact-sdk": "dev-master"
     }
```


### Manual Installation
If you are unable to install using composer, we have provided a zip file that includes a version of the dependencies at the time of our release, as well as our library. Unzip the vendor file in the standalone directory, and require the autoload.php file to use our methods.

## Documentation

The source documentation is hosted at http://constantcontact.github.io/php-sdk

API Documentation is located at http://developer.constantcontact.com/docs/developer-guides/api-documentation-index.html

## Usage
The ConstantContact class contains the underlying services that hold the methods that use the API.
```php
use Ctct\ConstantContact;
$cc = new ConstantContact('your api key');

$contacts = $cc->contactService->getContacts('your access token')
```

Many methods will take an array of parameters for use in the calls. Available params are documented in the PHPDoc of the method.
```php
$params = array("limit" => 500);
$contacts = $cc->contactService->getContacts('your access token', $params);
```
## Minimum Requirements
Use of this library requires PHP 5.5+
