# OpenAPI\Client\SilentPartnerApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSilentPartner()**](SilentPartnerApi.md#createSilentPartner) | **POST** /api/v1/silent-partners |  |
| [**deleteSilentPartner()**](SilentPartnerApi.md#deleteSilentPartner) | **DELETE** /api/v1/silent-partners/{id} |  |
| [**getSilentPartner()**](SilentPartnerApi.md#getSilentPartner) | **GET** /api/v1/silent-partners/{id} |  |
| [**getSilentPartners()**](SilentPartnerApi.md#getSilentPartners) | **GET** /api/v1/silent-partners/ |  |
| [**updateSilentPartner()**](SilentPartnerApi.md#updateSilentPartner) | **PUT** /api/v1/silent-partners/{id} |  |


## `createSilentPartner()`

```php
createSilentPartner($silent_partner_create): \OpenAPI\Client\Model\SilentPartner
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SilentPartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$silent_partner_create = new \OpenAPI\Client\Model\SilentPartnerCreate(); // \OpenAPI\Client\Model\SilentPartnerCreate

try {
    $result = $apiInstance->createSilentPartner($silent_partner_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SilentPartnerApi->createSilentPartner: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **silent_partner_create** | [**\OpenAPI\Client\Model\SilentPartnerCreate**](../Model/SilentPartnerCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SilentPartner**](../Model/SilentPartner.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteSilentPartner()`

```php
deleteSilentPartner($id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SilentPartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteSilentPartner($id);
} catch (Exception $e) {
    echo 'Exception when calling SilentPartnerApi->deleteSilentPartner: ', $e->getMessage(), PHP_EOL;
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

## `getSilentPartner()`

```php
getSilentPartner($id): \OpenAPI\Client\Model\SilentPartner
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SilentPartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getSilentPartner($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SilentPartnerApi->getSilentPartner: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SilentPartner**](../Model/SilentPartner.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSilentPartners()`

```php
getSilentPartners($page, $page_size, $search, $include_deleted): \OpenAPI\Client\Model\SilentPartner[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SilentPartnerApi(
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
    $result = $apiInstance->getSilentPartners($page, $page_size, $search, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SilentPartnerApi->getSilentPartners: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\SilentPartner[]**](../Model/SilentPartner.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSilentPartner()`

```php
updateSilentPartner($id, $silent_partner_update): \OpenAPI\Client\Model\SilentPartner
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SilentPartnerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$silent_partner_update = new \OpenAPI\Client\Model\SilentPartnerUpdate(); // \OpenAPI\Client\Model\SilentPartnerUpdate

try {
    $result = $apiInstance->updateSilentPartner($id, $silent_partner_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SilentPartnerApi->updateSilentPartner: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **silent_partner_update** | [**\OpenAPI\Client\Model\SilentPartnerUpdate**](../Model/SilentPartnerUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SilentPartner**](../Model/SilentPartner.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
