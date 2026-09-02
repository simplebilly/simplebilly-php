# OpenAPI\Client\ProductionOrderApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createProductionOrder()**](ProductionOrderApi.md#createProductionOrder) | **POST** /api/v1/production-orders |  |
| [**deleteProductionOrder()**](ProductionOrderApi.md#deleteProductionOrder) | **DELETE** /api/v1/production-orders/{production_order_id} |  |
| [**getProductionOrder()**](ProductionOrderApi.md#getProductionOrder) | **GET** /api/v1/production-orders/{production_order_id} |  |
| [**listProductionOrders()**](ProductionOrderApi.md#listProductionOrders) | **GET** /api/v1/production-orders/ |  |
| [**productionOrderCosting()**](ProductionOrderApi.md#productionOrderCosting) | **GET** /api/v1/production-orders/{production_order_id}/costing | Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product&#39;s sale price. |
| [**updateProductionOrder()**](ProductionOrderApi.md#updateProductionOrder) | **PUT** /api/v1/production-orders/{production_order_id} |  |
| [**updateProductionOrderStatus()**](ProductionOrderApi.md#updateProductionOrderStatus) | **PUT** /api/v1/production-orders/{production_order_id}/status |  |


## `createProductionOrder()`

```php
createProductionOrder($production_order): \OpenAPI\Client\Model\ProductionOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$production_order = new \OpenAPI\Client\Model\ProductionOrder(); // \OpenAPI\Client\Model\ProductionOrder

try {
    $result = $apiInstance->createProductionOrder($production_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->createProductionOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **production_order** | [**\OpenAPI\Client\Model\ProductionOrder**](../Model/ProductionOrder.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ProductionOrder**](../Model/ProductionOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteProductionOrder()`

```php
deleteProductionOrder($production_order_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$production_order_id = 'production_order_id_example'; // string

try {
    $apiInstance->deleteProductionOrder($production_order_id);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->deleteProductionOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **production_order_id** | **string**|  | |

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

## `getProductionOrder()`

```php
getProductionOrder($production_order_id): \OpenAPI\Client\Model\ProductionOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$production_order_id = 'production_order_id_example'; // string

try {
    $result = $apiInstance->getProductionOrder($production_order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->getProductionOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **production_order_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ProductionOrder**](../Model/ProductionOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listProductionOrders()`

```php
listProductionOrders($page, $page_size, $search, $status): \OpenAPI\Client\Model\ProductionOrder[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$search = 'search_example'; // string
$status = 'status_example'; // string | Filter by status.

try {
    $result = $apiInstance->listProductionOrders($page, $page_size, $search, $status);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->listProductionOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **search** | **string**|  | [optional] |
| **status** | **string**| Filter by status. | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductionOrder[]**](../Model/ProductionOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `productionOrderCosting()`

```php
productionOrderCosting($production_order_id): \OpenAPI\Client\Model\ProductionOrderCosting
```

Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$production_order_id = 'production_order_id_example'; // string

try {
    $result = $apiInstance->productionOrderCosting($production_order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->productionOrderCosting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **production_order_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ProductionOrderCosting**](../Model/ProductionOrderCosting.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateProductionOrder()`

```php
updateProductionOrder($production_order_id, $production_order): \OpenAPI\Client\Model\ProductionOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$production_order_id = 'production_order_id_example'; // string
$production_order = new \OpenAPI\Client\Model\ProductionOrder(); // \OpenAPI\Client\Model\ProductionOrder

try {
    $result = $apiInstance->updateProductionOrder($production_order_id, $production_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->updateProductionOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **production_order_id** | **string**|  | |
| **production_order** | [**\OpenAPI\Client\Model\ProductionOrder**](../Model/ProductionOrder.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ProductionOrder**](../Model/ProductionOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateProductionOrderStatus()`

```php
updateProductionOrderStatus($production_order_id, $production_order_status_update): \OpenAPI\Client\Model\ProductionOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductionOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$production_order_id = 'production_order_id_example'; // string
$production_order_status_update = new \OpenAPI\Client\Model\ProductionOrderStatusUpdate(); // \OpenAPI\Client\Model\ProductionOrderStatusUpdate

try {
    $result = $apiInstance->updateProductionOrderStatus($production_order_id, $production_order_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductionOrderApi->updateProductionOrderStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **production_order_id** | **string**|  | |
| **production_order_status_update** | [**\OpenAPI\Client\Model\ProductionOrderStatusUpdate**](../Model/ProductionOrderStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ProductionOrder**](../Model/ProductionOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
