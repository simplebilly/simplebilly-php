# OpenAPI\Client\EmissionsApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createEmissionEntryApi()**](EmissionsApi.md#createEmissionEntryApi) | **POST** /api/v1/bookkeeping/emissions/entries |  |
| [**createEmissionTargetApi()**](EmissionsApi.md#createEmissionTargetApi) | **POST** /api/v1/bookkeeping/emissions/targets |  |
| [**deleteEmissionEntryApi()**](EmissionsApi.md#deleteEmissionEntryApi) | **DELETE** /api/v1/bookkeeping/emissions/entries/{id} |  |
| [**deleteEmissionTargetApi()**](EmissionsApi.md#deleteEmissionTargetApi) | **DELETE** /api/v1/bookkeeping/emissions/targets/{id} |  |
| [**emissionsEntriesApi()**](EmissionsApi.md#emissionsEntriesApi) | **GET** /api/v1/bookkeeping/emissions/entries |  |
| [**emissionsExportApi()**](EmissionsApi.md#emissionsExportApi) | **GET** /api/v1/bookkeeping/emissions/export |  |
| [**emissionsFactorsApi()**](EmissionsApi.md#emissionsFactorsApi) | **GET** /api/v1/bookkeeping/emissions/factors |  |
| [**emissionsReportApi()**](EmissionsApi.md#emissionsReportApi) | **GET** /api/v1/bookkeeping/emissions/report |  |
| [**emissionsTargetsApi()**](EmissionsApi.md#emissionsTargetsApi) | **GET** /api/v1/bookkeeping/emissions/targets |  |


## `createEmissionEntryApi()`

```php
createEmissionEntryApi($create_emission_entry): \OpenAPI\Client\Model\EmissionEntry
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_emission_entry = new \OpenAPI\Client\Model\CreateEmissionEntry(); // \OpenAPI\Client\Model\CreateEmissionEntry

try {
    $result = $apiInstance->createEmissionEntryApi($create_emission_entry);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->createEmissionEntryApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_emission_entry** | [**\OpenAPI\Client\Model\CreateEmissionEntry**](../Model/CreateEmissionEntry.md)|  | |

### Return type

[**\OpenAPI\Client\Model\EmissionEntry**](../Model/EmissionEntry.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createEmissionTargetApi()`

```php
createEmissionTargetApi($create_emission_target): \OpenAPI\Client\Model\EmissionTarget
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_emission_target = new \OpenAPI\Client\Model\CreateEmissionTarget(); // \OpenAPI\Client\Model\CreateEmissionTarget

try {
    $result = $apiInstance->createEmissionTargetApi($create_emission_target);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->createEmissionTargetApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_emission_target** | [**\OpenAPI\Client\Model\CreateEmissionTarget**](../Model/CreateEmissionTarget.md)|  | |

### Return type

[**\OpenAPI\Client\Model\EmissionTarget**](../Model/EmissionTarget.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteEmissionEntryApi()`

```php
deleteEmissionEntryApi($id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteEmissionEntryApi($id);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->deleteEmissionEntryApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

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

## `deleteEmissionTargetApi()`

```php
deleteEmissionTargetApi($id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteEmissionTargetApi($id);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->deleteEmissionTargetApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

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

## `emissionsEntriesApi()`

```php
emissionsEntriesApi($year): \OpenAPI\Client\Model\EmissionEntry[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int

try {
    $result = $apiInstance->emissionsEntriesApi($year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->emissionsEntriesApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\EmissionEntry[]**](../Model/EmissionEntry.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `emissionsExportApi()`

```php
emissionsExportApi($year): \OpenAPI\Client\Model\EmissionsExportResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int

try {
    $result = $apiInstance->emissionsExportApi($year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->emissionsExportApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\EmissionsExportResponse**](../Model/EmissionsExportResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `emissionsFactorsApi()`

```php
emissionsFactorsApi(): \OpenAPI\Client\Model\EmissionFactorResponse[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->emissionsFactorsApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->emissionsFactorsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\EmissionFactorResponse[]**](../Model/EmissionFactorResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `emissionsReportApi()`

```php
emissionsReportApi($year): \OpenAPI\Client\Model\EmissionsReport
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int

try {
    $result = $apiInstance->emissionsReportApi($year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->emissionsReportApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\EmissionsReport**](../Model/EmissionsReport.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `emissionsTargetsApi()`

```php
emissionsTargetsApi(): \OpenAPI\Client\Model\EmissionTarget[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmissionsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->emissionsTargetsApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmissionsApi->emissionsTargetsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\EmissionTarget[]**](../Model/EmissionTarget.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
