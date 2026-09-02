# OpenAPI\Client\ServiceAssignmentApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createServiceAssignment()**](ServiceAssignmentApi.md#createServiceAssignment) | **POST** /api/v1/service-assignments |  |
| [**deleteServiceAssignment()**](ServiceAssignmentApi.md#deleteServiceAssignment) | **DELETE** /api/v1/service-assignments/{id} |  |
| [**getServiceAssignment()**](ServiceAssignmentApi.md#getServiceAssignment) | **GET** /api/v1/service-assignments/{id} |  |
| [**getServiceAssignments()**](ServiceAssignmentApi.md#getServiceAssignments) | **GET** /api/v1/service-assignments/ |  |
| [**updateServiceAssignment()**](ServiceAssignmentApi.md#updateServiceAssignment) | **PUT** /api/v1/service-assignments/{id} |  |


## `createServiceAssignment()`

```php
createServiceAssignment($service_assignment_create): \OpenAPI\Client\Model\ServiceAssignment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ServiceAssignmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$service_assignment_create = new \OpenAPI\Client\Model\ServiceAssignmentCreate(); // \OpenAPI\Client\Model\ServiceAssignmentCreate

try {
    $result = $apiInstance->createServiceAssignment($service_assignment_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServiceAssignmentApi->createServiceAssignment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **service_assignment_create** | [**\OpenAPI\Client\Model\ServiceAssignmentCreate**](../Model/ServiceAssignmentCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ServiceAssignment**](../Model/ServiceAssignment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteServiceAssignment()`

```php
deleteServiceAssignment($id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ServiceAssignmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteServiceAssignment($id);
} catch (Exception $e) {
    echo 'Exception when calling ServiceAssignmentApi->deleteServiceAssignment: ', $e->getMessage(), PHP_EOL;
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

## `getServiceAssignment()`

```php
getServiceAssignment($id): \OpenAPI\Client\Model\ServiceAssignment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ServiceAssignmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getServiceAssignment($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServiceAssignmentApi->getServiceAssignment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ServiceAssignment**](../Model/ServiceAssignment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getServiceAssignments()`

```php
getServiceAssignments($page, $page_size, $search, $include_deleted): \OpenAPI\Client\Model\ServiceAssignment[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ServiceAssignmentApi(
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
    $result = $apiInstance->getServiceAssignments($page, $page_size, $search, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServiceAssignmentApi->getServiceAssignments: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\ServiceAssignment[]**](../Model/ServiceAssignment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateServiceAssignment()`

```php
updateServiceAssignment($id, $service_assignment_update): \OpenAPI\Client\Model\ServiceAssignment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ServiceAssignmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$service_assignment_update = new \OpenAPI\Client\Model\ServiceAssignmentUpdate(); // \OpenAPI\Client\Model\ServiceAssignmentUpdate

try {
    $result = $apiInstance->updateServiceAssignment($id, $service_assignment_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ServiceAssignmentApi->updateServiceAssignment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **service_assignment_update** | [**\OpenAPI\Client\Model\ServiceAssignmentUpdate**](../Model/ServiceAssignmentUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ServiceAssignment**](../Model/ServiceAssignment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
