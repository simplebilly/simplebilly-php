# OpenAPI\Client\DatevApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**datevExportApi()**](DatevApi.md#datevExportApi) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV |
| [**datevPreviewApi()**](DatevApi.md#datevPreviewApi) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review |


## `datevExportApi()`

```php
datevExportApi($account_schema, $date_from, $date_to, $page, $page_size): \OpenAPI\Client\Model\DatevExportResponse
```

Export bookkeeping data as DATEV CSV

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DatevApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_schema = 'account_schema_example'; // string
$date_from = 'date_from_example'; // string
$date_to = 'date_to_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->datevExportApi($account_schema, $date_from, $date_to, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DatevApi->datevExportApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_schema** | **string**|  | [optional] |
| **date_from** | **string**|  | [optional] |
| **date_to** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DatevExportResponse**](../Model/DatevExportResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `datevPreviewApi()`

```php
datevPreviewApi($account_schema, $date_from, $date_to, $page, $page_size): \OpenAPI\Client\Model\DatevBookingPreview[]
```

Exported_datev_bookings: returns formed bookings for review

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DatevApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$account_schema = 'account_schema_example'; // string
$date_from = 'date_from_example'; // string
$date_to = 'date_to_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->datevPreviewApi($account_schema, $date_from, $date_to, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DatevApi->datevPreviewApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **account_schema** | **string**|  | [optional] |
| **date_from** | **string**|  | [optional] |
| **date_to** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DatevBookingPreview[]**](../Model/DatevBookingPreview.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
