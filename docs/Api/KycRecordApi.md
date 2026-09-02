# OpenAPI\Client\KycRecordApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createKycRecord()**](KycRecordApi.md#createKycRecord) | **POST** /api/v1/kyc-records |  |
| [**deleteKycRecord()**](KycRecordApi.md#deleteKycRecord) | **DELETE** /api/v1/kyc-records/{id} |  |
| [**getKycRecord()**](KycRecordApi.md#getKycRecord) | **GET** /api/v1/kyc-records/{id} |  |
| [**getKycRecords()**](KycRecordApi.md#getKycRecords) | **GET** /api/v1/kyc-records/ |  |
| [**updateKycRecord()**](KycRecordApi.md#updateKycRecord) | **PUT** /api/v1/kyc-records/{id} |  |


## `createKycRecord()`

```php
createKycRecord($kyc_record_create): \OpenAPI\Client\Model\KycRecord
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\KycRecordApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$kyc_record_create = new \OpenAPI\Client\Model\KycRecordCreate(); // \OpenAPI\Client\Model\KycRecordCreate

try {
    $result = $apiInstance->createKycRecord($kyc_record_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KycRecordApi->createKycRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **kyc_record_create** | [**\OpenAPI\Client\Model\KycRecordCreate**](../Model/KycRecordCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\KycRecord**](../Model/KycRecord.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteKycRecord()`

```php
deleteKycRecord($id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\KycRecordApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteKycRecord($id);
} catch (Exception $e) {
    echo 'Exception when calling KycRecordApi->deleteKycRecord: ', $e->getMessage(), PHP_EOL;
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

## `getKycRecord()`

```php
getKycRecord($id): \OpenAPI\Client\Model\KycRecord
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\KycRecordApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getKycRecord($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KycRecordApi->getKycRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\KycRecord**](../Model/KycRecord.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getKycRecords()`

```php
getKycRecords($page, $page_size, $search, $include_deleted): \OpenAPI\Client\Model\KycRecord[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\KycRecordApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 1; // int
$page_size = 56; // int
$search = 'search_example'; // string
$include_deleted = True; // bool | Soft-delete entities: set true to include rows with `deleted_at` set.

try {
    $result = $apiInstance->getKycRecords($page, $page_size, $search, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KycRecordApi->getKycRecords: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **search** | **string**|  | [optional] |
| **include_deleted** | **bool**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] |

### Return type

[**\OpenAPI\Client\Model\KycRecord[]**](../Model/KycRecord.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateKycRecord()`

```php
updateKycRecord($id, $kyc_record_update): \OpenAPI\Client\Model\KycRecord
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\KycRecordApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$kyc_record_update = new \OpenAPI\Client\Model\KycRecordUpdate(); // \OpenAPI\Client\Model\KycRecordUpdate

try {
    $result = $apiInstance->updateKycRecord($id, $kyc_record_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling KycRecordApi->updateKycRecord: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **kyc_record_update** | [**\OpenAPI\Client\Model\KycRecordUpdate**](../Model/KycRecordUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\KycRecord**](../Model/KycRecord.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
