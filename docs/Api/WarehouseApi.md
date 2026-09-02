# OpenAPI\Client\WarehouseApi

Warehouse management. Required permissions: warehouse:read, warehouse:write, warehouse:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createWarehouse()**](WarehouseApi.md#createWarehouse) | **POST** /api/v1/warehouses |  |
| [**deleteWarehouse()**](WarehouseApi.md#deleteWarehouse) | **DELETE** /api/v1/warehouses/{warehouse_id} |  |
| [**getWarehouse()**](WarehouseApi.md#getWarehouse) | **GET** /api/v1/warehouses/{warehouse_id} |  |
| [**listWarehouses()**](WarehouseApi.md#listWarehouses) | **GET** /api/v1/warehouses/ |  |
| [**updateWarehouse()**](WarehouseApi.md#updateWarehouse) | **PUT** /api/v1/warehouses/{warehouse_id} |  |


## `createWarehouse()`

```php
createWarehouse($warehouse): \OpenAPI\Client\Model\Warehouse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse = new \OpenAPI\Client\Model\Warehouse(); // \OpenAPI\Client\Model\Warehouse

try {
    $result = $apiInstance->createWarehouse($warehouse);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseApi->createWarehouse: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse** | [**\OpenAPI\Client\Model\Warehouse**](../Model/Warehouse.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Warehouse**](../Model/Warehouse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteWarehouse()`

```php
deleteWarehouse($warehouse_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse_id = 'warehouse_id_example'; // string

try {
    $apiInstance->deleteWarehouse($warehouse_id);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseApi->deleteWarehouse: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse_id** | **string**|  | |

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

## `getWarehouse()`

```php
getWarehouse($warehouse_id): \OpenAPI\Client\Model\Warehouse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse_id = 'warehouse_id_example'; // string

try {
    $result = $apiInstance->getWarehouse($warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseApi->getWarehouse: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Warehouse**](../Model/Warehouse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listWarehouses()`

```php
listWarehouses($page, $page_size, $search, $is_active): \OpenAPI\Client\Model\Warehouse[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$search = 'search_example'; // string
$is_active = True; // bool

try {
    $result = $apiInstance->listWarehouses($page, $page_size, $search, $is_active);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseApi->listWarehouses: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **search** | **string**|  | [optional] |
| **is_active** | **bool**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Warehouse[]**](../Model/Warehouse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateWarehouse()`

```php
updateWarehouse($warehouse_id, $body): \OpenAPI\Client\Model\Warehouse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse_id = 'warehouse_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateWarehouse($warehouse_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseApi->updateWarehouse: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\Warehouse**](../Model/Warehouse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
