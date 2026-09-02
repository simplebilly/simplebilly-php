# OpenAPI\Client\StockMovementApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getStockMovement()**](StockMovementApi.md#getStockMovement) | **GET** /api/v1/stock-movements/{movement_id} |  |
| [**listStockMovements()**](StockMovementApi.md#listStockMovements) | **GET** /api/v1/stock-movements/ |  |


## `getStockMovement()`

```php
getStockMovement($movement_id): \OpenAPI\Client\Model\StockMovement
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StockMovementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$movement_id = 'movement_id_example'; // string

try {
    $result = $apiInstance->getStockMovement($movement_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockMovementApi->getStockMovement: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **movement_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\StockMovement**](../Model/StockMovement.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listStockMovements()`

```php
listStockMovements($page, $page_size, $product_id, $warehouse_id, $movement_type, $from, $to): \OpenAPI\Client\Model\StockMovement[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\StockMovementApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$product_id = 'product_id_example'; // string
$warehouse_id = 'warehouse_id_example'; // string
$movement_type = 'movement_type_example'; // string
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Only movements on or after this date (inclusive).
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Only movements on or before this date (inclusive).

try {
    $result = $apiInstance->listStockMovements($page, $page_size, $product_id, $warehouse_id, $movement_type, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling StockMovementApi->listStockMovements: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **product_id** | **string**|  | [optional] |
| **warehouse_id** | **string**|  | [optional] |
| **movement_type** | **string**|  | [optional] |
| **from** | **\DateTime**| Only movements on or after this date (inclusive). | [optional] |
| **to** | **\DateTime**| Only movements on or before this date (inclusive). | [optional] |

### Return type

[**\OpenAPI\Client\Model\StockMovement[]**](../Model/StockMovement.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
