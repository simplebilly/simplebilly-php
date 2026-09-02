# OpenAPI\Client\PlausibilityApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**plausibilityCheckApi()**](PlausibilityApi.md#plausibilityCheckApi) | **GET** /api/v1/bookkeeping/plausibility |  |


## `plausibilityCheckApi()`

```php
plausibilityCheckApi($date_from, $date_to): \OpenAPI\Client\Model\PlausibilityReport
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PlausibilityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$date_from = 'date_from_example'; // string
$date_to = 'date_to_example'; // string

try {
    $result = $apiInstance->plausibilityCheckApi($date_from, $date_to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PlausibilityApi->plausibilityCheckApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **date_from** | **string**|  | [optional] |
| **date_to** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PlausibilityReport**](../Model/PlausibilityReport.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
