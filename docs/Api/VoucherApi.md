# OpenAPI\Client\VoucherApi

Voucher management. Required permissions: voucher:read, voucher:write, voucher:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createVoucher()**](VoucherApi.md#createVoucher) | **POST** /api/v1/vouchers |  |
| [**deleteVoucher()**](VoucherApi.md#deleteVoucher) | **DELETE** /api/v1/vouchers/{voucher_id} |  |
| [**getVoucher()**](VoucherApi.md#getVoucher) | **GET** /api/v1/vouchers/{voucher_id} |  |
| [**listVouchers()**](VoucherApi.md#listVouchers) | **GET** /api/v1/vouchers/ |  |
| [**updateVoucher()**](VoucherApi.md#updateVoucher) | **PUT** /api/v1/vouchers/{voucher_id} |  |
| [**voucherRestore()**](VoucherApi.md#voucherRestore) | **POST** /api/v1/vouchers/{voucher_id}/restore |  |


## `createVoucher()`

```php
createVoucher($voucher_create): \OpenAPI\Client\Model\Voucher
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\VoucherApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$voucher_create = new \OpenAPI\Client\Model\VoucherCreate(); // \OpenAPI\Client\Model\VoucherCreate

try {
    $result = $apiInstance->createVoucher($voucher_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherApi->createVoucher: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **voucher_create** | [**\OpenAPI\Client\Model\VoucherCreate**](../Model/VoucherCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Voucher**](../Model/Voucher.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteVoucher()`

```php
deleteVoucher($voucher_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\VoucherApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$voucher_id = 'voucher_id_example'; // string

try {
    $apiInstance->deleteVoucher($voucher_id);
} catch (Exception $e) {
    echo 'Exception when calling VoucherApi->deleteVoucher: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **voucher_id** | **string**|  | |

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

## `getVoucher()`

```php
getVoucher($voucher_id): \OpenAPI\Client\Model\Voucher
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\VoucherApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$voucher_id = 'voucher_id_example'; // string

try {
    $result = $apiInstance->getVoucher($voucher_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherApi->getVoucher: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **voucher_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Voucher**](../Model/Voucher.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listVouchers()`

```php
listVouchers($page, $page_size, $voucher_type, $voucher_status, $contact_name, $date_from, $date_to): \OpenAPI\Client\Model\Voucher[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\VoucherApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$voucher_type = 'voucher_type_example'; // string
$voucher_status = 'voucher_status_example'; // string
$contact_name = 'contact_name_example'; // string
$date_from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$date_to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime

try {
    $result = $apiInstance->listVouchers($page, $page_size, $voucher_type, $voucher_status, $contact_name, $date_from, $date_to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherApi->listVouchers: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **voucher_type** | **string**|  | [optional] |
| **voucher_status** | **string**|  | [optional] |
| **contact_name** | **string**|  | [optional] |
| **date_from** | **\DateTime**|  | [optional] |
| **date_to** | **\DateTime**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Voucher[]**](../Model/Voucher.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateVoucher()`

```php
updateVoucher($voucher_id, $body): \OpenAPI\Client\Model\Voucher
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\VoucherApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$voucher_id = 'voucher_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateVoucher($voucher_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherApi->updateVoucher: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **voucher_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\Voucher**](../Model/Voucher.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `voucherRestore()`

```php
voucherRestore($voucher_id): \OpenAPI\Client\Model\Voucher
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\VoucherApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$voucher_id = 'voucher_id_example'; // string

try {
    $result = $apiInstance->voucherRestore($voucher_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VoucherApi->voucherRestore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **voucher_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Voucher**](../Model/Voucher.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
