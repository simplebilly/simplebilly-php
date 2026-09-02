# OpenAPI\Client\InventoryCountApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createInventoryCount()**](InventoryCountApi.md#createInventoryCount) | **POST** /api/v1/inventory-counts |  |
| [**deleteInventoryCount()**](InventoryCountApi.md#deleteInventoryCount) | **DELETE** /api/v1/inventory-counts/{inventory_count_id} |  |
| [**generateInventoryCount()**](InventoryCountApi.md#generateInventoryCount) | **POST** /api/v1/inventory-counts/generate |  |
| [**getInventoryCount()**](InventoryCountApi.md#getInventoryCount) | **GET** /api/v1/inventory-counts/{inventory_count_id} |  |
| [**listInventoryCounts()**](InventoryCountApi.md#listInventoryCounts) | **GET** /api/v1/inventory-counts/ |  |
| [**updateInventoryCount()**](InventoryCountApi.md#updateInventoryCount) | **PUT** /api/v1/inventory-counts/{inventory_count_id} |  |
| [**updateInventoryCountStatus()**](InventoryCountApi.md#updateInventoryCountStatus) | **PUT** /api/v1/inventory-counts/{inventory_count_id}/status |  |


## `createInventoryCount()`

```php
createInventoryCount($inventory_count): \OpenAPI\Client\Model\InventoryCount
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InventoryCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inventory_count = new \OpenAPI\Client\Model\InventoryCount(); // \OpenAPI\Client\Model\InventoryCount

try {
    $result = $apiInstance->createInventoryCount($inventory_count);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryCountApi->createInventoryCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **inventory_count** | [**\OpenAPI\Client\Model\InventoryCount**](../Model/InventoryCount.md)|  | |

### Return type

[**\OpenAPI\Client\Model\InventoryCount**](../Model/InventoryCount.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteInventoryCount()`

```php
deleteInventoryCount($inventory_count_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InventoryCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inventory_count_id = 'inventory_count_id_example'; // string

try {
    $apiInstance->deleteInventoryCount($inventory_count_id);
} catch (Exception $e) {
    echo 'Exception when calling InventoryCountApi->deleteInventoryCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **inventory_count_id** | **string**|  | |

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

## `generateInventoryCount()`

```php
generateInventoryCount($generate_count_request): \OpenAPI\Client\Model\InventoryCount
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InventoryCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$generate_count_request = new \OpenAPI\Client\Model\GenerateCountRequest(); // \OpenAPI\Client\Model\GenerateCountRequest

try {
    $result = $apiInstance->generateInventoryCount($generate_count_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryCountApi->generateInventoryCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **generate_count_request** | [**\OpenAPI\Client\Model\GenerateCountRequest**](../Model/GenerateCountRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\InventoryCount**](../Model/InventoryCount.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getInventoryCount()`

```php
getInventoryCount($inventory_count_id): \OpenAPI\Client\Model\InventoryCount
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InventoryCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inventory_count_id = 'inventory_count_id_example'; // string

try {
    $result = $apiInstance->getInventoryCount($inventory_count_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryCountApi->getInventoryCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **inventory_count_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\InventoryCount**](../Model/InventoryCount.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listInventoryCounts()`

```php
listInventoryCounts($page, $page_size, $status, $warehouse_id): \OpenAPI\Client\Model\InventoryCount[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InventoryCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$status = 'status_example'; // string
$warehouse_id = 'warehouse_id_example'; // string

try {
    $result = $apiInstance->listInventoryCounts($page, $page_size, $status, $warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryCountApi->listInventoryCounts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |
| **warehouse_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\InventoryCount[]**](../Model/InventoryCount.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateInventoryCount()`

```php
updateInventoryCount($inventory_count_id, $body): \OpenAPI\Client\Model\InventoryCount
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InventoryCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inventory_count_id = 'inventory_count_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateInventoryCount($inventory_count_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryCountApi->updateInventoryCount: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **inventory_count_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\InventoryCount**](../Model/InventoryCount.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateInventoryCountStatus()`

```php
updateInventoryCountStatus($inventory_count_id, $inventory_count_status_update): \OpenAPI\Client\Model\InventoryCount
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InventoryCountApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$inventory_count_id = 'inventory_count_id_example'; // string
$inventory_count_status_update = new \OpenAPI\Client\Model\InventoryCountStatusUpdate(); // \OpenAPI\Client\Model\InventoryCountStatusUpdate

try {
    $result = $apiInstance->updateInventoryCountStatus($inventory_count_id, $inventory_count_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InventoryCountApi->updateInventoryCountStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **inventory_count_id** | **string**|  | |
| **inventory_count_status_update** | [**\OpenAPI\Client\Model\InventoryCountStatusUpdate**](../Model/InventoryCountStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\InventoryCount**](../Model/InventoryCount.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
