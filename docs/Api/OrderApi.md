# OpenAPI\Client\OrderApi

Order management. Required permissions: order:read, order:write, order:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addOrderTags()**](OrderApi.md#addOrderTags) | **POST** /api/v1/orders/{order_id}/tags |  |
| [**findOrderByExternalRef()**](OrderApi.md#findOrderByExternalRef) | **GET** /api/v1/orders/by-ext-ref/{ext_ref} |  |
| [**getOrder()**](OrderApi.md#getOrder) | **GET** /api/v1/order/{order_number} |  |
| [**getOrders()**](OrderApi.md#getOrders) | **GET** /api/v1/orders |  |
| [**patchOrder()**](OrderApi.md#patchOrder) | **PATCH** /api/v1/orders/{order_id} |  |
| [**replaceOrderTags()**](OrderApi.md#replaceOrderTags) | **PUT** /api/v1/orders/{order_id}/tags |  |
| [**updateOrderState()**](OrderApi.md#updateOrderState) | **PUT** /api/v1/orders/{order_id}/state |  |


## `addOrderTags()`

```php
addOrderTags($order_id, $order_tags_request): \OpenAPI\Client\Model\Order
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string
$order_tags_request = new \OpenAPI\Client\Model\OrderTagsRequest(); // \OpenAPI\Client\Model\OrderTagsRequest

try {
    $result = $apiInstance->addOrderTags($order_id, $order_tags_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->addOrderTags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **string**|  | |
| **order_tags_request** | [**\OpenAPI\Client\Model\OrderTagsRequest**](../Model/OrderTagsRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `findOrderByExternalRef()`

```php
findOrderByExternalRef($ext_ref): \OpenAPI\Client\Model\Order
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ext_ref = 'ext_ref_example'; // string

try {
    $result = $apiInstance->findOrderByExternalRef($ext_ref);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->findOrderByExternalRef: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ext_ref** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrder()`

```php
getOrder($order_number): \OpenAPI\Client\Model\Order
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_number = 'order_number_example'; // string

try {
    $result = $apiInstance->getOrder($order_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->getOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_number** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrders()`

```php
getOrders($page, $page_size, $search, $include_deleted): \OpenAPI\Client\Model\Order[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
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
    $result = $apiInstance->getOrders($page, $page_size, $search, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->getOrders: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\Order[]**](../Model/Order.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `patchOrder()`

```php
patchOrder($order_id, $body): \OpenAPI\Client\Model\Order
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->patchOrder($order_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->patchOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `replaceOrderTags()`

```php
replaceOrderTags($order_id, $order_tags_request): \OpenAPI\Client\Model\Order
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string
$order_tags_request = new \OpenAPI\Client\Model\OrderTagsRequest(); // \OpenAPI\Client\Model\OrderTagsRequest

try {
    $result = $apiInstance->replaceOrderTags($order_id, $order_tags_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->replaceOrderTags: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **string**|  | |
| **order_tags_request** | [**\OpenAPI\Client\Model\OrderTagsRequest**](../Model/OrderTagsRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOrderState()`

```php
updateOrderState($order_id, $order_state_update): \OpenAPI\Client\Model\Order
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_id = 'order_id_example'; // string
$order_state_update = new \OpenAPI\Client\Model\OrderStateUpdate(); // \OpenAPI\Client\Model\OrderStateUpdate

try {
    $result = $apiInstance->updateOrderState($order_id, $order_state_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->updateOrderState: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_id** | **string**|  | |
| **order_state_update** | [**\OpenAPI\Client\Model\OrderStateUpdate**](../Model/OrderStateUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Order**](../Model/Order.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
