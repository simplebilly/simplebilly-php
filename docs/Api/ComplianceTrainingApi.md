# OpenAPI\Client\ComplianceTrainingApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createComplianceTraining()**](ComplianceTrainingApi.md#createComplianceTraining) | **POST** /api/v1/compliance-trainings |  |
| [**deleteComplianceTraining()**](ComplianceTrainingApi.md#deleteComplianceTraining) | **DELETE** /api/v1/compliance-trainings/{id} |  |
| [**getComplianceTraining()**](ComplianceTrainingApi.md#getComplianceTraining) | **GET** /api/v1/compliance-trainings/{id} |  |
| [**getComplianceTrainings()**](ComplianceTrainingApi.md#getComplianceTrainings) | **GET** /api/v1/compliance-trainings/ |  |
| [**updateComplianceTraining()**](ComplianceTrainingApi.md#updateComplianceTraining) | **PUT** /api/v1/compliance-trainings/{id} |  |


## `createComplianceTraining()`

```php
createComplianceTraining($compliance_training_create): \OpenAPI\Client\Model\ComplianceTraining
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ComplianceTrainingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$compliance_training_create = new \OpenAPI\Client\Model\ComplianceTrainingCreate(); // \OpenAPI\Client\Model\ComplianceTrainingCreate

try {
    $result = $apiInstance->createComplianceTraining($compliance_training_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ComplianceTrainingApi->createComplianceTraining: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **compliance_training_create** | [**\OpenAPI\Client\Model\ComplianceTrainingCreate**](../Model/ComplianceTrainingCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ComplianceTraining**](../Model/ComplianceTraining.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteComplianceTraining()`

```php
deleteComplianceTraining($id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ComplianceTrainingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteComplianceTraining($id);
} catch (Exception $e) {
    echo 'Exception when calling ComplianceTrainingApi->deleteComplianceTraining: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getComplianceTraining()`

```php
getComplianceTraining($id): \OpenAPI\Client\Model\ComplianceTraining
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ComplianceTrainingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getComplianceTraining($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ComplianceTrainingApi->getComplianceTraining: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ComplianceTraining**](../Model/ComplianceTraining.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getComplianceTrainings()`

```php
getComplianceTrainings($page, $page_size, $search, $include_deleted): \OpenAPI\Client\Model\ComplianceTraining[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ComplianceTrainingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$page_size = 56; // int
$search = 'search_example'; // string
$include_deleted = True; // bool | Soft-delete entities: set true to include rows with `deleted_at` set.

try {
    $result = $apiInstance->getComplianceTrainings($page, $page_size, $search, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ComplianceTrainingApi->getComplianceTrainings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **search** | **string**|  | [optional] |
| **include_deleted** | **bool**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] |

### Return type

[**\OpenAPI\Client\Model\ComplianceTraining[]**](../Model/ComplianceTraining.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateComplianceTraining()`

```php
updateComplianceTraining($id, $compliance_training_update): \OpenAPI\Client\Model\ComplianceTraining
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ComplianceTrainingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$compliance_training_update = new \OpenAPI\Client\Model\ComplianceTrainingUpdate(); // \OpenAPI\Client\Model\ComplianceTrainingUpdate

try {
    $result = $apiInstance->updateComplianceTraining($id, $compliance_training_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ComplianceTrainingApi->updateComplianceTraining: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **compliance_training_update** | [**\OpenAPI\Client\Model\ComplianceTrainingUpdate**](../Model/ComplianceTrainingUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ComplianceTraining**](../Model/ComplianceTraining.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
