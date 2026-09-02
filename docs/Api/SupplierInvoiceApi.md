# OpenAPI\Client\SupplierInvoiceApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSupplierInvoice()**](SupplierInvoiceApi.md#createSupplierInvoice) | **POST** /api/v1/supplier-invoices |  |
| [**deleteSupplierInvoice()**](SupplierInvoiceApi.md#deleteSupplierInvoice) | **DELETE** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**getSupplierInvoice()**](SupplierInvoiceApi.md#getSupplierInvoice) | **GET** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**listSupplierInvoices()**](SupplierInvoiceApi.md#listSupplierInvoices) | **GET** /api/v1/supplier-invoices/ |  |
| [**updateSupplierInvoice()**](SupplierInvoiceApi.md#updateSupplierInvoice) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id} |  |
| [**updateSupplierInvoiceStatus()**](SupplierInvoiceApi.md#updateSupplierInvoiceStatus) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id}/status |  |


## `createSupplierInvoice()`

```php
createSupplierInvoice($supplier_invoice): \OpenAPI\Client\Model\SupplierInvoice
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_invoice = new \OpenAPI\Client\Model\SupplierInvoice(); // \OpenAPI\Client\Model\SupplierInvoice

try {
    $result = $apiInstance->createSupplierInvoice($supplier_invoice);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->createSupplierInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_invoice** | [**\OpenAPI\Client\Model\SupplierInvoice**](../Model/SupplierInvoice.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoice**](../Model/SupplierInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteSupplierInvoice()`

```php
deleteSupplierInvoice($supplier_invoice_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_invoice_id = 'supplier_invoice_id_example'; // string

try {
    $apiInstance->deleteSupplierInvoice($supplier_invoice_id);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->deleteSupplierInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_invoice_id** | **string**|  | |

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

## `getSupplierInvoice()`

```php
getSupplierInvoice($supplier_invoice_id): \OpenAPI\Client\Model\SupplierInvoice
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_invoice_id = 'supplier_invoice_id_example'; // string

try {
    $result = $apiInstance->getSupplierInvoice($supplier_invoice_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->getSupplierInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_invoice_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoice**](../Model/SupplierInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listSupplierInvoices()`

```php
listSupplierInvoices($page, $page_size, $status, $purchase_order_id, $supplier_name): \OpenAPI\Client\Model\SupplierInvoice[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$status = 'status_example'; // string
$purchase_order_id = 'purchase_order_id_example'; // string
$supplier_name = 'supplier_name_example'; // string

try {
    $result = $apiInstance->listSupplierInvoices($page, $page_size, $status, $purchase_order_id, $supplier_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->listSupplierInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |
| **purchase_order_id** | **string**|  | [optional] |
| **supplier_name** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoice[]**](../Model/SupplierInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSupplierInvoice()`

```php
updateSupplierInvoice($supplier_invoice_id, $body): \OpenAPI\Client\Model\SupplierInvoice
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_invoice_id = 'supplier_invoice_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateSupplierInvoice($supplier_invoice_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->updateSupplierInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_invoice_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoice**](../Model/SupplierInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSupplierInvoiceStatus()`

```php
updateSupplierInvoiceStatus($supplier_invoice_id, $supplier_invoice_status_update): \OpenAPI\Client\Model\SupplierInvoice
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupplierInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$supplier_invoice_id = 'supplier_invoice_id_example'; // string
$supplier_invoice_status_update = new \OpenAPI\Client\Model\SupplierInvoiceStatusUpdate(); // \OpenAPI\Client\Model\SupplierInvoiceStatusUpdate

try {
    $result = $apiInstance->updateSupplierInvoiceStatus($supplier_invoice_id, $supplier_invoice_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupplierInvoiceApi->updateSupplierInvoiceStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **supplier_invoice_id** | **string**|  | |
| **supplier_invoice_status_update** | [**\OpenAPI\Client\Model\SupplierInvoiceStatusUpdate**](../Model/SupplierInvoiceStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SupplierInvoice**](../Model/SupplierInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
