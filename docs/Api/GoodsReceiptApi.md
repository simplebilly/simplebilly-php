# OpenAPI\Client\GoodsReceiptApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createGoodsReceipt()**](GoodsReceiptApi.md#createGoodsReceipt) | **POST** /api/v1/goods-receipts |  |
| [**deleteGoodsReceipt()**](GoodsReceiptApi.md#deleteGoodsReceipt) | **DELETE** /api/v1/goods-receipts/{goods_receipt_id} |  |
| [**getGoodsReceipt()**](GoodsReceiptApi.md#getGoodsReceipt) | **GET** /api/v1/goods-receipts/{goods_receipt_id} |  |
| [**listGoodsReceipts()**](GoodsReceiptApi.md#listGoodsReceipts) | **GET** /api/v1/goods-receipts/ |  |


## `createGoodsReceipt()`

```php
createGoodsReceipt($goods_receipt): \OpenAPI\Client\Model\GoodsReceipt
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GoodsReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$goods_receipt = new \OpenAPI\Client\Model\GoodsReceipt(); // \OpenAPI\Client\Model\GoodsReceipt

try {
    $result = $apiInstance->createGoodsReceipt($goods_receipt);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoodsReceiptApi->createGoodsReceipt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **goods_receipt** | [**\OpenAPI\Client\Model\GoodsReceipt**](../Model/GoodsReceipt.md)|  | |

### Return type

[**\OpenAPI\Client\Model\GoodsReceipt**](../Model/GoodsReceipt.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteGoodsReceipt()`

```php
deleteGoodsReceipt($goods_receipt_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GoodsReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$goods_receipt_id = 'goods_receipt_id_example'; // string

try {
    $apiInstance->deleteGoodsReceipt($goods_receipt_id);
} catch (Exception $e) {
    echo 'Exception when calling GoodsReceiptApi->deleteGoodsReceipt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **goods_receipt_id** | **string**|  | |

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

## `getGoodsReceipt()`

```php
getGoodsReceipt($goods_receipt_id): \OpenAPI\Client\Model\GoodsReceipt
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GoodsReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$goods_receipt_id = 'goods_receipt_id_example'; // string

try {
    $result = $apiInstance->getGoodsReceipt($goods_receipt_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoodsReceiptApi->getGoodsReceipt: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **goods_receipt_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\GoodsReceipt**](../Model/GoodsReceipt.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listGoodsReceipts()`

```php
listGoodsReceipts($page, $page_size, $purchase_order_id, $supplier_name, $warehouse_id): \OpenAPI\Client\Model\GoodsReceipt[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GoodsReceiptApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$purchase_order_id = 'purchase_order_id_example'; // string
$supplier_name = 'supplier_name_example'; // string
$warehouse_id = 'warehouse_id_example'; // string

try {
    $result = $apiInstance->listGoodsReceipts($page, $page_size, $purchase_order_id, $supplier_name, $warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GoodsReceiptApi->listGoodsReceipts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **purchase_order_id** | **string**|  | [optional] |
| **supplier_name** | **string**|  | [optional] |
| **warehouse_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GoodsReceipt[]**](../Model/GoodsReceipt.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
