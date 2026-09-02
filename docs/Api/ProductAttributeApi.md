# OpenAPI\Client\ProductAttributeApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createProductAttribute()**](ProductAttributeApi.md#createProductAttribute) | **POST** /api/v1/product-attributes |  |
| [**deleteProductAttribute()**](ProductAttributeApi.md#deleteProductAttribute) | **DELETE** /api/v1/product-attributes/{attribute_id} |  |
| [**getProductAttribute()**](ProductAttributeApi.md#getProductAttribute) | **GET** /api/v1/product-attributes/{attribute_id} |  |
| [**listProductAttributes()**](ProductAttributeApi.md#listProductAttributes) | **GET** /api/v1/product-attributes/ |  |
| [**updateProductAttribute()**](ProductAttributeApi.md#updateProductAttribute) | **PUT** /api/v1/product-attributes/{attribute_id} |  |


## `createProductAttribute()`

```php
createProductAttribute($product_attribute_create): \OpenAPI\Client\Model\ProductAttribute
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductAttributeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$product_attribute_create = new \OpenAPI\Client\Model\ProductAttributeCreate(); // \OpenAPI\Client\Model\ProductAttributeCreate

try {
    $result = $apiInstance->createProductAttribute($product_attribute_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAttributeApi->createProductAttribute: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **product_attribute_create** | [**\OpenAPI\Client\Model\ProductAttributeCreate**](../Model/ProductAttributeCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ProductAttribute**](../Model/ProductAttribute.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteProductAttribute()`

```php
deleteProductAttribute($attribute_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductAttributeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$attribute_id = 'attribute_id_example'; // string

try {
    $apiInstance->deleteProductAttribute($attribute_id);
} catch (Exception $e) {
    echo 'Exception when calling ProductAttributeApi->deleteProductAttribute: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attribute_id** | **string**|  | |

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

## `getProductAttribute()`

```php
getProductAttribute($attribute_id): \OpenAPI\Client\Model\ProductAttribute
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductAttributeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$attribute_id = 'attribute_id_example'; // string

try {
    $result = $apiInstance->getProductAttribute($attribute_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAttributeApi->getProductAttribute: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attribute_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ProductAttribute**](../Model/ProductAttribute.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listProductAttributes()`

```php
listProductAttributes($page, $page_size, $product_id, $is_filterable, $search): \OpenAPI\Client\Model\ProductAttribute[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductAttributeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$product_id = 'product_id_example'; // string
$is_filterable = True; // bool
$search = 'search_example'; // string

try {
    $result = $apiInstance->listProductAttributes($page, $page_size, $product_id, $is_filterable, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAttributeApi->listProductAttributes: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **product_id** | **string**|  | [optional] |
| **is_filterable** | **bool**|  | [optional] |
| **search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProductAttribute[]**](../Model/ProductAttribute.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateProductAttribute()`

```php
updateProductAttribute($attribute_id, $product_attribute_update): \OpenAPI\Client\Model\ProductAttribute
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProductAttributeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$attribute_id = 'attribute_id_example'; // string
$product_attribute_update = new \OpenAPI\Client\Model\ProductAttributeUpdate(); // \OpenAPI\Client\Model\ProductAttributeUpdate

try {
    $result = $apiInstance->updateProductAttribute($attribute_id, $product_attribute_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProductAttributeApi->updateProductAttribute: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attribute_id** | **string**|  | |
| **product_attribute_update** | [**\OpenAPI\Client\Model\ProductAttributeUpdate**](../Model/ProductAttributeUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ProductAttribute**](../Model/ProductAttribute.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
