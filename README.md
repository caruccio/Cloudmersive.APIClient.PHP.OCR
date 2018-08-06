# cloudmersive_ocr_api_client
The powerful Optical Character Recognition (OCR) APIs let you convert scanned images of pages into recognized text.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: v1
- Package version: 1.3.9
- Build package: io.swagger.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/cloudmersive/cloudmersive_ocr_api_client.git"
    }
  ],
  "require": {
    "cloudmersive/cloudmersive_ocr_api_client": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/cloudmersive_ocr_api_client/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\ImageOcrApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$image_file = "/path/to/file.txt"; // \SplFileObject | Image file to perform OCR on.  Common file formats such as PNG, JPEG are supported.

try {
    $result = $apiInstance->imageOcrPost($image_file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImageOcrApi->imageOcrPost: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.cloudmersive.com*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*ImageOcrApi* | [**imageOcrPost**](docs/Api/ImageOcrApi.md#imageocrpost) | **POST** /ocr/image/toText | Converts an uploaded image in common formats such as JPEG, PNG into text via Optical Character Recognition.


## Documentation For Models

 - [ImageToTextResponse](docs/Model/ImageToTextResponse.md)


## Documentation For Authorization


## Apikey

- **Type**: API key
- **API key parameter name**: Apikey
- **Location**: HTTP header


## Author




