# OpenAPI\Client\ReplenishmentApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**applyReplenishments()**](ReplenishmentApi.md#applyReplenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair. |
| [**getReplenishments()**](ReplenishmentApi.md#getReplenishments) | **GET** /api/v1/replenishments |  |


## `applyReplenishments()`

```php
applyReplenishments($target_warehouse_id, $source_warehouse_id): mixed
```

Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReplenishmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$target_warehouse_id = 'target_warehouse_id_example'; // string | Warehouse to be replenished. Defaults to the tenant's default warehouse.
$source_warehouse_id = 'source_warehouse_id_example'; // string | Restrict source warehouses to this id.

try {
    $result = $apiInstance->applyReplenishments($target_warehouse_id, $source_warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReplenishmentApi->applyReplenishments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **target_warehouse_id** | **string**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] |
| **source_warehouse_id** | **string**| Restrict source warehouses to this id. | [optional] |

### Return type

**mixed**

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getReplenishments()`

```php
getReplenishments($target_warehouse_id, $source_warehouse_id): \OpenAPI\Client\Model\ReplenishmentResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReplenishmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$target_warehouse_id = 'target_warehouse_id_example'; // string | Warehouse to be replenished. Defaults to the tenant's default warehouse.
$source_warehouse_id = 'source_warehouse_id_example'; // string | Restrict source warehouses to this id.

try {
    $result = $apiInstance->getReplenishments($target_warehouse_id, $source_warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReplenishmentApi->getReplenishments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **target_warehouse_id** | **string**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] |
| **source_warehouse_id** | **string**| Restrict source warehouses to this id. | [optional] |

### Return type

[**\OpenAPI\Client\Model\ReplenishmentResponse**](../Model/ReplenishmentResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
