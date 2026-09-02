# OpenAPI\Client\PublicReturnsApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getPublicReturnStatus()**](PublicReturnsApi.md#getPublicReturnStatus) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches. |
| [**listPublicReturns()**](PublicReturnsApi.md#listPublicReturns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth). |
| [**requestPublicReturn()**](PublicReturnsApi.md#requestPublicReturn) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth). |


## `getPublicReturnStatus()`

```php
getPublicReturnStatus($email, $return_number, $return_order_id, $order_number): \OpenAPI\Client\Model\PublicReturnStatusResponse
```

Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PublicReturnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email = 'email_example'; // string
$return_number = 'return_number_example'; // string | Either return_number or return_order_id must be provided.
$return_order_id = 'return_order_id_example'; // string
$order_number = 'order_number_example'; // string

try {
    $result = $apiInstance->getPublicReturnStatus($email, $return_number, $return_order_id, $order_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicReturnsApi->getPublicReturnStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email** | **string**|  | |
| **return_number** | **string**| Either return_number or return_order_id must be provided. | [optional] |
| **return_order_id** | **string**|  | [optional] |
| **order_number** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\PublicReturnStatusResponse**](../Model/PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPublicReturns()`

```php
listPublicReturns($order_number, $email): \OpenAPI\Client\Model\PublicReturnStatusResponse[]
```

List all returns for an order (public, no auth).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PublicReturnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_number = 'order_number_example'; // string
$email = 'email_example'; // string

try {
    $result = $apiInstance->listPublicReturns($order_number, $email);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicReturnsApi->listPublicReturns: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_number** | **string**|  | |
| **email** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PublicReturnStatusResponse[]**](../Model/PublicReturnStatusResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `requestPublicReturn()`

```php
requestPublicReturn($public_return_request): \OpenAPI\Client\Model\PublicReturnResponse
```

Customer requests a return for an order (public, no auth).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PublicReturnsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$public_return_request = new \OpenAPI\Client\Model\PublicReturnRequest(); // \OpenAPI\Client\Model\PublicReturnRequest

try {
    $result = $apiInstance->requestPublicReturn($public_return_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PublicReturnsApi->requestPublicReturn: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **public_return_request** | [**\OpenAPI\Client\Model\PublicReturnRequest**](../Model/PublicReturnRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PublicReturnResponse**](../Model/PublicReturnResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
