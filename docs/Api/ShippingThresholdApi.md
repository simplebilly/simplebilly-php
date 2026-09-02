# OpenAPI\Client\ShippingThresholdApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createShippingThreshold()**](ShippingThresholdApi.md#createShippingThreshold) | **POST** /api/v1/shipping-thresholds |  |
| [**deleteShippingThreshold()**](ShippingThresholdApi.md#deleteShippingThreshold) | **DELETE** /api/v1/shipping-thresholds/{threshold_id} |  |
| [**getDeliverable()**](ShippingThresholdApi.md#getDeliverable) | **GET** /api/v1/shipping-thresholds/deliverable |  |
| [**getShippingThreshold()**](ShippingThresholdApi.md#getShippingThreshold) | **GET** /api/v1/shipping-thresholds/{threshold_id} |  |
| [**listShippingThresholds()**](ShippingThresholdApi.md#listShippingThresholds) | **GET** /api/v1/shipping-thresholds/ |  |
| [**updateShippingThreshold()**](ShippingThresholdApi.md#updateShippingThreshold) | **PUT** /api/v1/shipping-thresholds/{threshold_id} |  |


## `createShippingThreshold()`

```php
createShippingThreshold($shipping_threshold_create): \OpenAPI\Client\Model\ShippingThreshold
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingThresholdApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipping_threshold_create = new \OpenAPI\Client\Model\ShippingThresholdCreate(); // \OpenAPI\Client\Model\ShippingThresholdCreate

try {
    $result = $apiInstance->createShippingThreshold($shipping_threshold_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingThresholdApi->createShippingThreshold: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipping_threshold_create** | [**\OpenAPI\Client\Model\ShippingThresholdCreate**](../Model/ShippingThresholdCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ShippingThreshold**](../Model/ShippingThreshold.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteShippingThreshold()`

```php
deleteShippingThreshold($threshold_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingThresholdApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$threshold_id = 'threshold_id_example'; // string

try {
    $apiInstance->deleteShippingThreshold($threshold_id);
} catch (Exception $e) {
    echo 'Exception when calling ShippingThresholdApi->deleteShippingThreshold: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **threshold_id** | **string**|  | |

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

## `getDeliverable()`

```php
getDeliverable($product_id, $warehouse_id): \OpenAPI\Client\Model\DeliverableResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingThresholdApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 'product_id_example'; // string
$warehouse_id = 'warehouse_id_example'; // string

try {
    $result = $apiInstance->getDeliverable($product_id, $warehouse_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingThresholdApi->getDeliverable: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**|  | |
| **warehouse_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DeliverableResponse**](../Model/DeliverableResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getShippingThreshold()`

```php
getShippingThreshold($threshold_id): \OpenAPI\Client\Model\ShippingThreshold
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingThresholdApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$threshold_id = 'threshold_id_example'; // string

try {
    $result = $apiInstance->getShippingThreshold($threshold_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingThresholdApi->getShippingThreshold: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **threshold_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ShippingThreshold**](../Model/ShippingThreshold.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listShippingThresholds()`

```php
listShippingThresholds($page, $page_size, $product_id, $warehouse_id, $is_active): \OpenAPI\Client\Model\ShippingThreshold[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingThresholdApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$product_id = 'product_id_example'; // string
$warehouse_id = 'warehouse_id_example'; // string
$is_active = True; // bool

try {
    $result = $apiInstance->listShippingThresholds($page, $page_size, $product_id, $warehouse_id, $is_active);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingThresholdApi->listShippingThresholds: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **product_id** | **string**|  | [optional] |
| **warehouse_id** | **string**|  | [optional] |
| **is_active** | **bool**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ShippingThreshold[]**](../Model/ShippingThreshold.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateShippingThreshold()`

```php
updateShippingThreshold($threshold_id, $shipping_threshold_update): \OpenAPI\Client\Model\ShippingThreshold
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingThresholdApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$threshold_id = 'threshold_id_example'; // string
$shipping_threshold_update = new \OpenAPI\Client\Model\ShippingThresholdUpdate(); // \OpenAPI\Client\Model\ShippingThresholdUpdate

try {
    $result = $apiInstance->updateShippingThreshold($threshold_id, $shipping_threshold_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingThresholdApi->updateShippingThreshold: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **threshold_id** | **string**|  | |
| **shipping_threshold_update** | [**\OpenAPI\Client\Model\ShippingThresholdUpdate**](../Model/ShippingThresholdUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ShippingThreshold**](../Model/ShippingThreshold.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
