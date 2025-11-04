# OpenAPIClient-php

This SDK provides a PHP client for the Ubiqfy API, allowing developers to integrate mobile product offerings, handle transactions, and access international services seamlessly.

## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/):

```bash
composer require flipeaz342/ubiqfy-php-sdk
```

Or, add the following to `composer.json`:

```json
{
  "require": {
    "flipeaz342/ubiqfy-php-sdk": "^1.0"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');




$apiInstance = new OpenAPI\Client\Api\PartnersAPIApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$request = new \OpenAPI\Client\Model\AuthenticateRequest(); // \OpenAPI\Client\Model\AuthenticateRequest

try {
    $result = $apiInstance->partnersAPIAuthenticate($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PartnersAPIApi->partnersAPIAuthenticate: ', $e->getMessage(), PHP_EOL;
}

```

## API Endpoints

All URIs are relative to *https://api.ubiqfy.com*

| Class            | Method                                                                                                                        | HTTP request                                 | Description |
| ---------------- | ----------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------- | ----------- |
| _PartnersAPIApi_ | [**partnersAPIAuthenticate**](docs/Api/PartnersAPIApi.md#partnersapiauthenticate)                                             | **POST** /Authenticate                       |
| _PartnersAPIApi_ | [**partnersAPICancelTransaction**](docs/Api/PartnersAPIApi.md#partnersapicanceltransaction)                                   | **POST** /CancelTransaction                  |
| _PartnersAPIApi_ | [**partnersAPIDoCalculateEstimatePrice**](docs/Api/PartnersAPIApi.md#partnersapidocalculateestimateprice)                     | **POST** /DoCalculateEstimatePrice           |
| _PartnersAPIApi_ | [**partnersAPIDoTransaction**](docs/Api/PartnersAPIApi.md#partnersapidotransaction)                                           | **POST** /DoTransaction                      |
| _PartnersAPIApi_ | [**partnersAPIGetAvailableProduct**](docs/Api/PartnersAPIApi.md#partnersapigetavailableproduct)                               | **POST** /GetAvailableProduct                |
| _PartnersAPIApi_ | [**partnersAPIGetAvailableProductByCode**](docs/Api/PartnersAPIApi.md#partnersapigetavailableproductbycode)                   | **POST** /GetAvailableProductByCode          |
| _PartnersAPIApi_ | [**partnersAPIGetAvailableProductOptionByCode**](docs/Api/PartnersAPIApi.md#partnersapigetavailableproductoptionbycode)       | **POST** /GetAvailableProductOptionByCode    |
| _PartnersAPIApi_ | [**partnersAPIGetAvailableProductTypes**](docs/Api/PartnersAPIApi.md#partnersapigetavailableproducttypes)                     | **POST** /GetAvailableProductTypes           |
| _PartnersAPIApi_ | [**partnersAPIGetCountries**](docs/Api/PartnersAPIApi.md#partnersapigetcountries)                                             | **POST** /GetCountries                       |
| _PartnersAPIApi_ | [**partnersAPIGetInternationalMobileProducts**](docs/Api/PartnersAPIApi.md#partnersapigetinternationalmobileproducts)         | **POST** /GetInternationalMobileProducts     |
| _PartnersAPIApi_ | [**partnersAPIGetInternationalOperators**](docs/Api/PartnersAPIApi.md#partnersapigetinternationaloperators)                   | **POST** /GetInternationalOperators          |
| _PartnersAPIApi_ | [**partnersAPIGetInternationalPhoneNumberOptions**](docs/Api/PartnersAPIApi.md#partnersapigetinternationalphonenumberoptions) | **POST** /GetInternationalPhoneNumberOptions |
| _PartnersAPIApi_ | [**partnersAPIGetProductOptionPhoneNumber**](docs/Api/PartnersAPIApi.md#partnersapigetproductoptionphonenumber)               | **POST** /GetProductOptionPhoneNumber        |
| _PartnersAPIApi_ | [**partnersAPIGetTransaction**](docs/Api/PartnersAPIApi.md#partnersapigettransaction)                                         | **POST** /GetTransaction                     |

## Models

- [APICancelTransactionRequest](docs/Model/APICancelTransactionRequest.md)
- [APICancelTransactionResponse](docs/Model/APICancelTransactionResponse.md)
- [ApplyPaymentResultData](docs/Model/ApplyPaymentResultData.md)
- [ApplyTransactionRequest](docs/Model/ApplyTransactionRequest.md)
- [ApplyTransactionResponse](docs/Model/ApplyTransactionResponse.md)
- [AuthenticateRequest](docs/Model/AuthenticateRequest.md)
- [AuthenticateResponse](docs/Model/AuthenticateResponse.md)
- [AvailableCountries](docs/Model/AvailableCountries.md)
- [AvailableCountriesRequest](docs/Model/AvailableCountriesRequest.md)
- [AvailableCountriesResponse](docs/Model/AvailableCountriesResponse.md)
- [AvailableInternationalMobileProduct](docs/Model/AvailableInternationalMobileProduct.md)
- [AvailableInternationalMobileProductsRequest](docs/Model/AvailableInternationalMobileProductsRequest.md)
- [AvailableInternationalMobileProductsResponse](docs/Model/AvailableInternationalMobileProductsResponse.md)
- [AvailableInternationalOperator](docs/Model/AvailableInternationalOperator.md)
- [AvailableInternationalOperatorsRequest](docs/Model/AvailableInternationalOperatorsRequest.md)
- [AvailableInternationalOperatorsResponse](docs/Model/AvailableInternationalOperatorsResponse.md)
- [AvailableProduct](docs/Model/AvailableProduct.md)
- [AvailableProductOption](docs/Model/AvailableProductOption.md)
- [AvailableProductOptionByCodeRequest](docs/Model/AvailableProductOptionByCodeRequest.md)
- [AvailableProductOptionByCodeResponse](docs/Model/AvailableProductOptionByCodeResponse.md)
- [AvailableProductOptionRequest](docs/Model/AvailableProductOptionRequest.md)
- [AvailableProductOptionResponse](docs/Model/AvailableProductOptionResponse.md)
- [AvailableProductOptions](docs/Model/AvailableProductOptions.md)
- [AvailableProductRequest](docs/Model/AvailableProductRequest.md)
- [AvailableProductResponse](docs/Model/AvailableProductResponse.md)
- [AvailableProductTypes](docs/Model/AvailableProductTypes.md)
- [AvailableProductTypesRequest](docs/Model/AvailableProductTypesRequest.md)
- [AvailableProductTypesResponse](docs/Model/AvailableProductTypesResponse.md)
- [AvailableProducts](docs/Model/AvailableProducts.md)
- [AvailableProductsRequest](docs/Model/AvailableProductsRequest.md)
- [AvailableProductsResponse](docs/Model/AvailableProductsResponse.md)
- [CalculateEstimatePriceRequest](docs/Model/CalculateEstimatePriceRequest.md)
- [CalculateEstimatePriceResponse](docs/Model/CalculateEstimatePriceResponse.md)
- [Country](docs/Model/Country.md)
- [EzeTopCalculateError](docs/Model/EzeTopCalculateError.md)
- [EzeTopCalculateEstimatePrices](docs/Model/EzeTopCalculateEstimatePrices.md)
- [EzeTopCalculateEstimatedPrice](docs/Model/EzeTopCalculateEstimatedPrice.md)
- [EzeTopCalculatePrice](docs/Model/EzeTopCalculatePrice.md)
- [EzeTopError](docs/Model/EzeTopError.md)
- [EzeTopGetProductsResponse](docs/Model/EzeTopGetProductsResponse.md)
- [EzeTopInternationalDialingInformation](docs/Model/EzeTopInternationalDialingInformation.md)
- [EzeTopPrice](docs/Model/EzeTopPrice.md)
- [EzeTopProduct](docs/Model/EzeTopProduct.md)
- [EzeTopSetting](docs/Model/EzeTopSetting.md)
- [EzeTopSettingDefinition](docs/Model/EzeTopSettingDefinition.md)
- [GetInternationalPhoneNumberOptionsRequest](docs/Model/GetInternationalPhoneNumberOptionsRequest.md)
- [GetInternationalPhoneNumberOptionsResponse](docs/Model/GetInternationalPhoneNumberOptionsResponse.md)
- [GetTransactionRequest](docs/Model/GetTransactionRequest.md)
- [GetTransactionResponse](docs/Model/GetTransactionResponse.md)
- [MandatoryFields](docs/Model/MandatoryFields.md)
- [MinMaxFaceRangeValue](docs/Model/MinMaxFaceRangeValue.md)
- [MinMaxRangeValue](docs/Model/MinMaxRangeValue.md)
- [TransationData](docs/Model/TransationData.md)
- [VisibleFields](docs/Model/VisibleFields.md)

## Authorization

Endpoints do not require authorization.

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author

## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `v1`
  - Generator version: `7.17.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
