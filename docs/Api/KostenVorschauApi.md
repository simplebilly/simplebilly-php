# OpenAPI\Client\KostenVorschauApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**kostenVorschauApi()**](KostenVorschauApi.md#kostenVorschauApi) | **GET** /api/v1/bookkeeping/kosten-vorschau |  |


## `kostenVorschauApi()`

```php
kostenVorschauApi($year, $month): \OpenAPI\Client\Model\KostenVorschau
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\KostenVorschauApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$month = 56; // int

try {
    $result = $apiInstance->kostenVorschauApi($year, $month);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KostenVorschauApi->kostenVorschauApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |
| **month** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\KostenVorschau**](../Model/KostenVorschau.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
