# OpenAPI\Client\ReorderProposalApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**applyReorderProposal()**](ReorderProposalApi.md#applyReorderProposal) | **POST** /api/v1/reorder-proposals/apply | Convert a reorder proposal into a draft purchase order. |
| [**getReorderProposal()**](ReorderProposalApi.md#getReorderProposal) | **GET** /api/v1/reorder-proposals |  |


## `applyReorderProposal()`

```php
applyReorderProposal($configured_only, $warehouse_id): mixed
```

Convert a reorder proposal into a draft purchase order.

Returns the created purchase order id. Suggested line items are generated with the current reorder quantity per product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReorderProposalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$configured_only = True; // bool | Only include products with a reorder point configured (`min_stock`).
$warehouse_id = 'warehouse_id_example'; // string | Limit to a single warehouse id.

try {
    $result = $apiInstance->applyReorderProposal($configured_only, $warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReorderProposalApi->applyReorderProposal: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **configured_only** | **bool**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] |
| **warehouse_id** | **string**| Limit to a single warehouse id. | [optional] |

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

## `getReorderProposal()`

```php
getReorderProposal($configured_only, $warehouse_id): \OpenAPI\Client\Model\ReorderProposalResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReorderProposalApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$configured_only = True; // bool | Only include products with a reorder point configured (`min_stock`).
$warehouse_id = 'warehouse_id_example'; // string | Limit to a single warehouse id.

try {
    $result = $apiInstance->getReorderProposal($configured_only, $warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReorderProposalApi->getReorderProposal: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **configured_only** | **bool**| Only include products with a reorder point configured (&#x60;min_stock&#x60;). | [optional] |
| **warehouse_id** | **string**| Limit to a single warehouse id. | [optional] |

### Return type

[**\OpenAPI\Client\Model\ReorderProposalResponse**](../Model/ReorderProposalResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
