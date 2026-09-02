# OpenAPI\Client\OrderConfirmationApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createConfirmation()**](OrderConfirmationApi.md#createConfirmation) | **POST** /api/v1/order-confirmations |  |
| [**deleteConfirmation()**](OrderConfirmationApi.md#deleteConfirmation) | **DELETE** /api/v1/order-confirmations/{confirmation_id} |  |
| [**downloadConfirmationPdf()**](OrderConfirmationApi.md#downloadConfirmationPdf) | **GET** /api/v1/order-confirmations/{confirmation_id}/pdf |  |
| [**getConfirmation()**](OrderConfirmationApi.md#getConfirmation) | **GET** /api/v1/order-confirmations/{confirmation_id} |  |
| [**listConfirmations()**](OrderConfirmationApi.md#listConfirmations) | **GET** /api/v1/order-confirmations/ |  |
| [**orderconfirmationRestore()**](OrderConfirmationApi.md#orderconfirmationRestore) | **POST** /api/v1/order-confirmations/{confirmation_id}/restore |  |
| [**pursueConfirmation()**](OrderConfirmationApi.md#pursueConfirmation) | **POST** /api/v1/order-confirmations/{confirmation_id}/pursue |  |


## `createConfirmation()`

```php
createConfirmation($order_confirmation_create): \OpenAPI\Client\Model\OrderConfirmation
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderConfirmationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_confirmation_create = new \OpenAPI\Client\Model\OrderConfirmationCreate(); // \OpenAPI\Client\Model\OrderConfirmationCreate

try {
    $result = $apiInstance->createConfirmation($order_confirmation_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderConfirmationApi->createConfirmation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_confirmation_create** | [**\OpenAPI\Client\Model\OrderConfirmationCreate**](../Model/OrderConfirmationCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\OrderConfirmation**](../Model/OrderConfirmation.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteConfirmation()`

```php
deleteConfirmation($confirmation_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderConfirmationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$confirmation_id = 'confirmation_id_example'; // string

try {
    $apiInstance->deleteConfirmation($confirmation_id);
} catch (Exception $e) {
    echo 'Exception when calling OrderConfirmationApi->deleteConfirmation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **confirmation_id** | **string**|  | |

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

## `downloadConfirmationPdf()`

```php
downloadConfirmationPdf($confirmation_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderConfirmationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$confirmation_id = 'confirmation_id_example'; // string

try {
    $apiInstance->downloadConfirmationPdf($confirmation_id);
} catch (Exception $e) {
    echo 'Exception when calling OrderConfirmationApi->downloadConfirmationPdf: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **confirmation_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/pdf`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConfirmation()`

```php
getConfirmation($confirmation_id): \OpenAPI\Client\Model\OrderConfirmation
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderConfirmationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$confirmation_id = 'confirmation_id_example'; // string

try {
    $result = $apiInstance->getConfirmation($confirmation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderConfirmationApi->getConfirmation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **confirmation_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\OrderConfirmation**](../Model/OrderConfirmation.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listConfirmations()`

```php
listConfirmations($page, $page_size, $search, $include_deleted): \OpenAPI\Client\Model\OrderConfirmation[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderConfirmationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$page_size = 56; // int
$search = 'search_example'; // string
$include_deleted = True; // bool | Soft-delete entities: set true to include rows with `deleted_at` set.

try {
    $result = $apiInstance->listConfirmations($page, $page_size, $search, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderConfirmationApi->listConfirmations: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **search** | **string**|  | [optional] |
| **include_deleted** | **bool**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] |

### Return type

[**\OpenAPI\Client\Model\OrderConfirmation[]**](../Model/OrderConfirmation.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `orderconfirmationRestore()`

```php
orderconfirmationRestore($confirmation_id): \OpenAPI\Client\Model\OrderConfirmation
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderConfirmationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$confirmation_id = 'confirmation_id_example'; // string

try {
    $result = $apiInstance->orderconfirmationRestore($confirmation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderConfirmationApi->orderconfirmationRestore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **confirmation_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\OrderConfirmation**](../Model/OrderConfirmation.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pursueConfirmation()`

```php
pursueConfirmation($confirmation_id): \OpenAPI\Client\Model\DeliveryNote
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OrderConfirmationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$confirmation_id = 'confirmation_id_example'; // string

try {
    $result = $apiInstance->pursueConfirmation($confirmation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderConfirmationApi->pursueConfirmation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **confirmation_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryNote**](../Model/DeliveryNote.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
