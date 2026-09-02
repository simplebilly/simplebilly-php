# OpenAPI\Client\ReportsApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**bilanzReportApi()**](ReportsApi.md#bilanzReportApi) | **GET** /api/v1/bookkeeping/reports/bilanz | Bilanz (Balance Sheet) |
| [**guvReportApi()**](ReportsApi.md#guvReportApi) | **GET** /api/v1/bookkeeping/reports/guv | Gewinn- und Verlustrechnung (P&amp;L statement) |
| [**kontenansichtReportApi()**](ReportsApi.md#kontenansichtReportApi) | **GET** /api/v1/bookkeeping/reports/kontenansicht | Kontenansicht (Account Overview) |
| [**umsatzsteuerReportApi()**](ReportsApi.md#umsatzsteuerReportApi) | **GET** /api/v1/bookkeeping/reports/umsatzsteuer | Umsatzsteuer-Voranmeldung (VAT report) |


## `bilanzReportApi()`

```php
bilanzReportApi($year, $month, $date_from, $date_to, $page, $page_size): \OpenAPI\Client\Model\BilanzReport
```

Bilanz (Balance Sheet)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$month = 56; // int
$date_from = 'date_from_example'; // string
$date_to = 'date_to_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->bilanzReportApi($year, $month, $date_from, $date_to, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->bilanzReportApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | [optional] |
| **month** | **int**|  | [optional] |
| **date_from** | **string**|  | [optional] |
| **date_to** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\BilanzReport**](../Model/BilanzReport.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `guvReportApi()`

```php
guvReportApi($year, $month, $date_from, $date_to, $page, $page_size): \OpenAPI\Client\Model\GuVReport
```

Gewinn- und Verlustrechnung (P&L statement)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$month = 56; // int
$date_from = 'date_from_example'; // string
$date_to = 'date_to_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->guvReportApi($year, $month, $date_from, $date_to, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->guvReportApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | [optional] |
| **month** | **int**|  | [optional] |
| **date_from** | **string**|  | [optional] |
| **date_to** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GuVReport**](../Model/GuVReport.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `kontenansichtReportApi()`

```php
kontenansichtReportApi($year, $month, $date_from, $date_to, $page, $page_size): \OpenAPI\Client\Model\KontoReport
```

Kontenansicht (Account Overview)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$month = 56; // int
$date_from = 'date_from_example'; // string
$date_to = 'date_to_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->kontenansichtReportApi($year, $month, $date_from, $date_to, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->kontenansichtReportApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | [optional] |
| **month** | **int**|  | [optional] |
| **date_from** | **string**|  | [optional] |
| **date_to** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\KontoReport**](../Model/KontoReport.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `umsatzsteuerReportApi()`

```php
umsatzsteuerReportApi($year, $month, $date_from, $date_to, $page, $page_size): \OpenAPI\Client\Model\UmsatzsteuerReport
```

Umsatzsteuer-Voranmeldung (VAT report)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ReportsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$month = 56; // int
$date_from = 'date_from_example'; // string
$date_to = 'date_to_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->umsatzsteuerReportApi($year, $month, $date_from, $date_to, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReportsApi->umsatzsteuerReportApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | [optional] |
| **month** | **int**|  | [optional] |
| **date_from** | **string**|  | [optional] |
| **date_to** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\UmsatzsteuerReport**](../Model/UmsatzsteuerReport.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
