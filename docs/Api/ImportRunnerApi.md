# OpenAPI\Client\ImportRunnerApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getImportStatus()**](ImportRunnerApi.md#getImportStatus) | **GET** /api/v1/import/{job_id} |  |
| [**startImport()**](ImportRunnerApi.md#startImport) | **POST** /api/v1/import/start |  |
| [**testImportConnection()**](ImportRunnerApi.md#testImportConnection) | **POST** /api/v1/import/test |  |


## `getImportStatus()`

```php
getImportStatus($job_id): \OpenAPI\Client\Model\ImportJobStatus
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ImportRunnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$job_id = 'job_id_example'; // string

try {
    $result = $apiInstance->getImportStatus($job_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportRunnerApi->getImportStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **job_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ImportJobStatus**](../Model/ImportJobStatus.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `startImport()`

```php
startImport($import_start_request): \OpenAPI\Client\Model\ImportStartResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ImportRunnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_start_request = new \OpenAPI\Client\Model\ImportStartRequest(); // \OpenAPI\Client\Model\ImportStartRequest

try {
    $result = $apiInstance->startImport($import_start_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportRunnerApi->startImport: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_start_request** | [**\OpenAPI\Client\Model\ImportStartRequest**](../Model/ImportStartRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ImportStartResponse**](../Model/ImportStartResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `testImportConnection()`

```php
testImportConnection($import_test_request): \OpenAPI\Client\Model\ImportTestResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ImportRunnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$import_test_request = new \OpenAPI\Client\Model\ImportTestRequest(); // \OpenAPI\Client\Model\ImportTestRequest

try {
    $result = $apiInstance->testImportConnection($import_test_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ImportRunnerApi->testImportConnection: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **import_test_request** | [**\OpenAPI\Client\Model\ImportTestRequest**](../Model/ImportTestRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ImportTestResponse**](../Model/ImportTestResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
