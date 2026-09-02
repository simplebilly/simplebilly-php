# OpenAPI\Client\StockTransferApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createStockTransfer()**](StockTransferApi.md#createStockTransfer) | **POST** /api/v1/stock-transfers |  |
| [**deleteStockTransfer()**](StockTransferApi.md#deleteStockTransfer) | **DELETE** /api/v1/stock-transfers/{stock_transfer_id} |  |
| [**getStockTransfer()**](StockTransferApi.md#getStockTransfer) | **GET** /api/v1/stock-transfers/{stock_transfer_id} |  |
| [**listStockTransfers()**](StockTransferApi.md#listStockTransfers) | **GET** /api/v1/stock-transfers/ |  |
| [**updateStockTransferStatus()**](StockTransferApi.md#updateStockTransferStatus) | **PUT** /api/v1/stock-transfers/{stock_transfer_id}/status |  |


## `createStockTransfer()`

```php
createStockTransfer($stock_transfer): \OpenAPI\Client\Model\StockTransfer
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StockTransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stock_transfer = new \OpenAPI\Client\Model\StockTransfer(); // \OpenAPI\Client\Model\StockTransfer

try {
    $result = $apiInstance->createStockTransfer($stock_transfer);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockTransferApi->createStockTransfer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **stock_transfer** | [**\OpenAPI\Client\Model\StockTransfer**](../Model/StockTransfer.md)|  | |

### Return type

[**\OpenAPI\Client\Model\StockTransfer**](../Model/StockTransfer.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteStockTransfer()`

```php
deleteStockTransfer($stock_transfer_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StockTransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stock_transfer_id = 'stock_transfer_id_example'; // string

try {
    $apiInstance->deleteStockTransfer($stock_transfer_id);
} catch (Exception $e) {
    echo 'Exception when calling StockTransferApi->deleteStockTransfer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **stock_transfer_id** | **string**|  | |

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

## `getStockTransfer()`

```php
getStockTransfer($stock_transfer_id): \OpenAPI\Client\Model\StockTransfer
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StockTransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stock_transfer_id = 'stock_transfer_id_example'; // string

try {
    $result = $apiInstance->getStockTransfer($stock_transfer_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockTransferApi->getStockTransfer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **stock_transfer_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\StockTransfer**](../Model/StockTransfer.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listStockTransfers()`

```php
listStockTransfers($page, $page_size, $status, $warehouse_id): \OpenAPI\Client\Model\StockTransfer[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StockTransferApi(
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
    $result = $apiInstance->listStockTransfers($page, $page_size, $status, $warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockTransferApi->listStockTransfers: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\StockTransfer[]**](../Model/StockTransfer.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateStockTransferStatus()`

```php
updateStockTransferStatus($stock_transfer_id, $stock_transfer_status_update): \OpenAPI\Client\Model\StockTransfer
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StockTransferApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$stock_transfer_id = 'stock_transfer_id_example'; // string
$stock_transfer_status_update = new \OpenAPI\Client\Model\StockTransferStatusUpdate(); // \OpenAPI\Client\Model\StockTransferStatusUpdate

try {
    $result = $apiInstance->updateStockTransferStatus($stock_transfer_id, $stock_transfer_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockTransferApi->updateStockTransferStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **stock_transfer_id** | **string**|  | |
| **stock_transfer_status_update** | [**\OpenAPI\Client\Model\StockTransferStatusUpdate**](../Model/StockTransferStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\StockTransfer**](../Model/StockTransfer.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
