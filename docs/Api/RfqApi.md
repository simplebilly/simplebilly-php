# OpenAPI\Client\RfqApi

Rfq management. Required permissions: rfq:read, rfq:write, rfq:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**convertRfq()**](RfqApi.md#convertRfq) | **POST** /api/v1/rfqs/{rfq_id}/convert | Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as &#x60;converted&#x60;. |
| [**createRfq()**](RfqApi.md#createRfq) | **POST** /api/v1/rfqs |  |
| [**deleteRfq()**](RfqApi.md#deleteRfq) | **DELETE** /api/v1/rfqs/{rfq_id} |  |
| [**getRfq()**](RfqApi.md#getRfq) | **GET** /api/v1/rfqs/{rfq_id} |  |
| [**listRfqs()**](RfqApi.md#listRfqs) | **GET** /api/v1/rfqs/ |  |
| [**updateRfq()**](RfqApi.md#updateRfq) | **PUT** /api/v1/rfqs/{rfq_id} |  |
| [**updateRfqStatus()**](RfqApi.md#updateRfqStatus) | **PUT** /api/v1/rfqs/{rfq_id}/status |  |


## `convertRfq()`

```php
convertRfq($rfq_id): mixed
```

Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RfqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rfq_id = 'rfq_id_example'; // string

try {
    $result = $apiInstance->convertRfq($rfq_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RfqApi->convertRfq: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rfq_id** | **string**|  | |

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

## `createRfq()`

```php
createRfq($rfq): \OpenAPI\Client\Model\Rfq
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RfqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rfq = new \OpenAPI\Client\Model\Rfq(); // \OpenAPI\Client\Model\Rfq

try {
    $result = $apiInstance->createRfq($rfq);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RfqApi->createRfq: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rfq** | [**\OpenAPI\Client\Model\Rfq**](../Model/Rfq.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Rfq**](../Model/Rfq.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteRfq()`

```php
deleteRfq($rfq_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RfqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rfq_id = 'rfq_id_example'; // string

try {
    $apiInstance->deleteRfq($rfq_id);
} catch (Exception $e) {
    echo 'Exception when calling RfqApi->deleteRfq: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rfq_id** | **string**|  | |

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

## `getRfq()`

```php
getRfq($rfq_id): \OpenAPI\Client\Model\Rfq
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RfqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rfq_id = 'rfq_id_example'; // string

try {
    $result = $apiInstance->getRfq($rfq_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RfqApi->getRfq: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rfq_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Rfq**](../Model/Rfq.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listRfqs()`

```php
listRfqs($page, $page_size, $status, $supplier_name): \OpenAPI\Client\Model\Rfq[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RfqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$status = 'status_example'; // string
$supplier_name = 'supplier_name_example'; // string

try {
    $result = $apiInstance->listRfqs($page, $page_size, $status, $supplier_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RfqApi->listRfqs: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |
| **supplier_name** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Rfq[]**](../Model/Rfq.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateRfq()`

```php
updateRfq($rfq_id, $body): \OpenAPI\Client\Model\Rfq
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RfqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rfq_id = 'rfq_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateRfq($rfq_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RfqApi->updateRfq: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rfq_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\Rfq**](../Model/Rfq.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateRfqStatus()`

```php
updateRfqStatus($rfq_id, $rfq_status_update): \OpenAPI\Client\Model\Rfq
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\RfqApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rfq_id = 'rfq_id_example'; // string
$rfq_status_update = new \OpenAPI\Client\Model\RfqStatusUpdate(); // \OpenAPI\Client\Model\RfqStatusUpdate

try {
    $result = $apiInstance->updateRfqStatus($rfq_id, $rfq_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RfqApi->updateRfqStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rfq_id** | **string**|  | |
| **rfq_status_update** | [**\OpenAPI\Client\Model\RfqStatusUpdate**](../Model/RfqStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Rfq**](../Model/Rfq.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
