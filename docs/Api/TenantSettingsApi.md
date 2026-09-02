# OpenAPI\Client\TenantSettingsApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getTenantSettings()**](TenantSettingsApi.md#getTenantSettings) | **GET** /api/v1/settings/tenant |  |
| [**updateTenantSettings()**](TenantSettingsApi.md#updateTenantSettings) | **PUT** /api/v1/settings/tenant |  |


## `getTenantSettings()`

```php
getTenantSettings(): \OpenAPI\Client\Model\TenantSettings
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TenantSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getTenantSettings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSettingsApi->getTenantSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\TenantSettings**](../Model/TenantSettings.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTenantSettings()`

```php
updateTenantSettings($update_tenant_settings): \OpenAPI\Client\Model\TenantSettings
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TenantSettingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$update_tenant_settings = new \OpenAPI\Client\Model\UpdateTenantSettings(); // \OpenAPI\Client\Model\UpdateTenantSettings

try {
    $result = $apiInstance->updateTenantSettings($update_tenant_settings);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TenantSettingsApi->updateTenantSettings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **update_tenant_settings** | [**\OpenAPI\Client\Model\UpdateTenantSettings**](../Model/UpdateTenantSettings.md)|  | |

### Return type

[**\OpenAPI\Client\Model\TenantSettings**](../Model/TenantSettings.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
