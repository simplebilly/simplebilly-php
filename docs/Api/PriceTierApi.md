# OpenAPI\Client\PriceTierApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPriceTier()**](PriceTierApi.md#createPriceTier) | **POST** /api/v1/price-tiers |  |
| [**deletePriceTier()**](PriceTierApi.md#deletePriceTier) | **DELETE** /api/v1/price-tiers/{price_tier_id} |  |
| [**getPriceTier()**](PriceTierApi.md#getPriceTier) | **GET** /api/v1/price-tiers/{price_tier_id} |  |
| [**getResolvedPrice()**](PriceTierApi.md#getResolvedPrice) | **GET** /api/v1/price-tiers/resolved |  |
| [**listPriceTiers()**](PriceTierApi.md#listPriceTiers) | **GET** /api/v1/price-tiers/ |  |
| [**updatePriceTier()**](PriceTierApi.md#updatePriceTier) | **PUT** /api/v1/price-tiers/{price_tier_id} |  |


## `createPriceTier()`

```php
createPriceTier($price_tier_create): \OpenAPI\Client\Model\PriceTier
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PriceTierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$price_tier_create = new \OpenAPI\Client\Model\PriceTierCreate(); // \OpenAPI\Client\Model\PriceTierCreate

try {
    $result = $apiInstance->createPriceTier($price_tier_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PriceTierApi->createPriceTier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **price_tier_create** | [**\OpenAPI\Client\Model\PriceTierCreate**](../Model/PriceTierCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PriceTier**](../Model/PriceTier.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deletePriceTier()`

```php
deletePriceTier($price_tier_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PriceTierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$price_tier_id = 'price_tier_id_example'; // string

try {
    $apiInstance->deletePriceTier($price_tier_id);
} catch (Exception $e) {
    echo 'Exception when calling PriceTierApi->deletePriceTier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **price_tier_id** | **string**|  | |

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

## `getPriceTier()`

```php
getPriceTier($price_tier_id): \OpenAPI\Client\Model\PriceTier
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PriceTierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$price_tier_id = 'price_tier_id_example'; // string

try {
    $result = $apiInstance->getPriceTier($price_tier_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PriceTierApi->getPriceTier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **price_tier_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PriceTier**](../Model/PriceTier.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getResolvedPrice()`

```php
getResolvedPrice($product_id, $quantity, $contact_id): \OpenAPI\Client\Model\ResolvedPriceResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PriceTierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_id = 'product_id_example'; // string
$quantity = 56; // int
$contact_id = 'contact_id_example'; // string | Contact used to match customer-group-scoped tiers.

try {
    $result = $apiInstance->getResolvedPrice($product_id, $quantity, $contact_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PriceTierApi->getResolvedPrice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_id** | **string**|  | |
| **quantity** | **int**|  | [optional] |
| **contact_id** | **string**| Contact used to match customer-group-scoped tiers. | [optional] |

### Return type

[**\OpenAPI\Client\Model\ResolvedPriceResponse**](../Model/ResolvedPriceResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPriceTiers()`

```php
listPriceTiers($page, $page_size, $product_id, $customer_group_id): \OpenAPI\Client\Model\PriceTier[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PriceTierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$product_id = 'product_id_example'; // string
$customer_group_id = 'customer_group_id_example'; // string

try {
    $result = $apiInstance->listPriceTiers($page, $page_size, $product_id, $customer_group_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PriceTierApi->listPriceTiers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **product_id** | **string**|  | [optional] |
| **customer_group_id** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PriceTier[]**](../Model/PriceTier.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePriceTier()`

```php
updatePriceTier($price_tier_id, $price_tier_update): \OpenAPI\Client\Model\PriceTier
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PriceTierApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$price_tier_id = 'price_tier_id_example'; // string
$price_tier_update = new \OpenAPI\Client\Model\PriceTierUpdate(); // \OpenAPI\Client\Model\PriceTierUpdate

try {
    $result = $apiInstance->updatePriceTier($price_tier_id, $price_tier_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PriceTierApi->updatePriceTier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **price_tier_id** | **string**|  | |
| **price_tier_update** | [**\OpenAPI\Client\Model\PriceTierUpdate**](../Model/PriceTierUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PriceTier**](../Model/PriceTier.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
