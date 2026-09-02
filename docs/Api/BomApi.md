# OpenAPI\Client\BomApi

Bom management. Required permissions: bom:read, bom:write, bom:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createBom()**](BomApi.md#createBom) | **POST** /api/v1/boms |  |
| [**deleteBom()**](BomApi.md#deleteBom) | **DELETE** /api/v1/boms/{bom_id} |  |
| [**getBom()**](BomApi.md#getBom) | **GET** /api/v1/boms/{bom_id} |  |
| [**listBoms()**](BomApi.md#listBoms) | **GET** /api/v1/boms/ |  |
| [**updateBom()**](BomApi.md#updateBom) | **PUT** /api/v1/boms/{bom_id} |  |


## `createBom()`

```php
createBom($bom_create): \OpenAPI\Client\Model\Bom
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BomApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bom_create = new \OpenAPI\Client\Model\BomCreate(); // \OpenAPI\Client\Model\BomCreate

try {
    $result = $apiInstance->createBom($bom_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BomApi->createBom: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bom_create** | [**\OpenAPI\Client\Model\BomCreate**](../Model/BomCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Bom**](../Model/Bom.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteBom()`

```php
deleteBom($bom_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BomApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bom_id = 'bom_id_example'; // string

try {
    $apiInstance->deleteBom($bom_id);
} catch (Exception $e) {
    echo 'Exception when calling BomApi->deleteBom: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bom_id** | **string**|  | |

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

## `getBom()`

```php
getBom($bom_id): \OpenAPI\Client\Model\Bom
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BomApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bom_id = 'bom_id_example'; // string

try {
    $result = $apiInstance->getBom($bom_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BomApi->getBom: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bom_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Bom**](../Model/Bom.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listBoms()`

```php
listBoms($page, $page_size, $search, $product_id): \OpenAPI\Client\Model\Bom[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BomApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$search = 'search_example'; // string
$product_id = 'product_id_example'; // string | Filter by finished product id.

try {
    $result = $apiInstance->listBoms($page, $page_size, $search, $product_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BomApi->listBoms: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **search** | **string**|  | [optional] |
| **product_id** | **string**| Filter by finished product id. | [optional] |

### Return type

[**\OpenAPI\Client\Model\Bom[]**](../Model/Bom.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateBom()`

```php
updateBom($bom_id, $bom_update): \OpenAPI\Client\Model\Bom
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BomApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bom_id = 'bom_id_example'; // string
$bom_update = new \OpenAPI\Client\Model\BomUpdate(); // \OpenAPI\Client\Model\BomUpdate

try {
    $result = $apiInstance->updateBom($bom_id, $bom_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BomApi->updateBom: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bom_id** | **string**|  | |
| **bom_update** | [**\OpenAPI\Client\Model\BomUpdate**](../Model/BomUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Bom**](../Model/Bom.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
