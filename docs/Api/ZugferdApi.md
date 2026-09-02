# OpenAPI\Client\ZugferdApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**generateZugferdApi()**](ZugferdApi.md#generateZugferdApi) | **GET** /api/v1/invoices/{id}/zugferd |  |


## `generateZugferdApi()`

```php
generateZugferdApi($id, $supplier_name, $supplier_street, $supplier_city, $supplier_zip, $supplier_country, $supplier_vat_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ZugferdApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$supplier_name = 'supplier_name_example'; // string
$supplier_street = 'supplier_street_example'; // string
$supplier_city = 'supplier_city_example'; // string
$supplier_zip = 'supplier_zip_example'; // string
$supplier_country = 'supplier_country_example'; // string
$supplier_vat_id = 'supplier_vat_id_example'; // string

try {
    $apiInstance->generateZugferdApi($id, $supplier_name, $supplier_street, $supplier_city, $supplier_zip, $supplier_country, $supplier_vat_id);
} catch (Exception $e) {
    echo 'Exception when calling ZugferdApi->generateZugferdApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **supplier_name** | **string**|  | [optional] |
| **supplier_street** | **string**|  | [optional] |
| **supplier_city** | **string**|  | [optional] |
| **supplier_zip** | **string**|  | [optional] |
| **supplier_country** | **string**|  | [optional] |
| **supplier_vat_id** | **string**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/pdf`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
