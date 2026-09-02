# OpenAPI\Client\PaymentGatewayApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createPaymentGatewayApi()**](PaymentGatewayApi.md#createPaymentGatewayApi) | **POST** /api/v1/payment-gateways |  |
| [**deletePaymentGatewayApi()**](PaymentGatewayApi.md#deletePaymentGatewayApi) | **DELETE** /api/v1/payment-gateways/{gateway_id} |  |
| [**listPaymentGatewaysApi()**](PaymentGatewayApi.md#listPaymentGatewaysApi) | **GET** /api/v1/payment-gateways/ |  |
| [**oauthAuthorizeApi()**](PaymentGatewayApi.md#oauthAuthorizeApi) | **POST** /api/v1/payment-gateways/oauth/authorize |  |
| [**oauthCallbackApi()**](PaymentGatewayApi.md#oauthCallbackApi) | **POST** /api/v1/payment-gateways/oauth/callback |  |
| [**updatePaymentGatewayApi()**](PaymentGatewayApi.md#updatePaymentGatewayApi) | **PUT** /api/v1/payment-gateways/{gateway_id} |  |


## `createPaymentGatewayApi()`

```php
createPaymentGatewayApi($body): \OpenAPI\Client\Model\PaymentGateway
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentGatewayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = NULL; // mixed

try {
    $result = $apiInstance->createPaymentGatewayApi($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentGatewayApi->createPaymentGatewayApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentGateway**](../Model/PaymentGateway.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deletePaymentGatewayApi()`

```php
deletePaymentGatewayApi($gateway_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentGatewayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gateway_id = 'gateway_id_example'; // string

try {
    $apiInstance->deletePaymentGatewayApi($gateway_id);
} catch (Exception $e) {
    echo 'Exception when calling PaymentGatewayApi->deletePaymentGatewayApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gateway_id** | **string**|  | |

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

## `listPaymentGatewaysApi()`

```php
listPaymentGatewaysApi(): \OpenAPI\Client\Model\PaymentGateway[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentGatewayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listPaymentGatewaysApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentGatewayApi->listPaymentGatewaysApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\PaymentGateway[]**](../Model/PaymentGateway.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `oauthAuthorizeApi()`

```php
oauthAuthorizeApi($gateway_o_auth_authorize_request): \OpenAPI\Client\Model\GatewayOAuthAuthorizeResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentGatewayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gateway_o_auth_authorize_request = new \OpenAPI\Client\Model\GatewayOAuthAuthorizeRequest(); // \OpenAPI\Client\Model\GatewayOAuthAuthorizeRequest

try {
    $result = $apiInstance->oauthAuthorizeApi($gateway_o_auth_authorize_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentGatewayApi->oauthAuthorizeApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gateway_o_auth_authorize_request** | [**\OpenAPI\Client\Model\GatewayOAuthAuthorizeRequest**](../Model/GatewayOAuthAuthorizeRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\GatewayOAuthAuthorizeResponse**](../Model/GatewayOAuthAuthorizeResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `oauthCallbackApi()`

```php
oauthCallbackApi($gateway_o_auth_callback_request): \OpenAPI\Client\Model\PaymentGateway
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentGatewayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gateway_o_auth_callback_request = new \OpenAPI\Client\Model\GatewayOAuthCallbackRequest(); // \OpenAPI\Client\Model\GatewayOAuthCallbackRequest

try {
    $result = $apiInstance->oauthCallbackApi($gateway_o_auth_callback_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentGatewayApi->oauthCallbackApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gateway_o_auth_callback_request** | [**\OpenAPI\Client\Model\GatewayOAuthCallbackRequest**](../Model/GatewayOAuthCallbackRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentGateway**](../Model/PaymentGateway.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updatePaymentGatewayApi()`

```php
updatePaymentGatewayApi($gateway_id, $body): \OpenAPI\Client\Model\PaymentGateway
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\PaymentGatewayApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$gateway_id = 'gateway_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updatePaymentGatewayApi($gateway_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PaymentGatewayApi->updatePaymentGatewayApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **gateway_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\PaymentGateway**](../Model/PaymentGateway.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
