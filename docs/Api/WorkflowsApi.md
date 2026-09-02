# OpenAPI\Client\WorkflowsApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listWorkflowsApi()**](WorkflowsApi.md#listWorkflowsApi) | **GET** /api/v1/workflows |  |
| [**setWorkflowEnabledApi()**](WorkflowsApi.md#setWorkflowEnabledApi) | **PUT** /api/v1/workflows/{workflow_id}/enabled |  |


## `listWorkflowsApi()`

```php
listWorkflowsApi(): \OpenAPI\Client\Model\Workflow[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkflowsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listWorkflowsApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowsApi->listWorkflowsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\Workflow[]**](../Model/Workflow.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setWorkflowEnabledApi()`

```php
setWorkflowEnabledApi($workflow_id, $workflow_enabled_update): \OpenAPI\Client\Model\Workflow
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WorkflowsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$workflow_id = 'workflow_id_example'; // string
$workflow_enabled_update = new \OpenAPI\Client\Model\WorkflowEnabledUpdate(); // \OpenAPI\Client\Model\WorkflowEnabledUpdate

try {
    $result = $apiInstance->setWorkflowEnabledApi($workflow_id, $workflow_enabled_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WorkflowsApi->setWorkflowEnabledApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **workflow_id** | **string**|  | |
| **workflow_enabled_update** | [**\OpenAPI\Client\Model\WorkflowEnabledUpdate**](../Model/WorkflowEnabledUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Workflow**](../Model/Workflow.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
