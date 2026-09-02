# OpenAPI\Client\KstApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**kstApi()**](KstApi.md#kstApi) | **GET** /api/v1/bookkeeping/kst |  |


## `kstApi()`

```php
kstApi($year, $gewinn): \OpenAPI\Client\Model\KstErgebnis
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\KstApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$gewinn = 'gewinn_example'; // string

try {
    $result = $apiInstance->kstApi($year, $gewinn);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KstApi->kstApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |
| **gewinn** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\KstErgebnis**](../Model/KstErgebnis.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
