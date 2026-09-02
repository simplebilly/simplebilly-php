# OpenAPI\Client\BankingApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bankLookupApi()**](BankingApi.md#bankLookupApi) | **GET** /api/v1/bookkeeping/banking/lookup |  |
| [**bankTransactionsApi()**](BankingApi.md#bankTransactionsApi) | **GET** /api/v1/bookkeeping/banking/transactions |  |
| [**hebesatzLookupApi()**](BankingApi.md#hebesatzLookupApi) | **GET** /api/v1/bookkeeping/hebesatz |  |


## `bankLookupApi()`

```php
bankLookupApi($iban): \OpenAPI\Client\Model\BankLookup
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$iban = 'iban_example'; // string

try {
    $result = $apiInstance->bankLookupApi($iban);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankingApi->bankLookupApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **iban** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\BankLookup**](../Model/BankLookup.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `bankTransactionsApi()`

```php
bankTransactionsApi()
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->bankTransactionsApi();
} catch (Exception $e) {
    echo 'Exception when calling BankingApi->bankTransactionsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `hebesatzLookupApi()`

```php
hebesatzLookupApi($gemeindeschluessel, $plz, $name, $stichtag, $country_code): \OpenAPI\Client\Model\HebesatzLookup[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BankingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gemeindeschluessel = 'gemeindeschluessel_example'; // string
$plz = 'plz_example'; // string
$name = 'name_example'; // string
$stichtag = 'stichtag_example'; // string | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from <= date <= valid_to.
$country_code = 'country_code_example'; // string

try {
    $result = $apiInstance->hebesatzLookupApi($gemeindeschluessel, $plz, $name, $stichtag, $country_code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BankingApi->hebesatzLookupApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gemeindeschluessel** | **string**|  | [optional] |
| **plz** | **string**|  | [optional] |
| **name** | **string**|  | [optional] |
| **stichtag** | **string**| Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from &lt;&#x3D; date &lt;&#x3D; valid_to. | [optional] |
| **country_code** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\HebesatzLookup[]**](../Model/HebesatzLookup.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
