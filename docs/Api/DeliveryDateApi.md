# OpenAPI\Client\DeliveryDateApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDeliveryDate()**](DeliveryDateApi.md#createDeliveryDate) | **POST** /api/v1/delivery-dates |  |
| [**deleteDeliveryDate()**](DeliveryDateApi.md#deleteDeliveryDate) | **DELETE** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**getDeliveryDate()**](DeliveryDateApi.md#getDeliveryDate) | **GET** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**getDeliveryPerformance()**](DeliveryDateApi.md#getDeliveryPerformance) | **GET** /api/v1/delivery-dates/performance | On-time performance summary: how many promised delivery dates were met within a period. |
| [**listDeliveryDates()**](DeliveryDateApi.md#listDeliveryDates) | **GET** /api/v1/delivery-dates/ |  |
| [**updateDeliveryDate()**](DeliveryDateApi.md#updateDeliveryDate) | **PUT** /api/v1/delivery-dates/{delivery_date_id} |  |
| [**updateDeliveryDateStatus()**](DeliveryDateApi.md#updateDeliveryDateStatus) | **PUT** /api/v1/delivery-dates/{delivery_date_id}/status |  |


## `createDeliveryDate()`

```php
createDeliveryDate($delivery_date_create): \OpenAPI\Client\Model\DeliveryDate
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryDateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_date_create = new \OpenAPI\Client\Model\DeliveryDateCreate(); // \OpenAPI\Client\Model\DeliveryDateCreate

try {
    $result = $apiInstance->createDeliveryDate($delivery_date_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryDateApi->createDeliveryDate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_date_create** | [**\OpenAPI\Client\Model\DeliveryDateCreate**](../Model/DeliveryDateCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryDate**](../Model/DeliveryDate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteDeliveryDate()`

```php
deleteDeliveryDate($delivery_date_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryDateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_date_id = 'delivery_date_id_example'; // string

try {
    $apiInstance->deleteDeliveryDate($delivery_date_id);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryDateApi->deleteDeliveryDate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_date_id** | **string**|  | |

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

## `getDeliveryDate()`

```php
getDeliveryDate($delivery_date_id): \OpenAPI\Client\Model\DeliveryDate
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryDateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_date_id = 'delivery_date_id_example'; // string

try {
    $result = $apiInstance->getDeliveryDate($delivery_date_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryDateApi->getDeliveryDate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_date_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryDate**](../Model/DeliveryDate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDeliveryPerformance()`

```php
getDeliveryPerformance($page, $page_size, $order_number, $status, $from, $to): mixed
```

On-time performance summary: how many promised delivery dates were met within a period.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryDateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$order_number = 'order_number_example'; // string
$status = 'status_example'; // string
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Only dates on or after this date.
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Only dates on or before this date.

try {
    $result = $apiInstance->getDeliveryPerformance($page, $page_size, $order_number, $status, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryDateApi->getDeliveryPerformance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **order_number** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **from** | **\DateTime**| Only dates on or after this date. | [optional] |
| **to** | **\DateTime**| Only dates on or before this date. | [optional] |

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

## `listDeliveryDates()`

```php
listDeliveryDates($page, $page_size, $order_number, $status, $from, $to): \OpenAPI\Client\Model\DeliveryDate[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryDateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$order_number = 'order_number_example'; // string
$status = 'status_example'; // string
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Only dates on or after this date.
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Only dates on or before this date.

try {
    $result = $apiInstance->listDeliveryDates($page, $page_size, $order_number, $status, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryDateApi->listDeliveryDates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **order_number** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **from** | **\DateTime**| Only dates on or after this date. | [optional] |
| **to** | **\DateTime**| Only dates on or before this date. | [optional] |

### Return type

[**\OpenAPI\Client\Model\DeliveryDate[]**](../Model/DeliveryDate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDeliveryDate()`

```php
updateDeliveryDate($delivery_date_id, $body): \OpenAPI\Client\Model\DeliveryDate
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryDateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_date_id = 'delivery_date_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateDeliveryDate($delivery_date_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryDateApi->updateDeliveryDate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_date_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryDate**](../Model/DeliveryDate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDeliveryDateStatus()`

```php
updateDeliveryDateStatus($delivery_date_id, $delivery_date_status_update): \OpenAPI\Client\Model\DeliveryDate
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryDateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_date_id = 'delivery_date_id_example'; // string
$delivery_date_status_update = new \OpenAPI\Client\Model\DeliveryDateStatusUpdate(); // \OpenAPI\Client\Model\DeliveryDateStatusUpdate

try {
    $result = $apiInstance->updateDeliveryDateStatus($delivery_date_id, $delivery_date_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryDateApi->updateDeliveryDateStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_date_id** | **string**|  | |
| **delivery_date_status_update** | [**\OpenAPI\Client\Model\DeliveryDateStatusUpdate**](../Model/DeliveryDateStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryDate**](../Model/DeliveryDate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
