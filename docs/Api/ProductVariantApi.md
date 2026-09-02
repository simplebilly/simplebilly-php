# OpenAPI\Client\ProductVariantApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createProductVariant()**](ProductVariantApi.md#createProductVariant) | **POST** /api/v1/product-variants |  |
| [**deleteProductVariant()**](ProductVariantApi.md#deleteProductVariant) | **DELETE** /api/v1/product-variants/{variant_id} |  |
| [**generateProductVariants()**](ProductVariantApi.md#generateProductVariants) | **POST** /api/v1/product-variants/generate |  |
| [**getProductVariant()**](ProductVariantApi.md#getProductVariant) | **GET** /api/v1/product-variants/{variant_id} |  |
| [**listProductVariants()**](ProductVariantApi.md#listProductVariants) | **GET** /api/v1/product-variants/ |  |
| [**updateProductVariant()**](ProductVariantApi.md#updateProductVariant) | **PUT** /api/v1/product-variants/{variant_id} |  |


## `createProductVariant()`

```php
createProductVariant($product_variant): \OpenAPI\Client\Model\ProductVariant
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductVariantApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_variant = new \OpenAPI\Client\Model\ProductVariant(); // \OpenAPI\Client\Model\ProductVariant

try {
    $result = $apiInstance->createProductVariant($product_variant);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductVariantApi->createProductVariant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_variant** | [**\OpenAPI\Client\Model\ProductVariant**](../Model/ProductVariant.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ProductVariant**](../Model/ProductVariant.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteProductVariant()`

```php
deleteProductVariant($variant_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductVariantApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$variant_id = 'variant_id_example'; // string

try {
    $apiInstance->deleteProductVariant($variant_id);
} catch (Exception $e) {
    echo 'Exception when calling ProductVariantApi->deleteProductVariant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **variant_id** | **string**|  | |

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

## `generateProductVariants()`

```php
generateProductVariants($generate_variants_request): \OpenAPI\Client\Model\ProductVariant[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductVariantApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$generate_variants_request = new \OpenAPI\Client\Model\GenerateVariantsRequest(); // \OpenAPI\Client\Model\GenerateVariantsRequest

try {
    $result = $apiInstance->generateProductVariants($generate_variants_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductVariantApi->generateProductVariants: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **generate_variants_request** | [**\OpenAPI\Client\Model\GenerateVariantsRequest**](../Model/GenerateVariantsRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ProductVariant[]**](../Model/ProductVariant.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getProductVariant()`

```php
getProductVariant($variant_id): \OpenAPI\Client\Model\ProductVariant
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductVariantApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$variant_id = 'variant_id_example'; // string

try {
    $result = $apiInstance->getProductVariant($variant_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductVariantApi->getProductVariant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **variant_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ProductVariant**](../Model/ProductVariant.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listProductVariants()`

```php
listProductVariants($page, $page_size, $product_id, $is_active): \OpenAPI\Client\Model\ProductVariant[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductVariantApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$product_id = 'product_id_example'; // string
$is_active = True; // bool

try {
    $result = $apiInstance->listProductVariants($page, $page_size, $product_id, $is_active);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductVariantApi->listProductVariants: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **product_id** | **string**|  | [optional] |
| **is_active** | **bool**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductVariant[]**](../Model/ProductVariant.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateProductVariant()`

```php
updateProductVariant($variant_id, $body): \OpenAPI\Client\Model\ProductVariant
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductVariantApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$variant_id = 'variant_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateProductVariant($variant_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductVariantApi->updateProductVariant: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **variant_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\ProductVariant**](../Model/ProductVariant.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
