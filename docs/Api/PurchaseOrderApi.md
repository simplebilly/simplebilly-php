# OpenAPI\Client\PurchaseOrderApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPurchaseOrder()**](PurchaseOrderApi.md#createPurchaseOrder) | **POST** /api/v1/purchase-orders |  |
| [**deletePurchaseOrder()**](PurchaseOrderApi.md#deletePurchaseOrder) | **DELETE** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**getPurchaseOrder()**](PurchaseOrderApi.md#getPurchaseOrder) | **GET** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**listPurchaseOrders()**](PurchaseOrderApi.md#listPurchaseOrders) | **GET** /api/v1/purchase-orders/ |  |
| [**matchInvoice()**](PurchaseOrderApi.md#matchInvoice) | **POST** /api/v1/purchase-orders/{purchase_order_id}/match-invoice | 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product. |
| [**updatePurchaseOrder()**](PurchaseOrderApi.md#updatePurchaseOrder) | **PUT** /api/v1/purchase-orders/{purchase_order_id} |  |
| [**updatePurchaseOrderStatus()**](PurchaseOrderApi.md#updatePurchaseOrderStatus) | **PUT** /api/v1/purchase-orders/{purchase_order_id}/status |  |


## `createPurchaseOrder()`

```php
createPurchaseOrder($purchase_order): \OpenAPI\Client\Model\PurchaseOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchase_order = new \OpenAPI\Client\Model\PurchaseOrder(); // \OpenAPI\Client\Model\PurchaseOrder

try {
    $result = $apiInstance->createPurchaseOrder($purchase_order);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->createPurchaseOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **purchase_order** | [**\OpenAPI\Client\Model\PurchaseOrder**](../Model/PurchaseOrder.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PurchaseOrder**](../Model/PurchaseOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deletePurchaseOrder()`

```php
deletePurchaseOrder($purchase_order_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchase_order_id = 'purchase_order_id_example'; // string

try {
    $apiInstance->deletePurchaseOrder($purchase_order_id);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->deletePurchaseOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **purchase_order_id** | **string**|  | |

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

## `getPurchaseOrder()`

```php
getPurchaseOrder($purchase_order_id): \OpenAPI\Client\Model\PurchaseOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchase_order_id = 'purchase_order_id_example'; // string

try {
    $result = $apiInstance->getPurchaseOrder($purchase_order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->getPurchaseOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **purchase_order_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PurchaseOrder**](../Model/PurchaseOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPurchaseOrders()`

```php
listPurchaseOrders($page, $page_size, $status, $supplier_name, $search): \OpenAPI\Client\Model\PurchaseOrder[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$status = 'status_example'; // string
$supplier_name = 'supplier_name_example'; // string
$search = 'search_example'; // string

try {
    $result = $apiInstance->listPurchaseOrders($page, $page_size, $status, $supplier_name, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->listPurchaseOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |
| **supplier_name** | **string**|  | [optional] |
| **search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PurchaseOrder[]**](../Model/PurchaseOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `matchInvoice()`

```php
matchInvoice($purchase_order_id, $invoice_match_request): mixed
```

3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchase_order_id = 'purchase_order_id_example'; // string
$invoice_match_request = new \OpenAPI\Client\Model\InvoiceMatchRequest(); // \OpenAPI\Client\Model\InvoiceMatchRequest

try {
    $result = $apiInstance->matchInvoice($purchase_order_id, $invoice_match_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->matchInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **purchase_order_id** | **string**|  | |
| **invoice_match_request** | [**\OpenAPI\Client\Model\InvoiceMatchRequest**](../Model/InvoiceMatchRequest.md)|  | |

### Return type

**mixed**

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePurchaseOrder()`

```php
updatePurchaseOrder($purchase_order_id, $body): \OpenAPI\Client\Model\PurchaseOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchase_order_id = 'purchase_order_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updatePurchaseOrder($purchase_order_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->updatePurchaseOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **purchase_order_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\PurchaseOrder**](../Model/PurchaseOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePurchaseOrderStatus()`

```php
updatePurchaseOrderStatus($purchase_order_id, $purchase_order_status_update): \OpenAPI\Client\Model\PurchaseOrder
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PurchaseOrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$purchase_order_id = 'purchase_order_id_example'; // string
$purchase_order_status_update = new \OpenAPI\Client\Model\PurchaseOrderStatusUpdate(); // \OpenAPI\Client\Model\PurchaseOrderStatusUpdate

try {
    $result = $apiInstance->updatePurchaseOrderStatus($purchase_order_id, $purchase_order_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PurchaseOrderApi->updatePurchaseOrderStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **purchase_order_id** | **string**|  | |
| **purchase_order_status_update** | [**\OpenAPI\Client\Model\PurchaseOrderStatusUpdate**](../Model/PurchaseOrderStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PurchaseOrder**](../Model/PurchaseOrder.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
