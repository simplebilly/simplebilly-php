# OpenAPI\Client\SupplierConditionApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSupplierCondition()**](SupplierConditionApi.md#createSupplierCondition) | **POST** /api/v1/supplier-conditions |  |
| [**deleteSupplierCondition()**](SupplierConditionApi.md#deleteSupplierCondition) | **DELETE** /api/v1/supplier-conditions/{supplier_condition_id} |  |
| [**getSupplierCondition()**](SupplierConditionApi.md#getSupplierCondition) | **GET** /api/v1/supplier-conditions/{supplier_condition_id} |  |
| [**listSupplierConditions()**](SupplierConditionApi.md#listSupplierConditions) | **GET** /api/v1/supplier-conditions/ |  |
| [**updateSupplierCondition()**](SupplierConditionApi.md#updateSupplierCondition) | **PUT** /api/v1/supplier-conditions/{supplier_condition_id} |  |


## `createSupplierCondition()`

```php
createSupplierCondition($supplier_condition_create): \OpenAPI\Client\Model\SupplierCondition
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierConditionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_condition_create = new \OpenAPI\Client\Model\SupplierConditionCreate(); // \OpenAPI\Client\Model\SupplierConditionCreate

try {
    $result = $apiInstance->createSupplierCondition($supplier_condition_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierConditionApi->createSupplierCondition: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_condition_create** | [**\OpenAPI\Client\Model\SupplierConditionCreate**](../Model/SupplierConditionCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SupplierCondition**](../Model/SupplierCondition.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteSupplierCondition()`

```php
deleteSupplierCondition($supplier_condition_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierConditionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_condition_id = 'supplier_condition_id_example'; // string

try {
    $apiInstance->deleteSupplierCondition($supplier_condition_id);
} catch (Exception $e) {
    echo 'Exception when calling SupplierConditionApi->deleteSupplierCondition: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_condition_id** | **string**|  | |

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

## `getSupplierCondition()`

```php
getSupplierCondition($supplier_condition_id): \OpenAPI\Client\Model\SupplierCondition
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierConditionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_condition_id = 'supplier_condition_id_example'; // string

try {
    $result = $apiInstance->getSupplierCondition($supplier_condition_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierConditionApi->getSupplierCondition: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_condition_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SupplierCondition**](../Model/SupplierCondition.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listSupplierConditions()`

```php
listSupplierConditions($page, $page_size, $supplier_contact_id, $search): \OpenAPI\Client\Model\SupplierCondition[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierConditionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$supplier_contact_id = 'supplier_contact_id_example'; // string
$search = 'search_example'; // string

try {
    $result = $apiInstance->listSupplierConditions($page, $page_size, $supplier_contact_id, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierConditionApi->listSupplierConditions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **supplier_contact_id** | **string**|  | [optional] |
| **search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SupplierCondition[]**](../Model/SupplierCondition.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSupplierCondition()`

```php
updateSupplierCondition($supplier_condition_id, $supplier_condition_update): \OpenAPI\Client\Model\SupplierCondition
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierConditionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_condition_id = 'supplier_condition_id_example'; // string
$supplier_condition_update = new \OpenAPI\Client\Model\SupplierConditionUpdate(); // \OpenAPI\Client\Model\SupplierConditionUpdate

try {
    $result = $apiInstance->updateSupplierCondition($supplier_condition_id, $supplier_condition_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierConditionApi->updateSupplierCondition: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_condition_id** | **string**|  | |
| **supplier_condition_update** | [**\OpenAPI\Client\Model\SupplierConditionUpdate**](../Model/SupplierConditionUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SupplierCondition**](../Model/SupplierCondition.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
