# OpenAPI\Client\OnlineshopApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getSmtpConfigApi()**](OnlineshopApi.md#getSmtpConfigApi) | **GET** /api/v1/settings/smtp |  |
| [**saveSmtpConfigApi()**](OnlineshopApi.md#saveSmtpConfigApi) | **PUT** /api/v1/settings/smtp |  |


## `getSmtpConfigApi()`

```php
getSmtpConfigApi(): \OpenAPI\Client\Model\SmtpConfig
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OnlineshopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getSmtpConfigApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OnlineshopApi->getSmtpConfigApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\SmtpConfig**](../Model/SmtpConfig.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `saveSmtpConfigApi()`

```php
saveSmtpConfigApi($smtp_config): \OpenAPI\Client\Model\SmtpConfig
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OnlineshopApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$smtp_config = new \OpenAPI\Client\Model\SmtpConfig(); // \OpenAPI\Client\Model\SmtpConfig

try {
    $result = $apiInstance->saveSmtpConfigApi($smtp_config);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OnlineshopApi->saveSmtpConfigApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **smtp_config** | [**\OpenAPI\Client\Model\SmtpConfig**](../Model/SmtpConfig.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SmtpConfig**](../Model/SmtpConfig.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
