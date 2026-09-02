# OpenAPI\Client\SuitabilityApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**shippingSuitabilityApi()**](SuitabilityApi.md#shippingSuitabilityApi) | **POST** /api/v1/shipping/suitability |  |


## `shippingSuitabilityApi()`

```php
shippingSuitabilityApi($suitability_request): \OpenAPI\Client\Model\SuitabilityResult
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SuitabilityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$suitability_request = new \OpenAPI\Client\Model\SuitabilityRequest(); // \OpenAPI\Client\Model\SuitabilityRequest

try {
    $result = $apiInstance->shippingSuitabilityApi($suitability_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SuitabilityApi->shippingSuitabilityApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **suitability_request** | [**\OpenAPI\Client\Model\SuitabilityRequest**](../Model/SuitabilityRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SuitabilityResult**](../Model/SuitabilityResult.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
