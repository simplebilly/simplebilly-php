# OpenAPI\Client\WarehouseStockApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createWarehouseStock()**](WarehouseStockApi.md#createWarehouseStock) | **POST** /api/v1/warehouses/{warehouse_id}/stock |  |
| [**deleteWarehouseStock()**](WarehouseStockApi.md#deleteWarehouseStock) | **DELETE** /api/v1/warehouses/{warehouse_id}/stock/{product_id} |  |
| [**listWarehouseStock()**](WarehouseStockApi.md#listWarehouseStock) | **GET** /api/v1/warehouses/{warehouse_id}/stock |  |
| [**updateWarehouseStock()**](WarehouseStockApi.md#updateWarehouseStock) | **PUT** /api/v1/warehouses/{warehouse_id}/stock/{product_id} |  |


## `createWarehouseStock()`

```php
createWarehouseStock($warehouse_id, $stock_adjustment): \OpenAPI\Client\Model\WarehouseStock
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse_id = 'warehouse_id_example'; // string
$stock_adjustment = new \OpenAPI\Client\Model\StockAdjustment(); // \OpenAPI\Client\Model\StockAdjustment

try {
    $result = $apiInstance->createWarehouseStock($warehouse_id, $stock_adjustment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseStockApi->createWarehouseStock: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse_id** | **string**|  | |
| **stock_adjustment** | [**\OpenAPI\Client\Model\StockAdjustment**](../Model/StockAdjustment.md)|  | |

### Return type

[**\OpenAPI\Client\Model\WarehouseStock**](../Model/WarehouseStock.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteWarehouseStock()`

```php
deleteWarehouseStock($warehouse_id, $product_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse_id = 'warehouse_id_example'; // string
$product_id = 'product_id_example'; // string

try {
    $apiInstance->deleteWarehouseStock($warehouse_id, $product_id);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseStockApi->deleteWarehouseStock: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse_id** | **string**|  | |
| **product_id** | **string**|  | |

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

## `listWarehouseStock()`

```php
listWarehouseStock($warehouse_id): \OpenAPI\Client\Model\WarehouseStock[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse_id = 'warehouse_id_example'; // string

try {
    $result = $apiInstance->listWarehouseStock($warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseStockApi->listWarehouseStock: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\WarehouseStock[]**](../Model/WarehouseStock.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateWarehouseStock()`

```php
updateWarehouseStock($warehouse_id, $product_id, $stock_adjustment): \OpenAPI\Client\Model\WarehouseStock
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\WarehouseStockApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$warehouse_id = 'warehouse_id_example'; // string
$product_id = 'product_id_example'; // string
$stock_adjustment = new \OpenAPI\Client\Model\StockAdjustment(); // \OpenAPI\Client\Model\StockAdjustment

try {
    $result = $apiInstance->updateWarehouseStock($warehouse_id, $product_id, $stock_adjustment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling WarehouseStockApi->updateWarehouseStock: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **warehouse_id** | **string**|  | |
| **product_id** | **string**|  | |
| **stock_adjustment** | [**\OpenAPI\Client\Model\StockAdjustment**](../Model/StockAdjustment.md)|  | |

### Return type

[**\OpenAPI\Client\Model\WarehouseStock**](../Model/WarehouseStock.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
