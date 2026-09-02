# OpenAPI\Client\ListOpenItemsApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listOpenItemsApi()**](ListOpenItemsApi.md#listOpenItemsApi) | **GET** /api/v1/bookkeeping/open-items |  |


## `listOpenItemsApi()`

```php
listOpenItemsApi($reminder_level1_days, $reminder_level2_days, $reminder_level3_days, $customer_id): \OpenAPI\Client\Model\OpenItem[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ListOpenItemsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reminder_level1_days = 56; // int
$reminder_level2_days = 56; // int
$reminder_level3_days = 56; // int
$customer_id = 'customer_id_example'; // string

try {
    $result = $apiInstance->listOpenItemsApi($reminder_level1_days, $reminder_level2_days, $reminder_level3_days, $customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ListOpenItemsApi->listOpenItemsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reminder_level1_days** | **int**|  | [optional] |
| **reminder_level2_days** | **int**|  | [optional] |
| **reminder_level3_days** | **int**|  | [optional] |
| **customer_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\OpenItem[]**](../Model/OpenItem.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
