# OpenAPI\Client\ProposeAssignmentsApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**proposeAssignmentsApi()**](ProposeAssignmentsApi.md#proposeAssignmentsApi) | **GET** /api/v1/bookkeeping/propose-assignments |  |


## `proposeAssignmentsApi()`

```php
proposeAssignmentsApi($min_confidence, $customer_id): \OpenAPI\Client\Model\ProposedAssignment[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProposeAssignmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$min_confidence = 3.4; // float
$customer_id = 'customer_id_example'; // string

try {
    $result = $apiInstance->proposeAssignmentsApi($min_confidence, $customer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProposeAssignmentsApi->proposeAssignmentsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **min_confidence** | **float**|  | [optional] |
| **customer_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProposedAssignment[]**](../Model/ProposedAssignment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
