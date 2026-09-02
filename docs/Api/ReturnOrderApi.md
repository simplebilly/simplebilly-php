# OpenAPI\Client\ReturnOrderApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createReturnOrder()**](ReturnOrderApi.md#createReturnOrder) | **POST** /api/v1/returns |  |
| [**deleteReturnOrder()**](ReturnOrderApi.md#deleteReturnOrder) | **DELETE** /api/v1/returns/{return_order_id} |  |
| [**getReturnOrder()**](ReturnOrderApi.md#getReturnOrder) | **GET** /api/v1/returns/{return_order_id} |  |
| [**listReturnOrders()**](ReturnOrderApi.md#listReturnOrders) | **GET** /api/v1/returns/ |  |
| [**returnLogisticsQueue()**](ReturnOrderApi.md#returnLogisticsQueue) | **GET** /api/v1/returns/logistics-queue |  |
| [**returnLogisticsSummary()**](ReturnOrderApi.md#returnLogisticsSummary) | **GET** /api/v1/returns/logistics-summary | Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse. |
| [**updateReturnOrder()**](ReturnOrderApi.md#updateReturnOrder) | **PUT** /api/v1/returns/{return_order_id} |  |
| [**updateReturnOrderStatus()**](ReturnOrderApi.md#updateReturnOrderStatus) | **PUT** /api/v1/returns/{return_order_id}/status |  |


## `createReturnOrder()`

```php
createReturnOrder($return_order): \OpenAPI\Client\Model\ReturnOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReturnOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$return_order = new \OpenAPI\Client\Model\ReturnOrder(); // \OpenAPI\Client\Model\ReturnOrder

try {
    $result = $apiInstance->createReturnOrder($return_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnOrderApi->createReturnOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **return_order** | [**\OpenAPI\Client\Model\ReturnOrder**](../Model/ReturnOrder.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ReturnOrder**](../Model/ReturnOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteReturnOrder()`

```php
deleteReturnOrder($return_order_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReturnOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$return_order_id = 'return_order_id_example'; // string

try {
    $apiInstance->deleteReturnOrder($return_order_id);
} catch (Exception $e) {
    echo 'Exception when calling ReturnOrderApi->deleteReturnOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **return_order_id** | **string**|  | |

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

## `getReturnOrder()`

```php
getReturnOrder($return_order_id): \OpenAPI\Client\Model\ReturnOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReturnOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$return_order_id = 'return_order_id_example'; // string

try {
    $result = $apiInstance->getReturnOrder($return_order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnOrderApi->getReturnOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **return_order_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ReturnOrder**](../Model/ReturnOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listReturnOrders()`

```php
listReturnOrders($page, $page_size, $status, $customer_name, $order_number): \OpenAPI\Client\Model\ReturnOrder[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReturnOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$status = 'status_example'; // string
$customer_name = 'customer_name_example'; // string
$order_number = 'order_number_example'; // string

try {
    $result = $apiInstance->listReturnOrders($page, $page_size, $status, $customer_name, $order_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnOrderApi->listReturnOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |
| **customer_name** | **string**|  | [optional] |
| **order_number** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ReturnOrder[]**](../Model/ReturnOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `returnLogisticsQueue()`

```php
returnLogisticsQueue(): \OpenAPI\Client\Model\ReturnLogisticsQueueItem[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReturnOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->returnLogisticsQueue();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnOrderApi->returnLogisticsQueue: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ReturnLogisticsQueueItem[]**](../Model/ReturnLogisticsQueueItem.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `returnLogisticsSummary()`

```php
returnLogisticsSummary(): \OpenAPI\Client\Model\ReturnLogisticsSummary
```

Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReturnOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->returnLogisticsSummary();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnOrderApi->returnLogisticsSummary: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ReturnLogisticsSummary**](../Model/ReturnLogisticsSummary.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateReturnOrder()`

```php
updateReturnOrder($return_order_id, $body): \OpenAPI\Client\Model\ReturnOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReturnOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$return_order_id = 'return_order_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateReturnOrder($return_order_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnOrderApi->updateReturnOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **return_order_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\ReturnOrder**](../Model/ReturnOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateReturnOrderStatus()`

```php
updateReturnOrderStatus($return_order_id, $return_order_status_update): \OpenAPI\Client\Model\ReturnOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReturnOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$return_order_id = 'return_order_id_example'; // string
$return_order_status_update = new \OpenAPI\Client\Model\ReturnOrderStatusUpdate(); // \OpenAPI\Client\Model\ReturnOrderStatusUpdate

try {
    $result = $apiInstance->updateReturnOrderStatus($return_order_id, $return_order_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReturnOrderApi->updateReturnOrderStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **return_order_id** | **string**|  | |
| **return_order_status_update** | [**\OpenAPI\Client\Model\ReturnOrderStatusUpdate**](../Model/ReturnOrderStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ReturnOrder**](../Model/ReturnOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
