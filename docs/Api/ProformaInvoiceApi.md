# OpenAPI\Client\ProformaInvoiceApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**convertProformaToInvoice()**](ProformaInvoiceApi.md#convertProformaToInvoice) | **POST** /api/v1/proforma-invoices/{proforma_id}/convert |  |
| [**createProformaInvoice()**](ProformaInvoiceApi.md#createProformaInvoice) | **POST** /api/v1/proforma-invoices |  |
| [**deleteProformaInvoice()**](ProformaInvoiceApi.md#deleteProformaInvoice) | **DELETE** /api/v1/proforma-invoices/{proforma_id} |  |
| [**getProformaInvoice()**](ProformaInvoiceApi.md#getProformaInvoice) | **GET** /api/v1/proforma-invoices/{proforma_id} |  |
| [**listProformaInvoices()**](ProformaInvoiceApi.md#listProformaInvoices) | **GET** /api/v1/proforma-invoices/ |  |
| [**updateProformaInvoice()**](ProformaInvoiceApi.md#updateProformaInvoice) | **PUT** /api/v1/proforma-invoices/{proforma_id} |  |


## `convertProformaToInvoice()`

```php
convertProformaToInvoice($proforma_id): \OpenAPI\Client\Model\ConvertResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProformaInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$proforma_id = 'proforma_id_example'; // string

try {
    $result = $apiInstance->convertProformaToInvoice($proforma_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProformaInvoiceApi->convertProformaToInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **proforma_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ConvertResponse**](../Model/ConvertResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createProformaInvoice()`

```php
createProformaInvoice($proforma_invoice): \OpenAPI\Client\Model\ProformaInvoice
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProformaInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$proforma_invoice = new \OpenAPI\Client\Model\ProformaInvoice(); // \OpenAPI\Client\Model\ProformaInvoice

try {
    $result = $apiInstance->createProformaInvoice($proforma_invoice);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProformaInvoiceApi->createProformaInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **proforma_invoice** | [**\OpenAPI\Client\Model\ProformaInvoice**](../Model/ProformaInvoice.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ProformaInvoice**](../Model/ProformaInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteProformaInvoice()`

```php
deleteProformaInvoice($proforma_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProformaInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$proforma_id = 'proforma_id_example'; // string

try {
    $apiInstance->deleteProformaInvoice($proforma_id);
} catch (Exception $e) {
    echo 'Exception when calling ProformaInvoiceApi->deleteProformaInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **proforma_id** | **string**|  | |

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

## `getProformaInvoice()`

```php
getProformaInvoice($proforma_id): \OpenAPI\Client\Model\ProformaInvoice
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProformaInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$proforma_id = 'proforma_id_example'; // string

try {
    $result = $apiInstance->getProformaInvoice($proforma_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProformaInvoiceApi->getProformaInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **proforma_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ProformaInvoice**](../Model/ProformaInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listProformaInvoices()`

```php
listProformaInvoices($page, $page_size, $status, $customer_id, $order_number): \OpenAPI\Client\Model\ProformaInvoice[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProformaInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$status = 'status_example'; // string
$customer_id = 'customer_id_example'; // string
$order_number = 'order_number_example'; // string

try {
    $result = $apiInstance->listProformaInvoices($page, $page_size, $status, $customer_id, $order_number);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProformaInvoiceApi->listProformaInvoices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |
| **customer_id** | **string**|  | [optional] |
| **order_number** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ProformaInvoice[]**](../Model/ProformaInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateProformaInvoice()`

```php
updateProformaInvoice($proforma_id, $body): \OpenAPI\Client\Model\ProformaInvoice
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ProformaInvoiceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$proforma_id = 'proforma_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateProformaInvoice($proforma_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ProformaInvoiceApi->updateProformaInvoice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **proforma_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\ProformaInvoice**](../Model/ProformaInvoice.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
