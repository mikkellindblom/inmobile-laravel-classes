# Inmobile API laravel classes

Simple classes for the inmobile.dk SMS API

## Usage

Register classes:

```php
use App\Classes\SimpleXMLExtended;
use App\Classes\MM_Connector;
use App\Classes\MM_Message;
use App\Classes\MM_Premium_Message;
```

Connect to the API: 

```php
$MM_Connector = new MM_Connector(
    'YOUR-API-KEY',
    'https://mm.inmobile.dk'
);
```

Send something: 

```php
$MM_Connector->addMessage(
    new MM_Message(request('text'), array(request('to')), request('from'))
);
```