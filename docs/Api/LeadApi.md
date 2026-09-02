# OpenAPI\Client\LeadApi

Lead management. Required permissions: lead:read, lead:write, lead:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listLeadsApi()**](LeadApi.md#listLeadsApi) | **GET** /api/v1/support/leads |  |
| [**updateLeadApi()**](LeadApi.md#updateLeadApi) | **PUT** /api/v1/support/leads/{lead_id} |  |


## `listLeadsApi()`

```php
listLeadsApi($status, $source, $search, $page, $page_size): \OpenAPI\Client\Model\Lead[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LeadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = 'status_example'; // string
$source = 'source_example'; // string
$search = 'search_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->listLeadsApi($status, $source, $search, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeadApi->listLeadsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**|  | [optional] |
| **source** | **string**|  | [optional] |
| **search** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Lead[]**](../Model/Lead.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateLeadApi()`

```php
updateLeadApi($lead_id, $lead_update): \OpenAPI\Client\Model\Lead
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LeadApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$lead_id = 'lead_id_example'; // string
$lead_update = new \OpenAPI\Client\Model\LeadUpdate(); // \OpenAPI\Client\Model\LeadUpdate

try {
    $result = $apiInstance->updateLeadApi($lead_id, $lead_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LeadApi->updateLeadApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **lead_id** | **string**|  | |
| **lead_update** | [**\OpenAPI\Client\Model\LeadUpdate**](../Model/LeadUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Lead**](../Model/Lead.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
