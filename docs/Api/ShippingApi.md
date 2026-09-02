# OpenAPI\Client\ShippingApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getCredentialsApi()**](ShippingApi.md#getCredentialsApi) | **GET** /api/v1/shipping/credentials |  |
| [**getRatesApi()**](ShippingApi.md#getRatesApi) | **POST** /api/v1/shipping/rates |  |
| [**listProvidersApi()**](ShippingApi.md#listProvidersApi) | **GET** /api/v1/shipping/providers |  |
| [**saveCredentialsApi()**](ShippingApi.md#saveCredentialsApi) | **PUT** /api/v1/shipping/credentials |  |


## `getCredentialsApi()`

```php
getCredentialsApi(): \OpenAPI\Client\Model\ShippingCredentials
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getCredentialsApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->getCredentialsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ShippingCredentials**](../Model/ShippingCredentials.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getRatesApi()`

```php
getRatesApi($rate_request): \OpenAPI\Client\Model\RateResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rate_request = new \OpenAPI\Client\Model\RateRequest(); // \OpenAPI\Client\Model\RateRequest

try {
    $result = $apiInstance->getRatesApi($rate_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->getRatesApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rate_request** | [**\OpenAPI\Client\Model\RateRequest**](../Model/RateRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\RateResponse**](../Model/RateResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listProvidersApi()`

```php
listProvidersApi(): \OpenAPI\Client\Model\ProviderInfo[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listProvidersApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->listProvidersApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\ProviderInfo[]**](../Model/ProviderInfo.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `saveCredentialsApi()`

```php
saveCredentialsApi($shipping_credentials): \OpenAPI\Client\Model\ShippingCredentials
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipping_credentials = new \OpenAPI\Client\Model\ShippingCredentials(); // \OpenAPI\Client\Model\ShippingCredentials

try {
    $result = $apiInstance->saveCredentialsApi($shipping_credentials);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingApi->saveCredentialsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipping_credentials** | [**\OpenAPI\Client\Model\ShippingCredentials**](../Model/ShippingCredentials.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ShippingCredentials**](../Model/ShippingCredentials.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
