# OpenAPI\Client\UstvaApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**jahresustApi()**](UstvaApi.md#jahresustApi) | **GET** /api/v1/bookkeeping/jahresust |  |
| [**ustvaApi()**](UstvaApi.md#ustvaApi) | **GET** /api/v1/bookkeeping/ustva |  |


## `jahresustApi()`

```php
jahresustApi($year): \OpenAPI\Client\Model\JahresUstErgebnis
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UstvaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int

try {
    $result = $apiInstance->jahresustApi($year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UstvaApi->jahresustApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\JahresUstErgebnis**](../Model/JahresUstErgebnis.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `ustvaApi()`

```php
ustvaApi($zeitraum): \OpenAPI\Client\Model\UstvaErgebnis
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\UstvaApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$zeitraum = 'zeitraum_example'; // string

try {
    $result = $apiInstance->ustvaApi($zeitraum);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UstvaApi->ustvaApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **zeitraum** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\UstvaErgebnis**](../Model/UstvaErgebnis.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
