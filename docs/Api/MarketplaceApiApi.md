# OpenAPI\Client\MarketplaceApiApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createConnectionApi()**](MarketplaceApiApi.md#createConnectionApi) | **POST** /api/v1/marketplace/connections | Create a new connection (for API-key based platforms) |
| [**deleteConnectionApi()**](MarketplaceApiApi.md#deleteConnectionApi) | **DELETE** /api/v1/marketplace/connections/{connection_id} | Soft-delete a connection |
| [**getConnectionApi()**](MarketplaceApiApi.md#getConnectionApi) | **GET** /api/v1/marketplace/connections/{connection_id} | Get a single connection |
| [**getSyncDirectionApi()**](MarketplaceApiApi.md#getSyncDirectionApi) | **GET** /api/v1/marketplace/connections/{connection_id}/directions | Get current sync direction configuration for a connection |
| [**getSyncLogsApi()**](MarketplaceApiApi.md#getSyncLogsApi) | **GET** /api/v1/marketplace/connections/{connection_id}/logs | Get sync logs for a connection |
| [**listConnectionsApi()**](MarketplaceApiApi.md#listConnectionsApi) | **GET** /api/v1/marketplace/connections | List connections for the current tenant |
| [**listPlatformsApi()**](MarketplaceApiApi.md#listPlatformsApi) | **GET** /api/v1/marketplace/platforms | List all supported platforms |
| [**oauthAuthorizeApi()**](MarketplaceApiApi.md#oauthAuthorizeApi) | **POST** /api/v1/marketplace/oauth/authorize | OAuth: initiate authorization flow |
| [**oauthCallbackApi()**](MarketplaceApiApi.md#oauthCallbackApi) | **POST** /api/v1/marketplace/oauth/callback | OAuth: handle callback after authorization |
| [**triggerSyncApi()**](MarketplaceApiApi.md#triggerSyncApi) | **POST** /api/v1/marketplace/connections/{connection_id}/sync | Trigger sync for a connection |
| [**updateConnectionApi()**](MarketplaceApiApi.md#updateConnectionApi) | **PUT** /api/v1/marketplace/connections/{connection_id} | Update a connection |
| [**updateSyncDirectionApi()**](MarketplaceApiApi.md#updateSyncDirectionApi) | **PUT** /api/v1/marketplace/connections/{connection_id}/directions | Update per-entity sync direction configuration for a connection |
| [**webhookReceiverApi()**](MarketplaceApiApi.md#webhookReceiverApi) | **POST** /api/v1/marketplace/webhook/{platform}/{connection_id} | Webhook receiver |


## `createConnectionApi()`

```php
createConnectionApi($create_connection_request): \OpenAPI\Client\Model\MarketplaceConnection
```

Create a new connection (for API-key based platforms)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_connection_request = new \OpenAPI\Client\Model\CreateConnectionRequest(); // \OpenAPI\Client\Model\CreateConnectionRequest

try {
    $result = $apiInstance->createConnectionApi($create_connection_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->createConnectionApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_connection_request** | [**\OpenAPI\Client\Model\CreateConnectionRequest**](../Model/CreateConnectionRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\MarketplaceConnection**](../Model/MarketplaceConnection.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteConnectionApi()`

```php
deleteConnectionApi($connection_id)
```

Soft-delete a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_id = 'connection_id_example'; // string

try {
    $apiInstance->deleteConnectionApi($connection_id);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->deleteConnectionApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getConnectionApi()`

```php
getConnectionApi($connection_id): \OpenAPI\Client\Model\MarketplaceConnection
```

Get a single connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_id = 'connection_id_example'; // string

try {
    $result = $apiInstance->getConnectionApi($connection_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->getConnectionApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\MarketplaceConnection**](../Model/MarketplaceConnection.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSyncDirectionApi()`

```php
getSyncDirectionApi($connection_id)
```

Get current sync direction configuration for a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_id = 'connection_id_example'; // string

try {
    $apiInstance->getSyncDirectionApi($connection_id);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->getSyncDirectionApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSyncLogsApi()`

```php
getSyncLogsApi($connection_id): \OpenAPI\Client\Model\SyncLog[]
```

Get sync logs for a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_id = 'connection_id_example'; // string

try {
    $result = $apiInstance->getSyncLogsApi($connection_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->getSyncLogsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SyncLog[]**](../Model/SyncLog.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listConnectionsApi()`

```php
listConnectionsApi(): \OpenAPI\Client\Model\MarketplaceConnection[]
```

List connections for the current tenant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listConnectionsApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->listConnectionsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\MarketplaceConnection[]**](../Model/MarketplaceConnection.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listPlatformsApi()`

```php
listPlatformsApi(): \OpenAPI\Client\Model\PlatformInfo[]
```

List all supported platforms

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listPlatformsApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->listPlatformsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\PlatformInfo[]**](../Model/PlatformInfo.md)

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
oauthAuthorizeApi($o_auth_authorize_request): \OpenAPI\Client\Model\OAuthAuthorizeResponse
```

OAuth: initiate authorization flow

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$o_auth_authorize_request = new \OpenAPI\Client\Model\OAuthAuthorizeRequest(); // \OpenAPI\Client\Model\OAuthAuthorizeRequest

try {
    $result = $apiInstance->oauthAuthorizeApi($o_auth_authorize_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->oauthAuthorizeApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **o_auth_authorize_request** | [**\OpenAPI\Client\Model\OAuthAuthorizeRequest**](../Model/OAuthAuthorizeRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\OAuthAuthorizeResponse**](../Model/OAuthAuthorizeResponse.md)

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
oauthCallbackApi($o_auth_callback_request): \OpenAPI\Client\Model\MarketplaceConnection
```

OAuth: handle callback after authorization

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$o_auth_callback_request = new \OpenAPI\Client\Model\OAuthCallbackRequest(); // \OpenAPI\Client\Model\OAuthCallbackRequest

try {
    $result = $apiInstance->oauthCallbackApi($o_auth_callback_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->oauthCallbackApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **o_auth_callback_request** | [**\OpenAPI\Client\Model\OAuthCallbackRequest**](../Model/OAuthCallbackRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\MarketplaceConnection**](../Model/MarketplaceConnection.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `triggerSyncApi()`

```php
triggerSyncApi($connection_id, $sync_type, $direction): \OpenAPI\Client\Model\SyncSummary
```

Trigger sync for a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_id = 'connection_id_example'; // string
$sync_type = 'sync_type_example'; // string
$direction = 'direction_example'; // string

try {
    $result = $apiInstance->triggerSyncApi($connection_id, $sync_type, $direction);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->triggerSyncApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_id** | **string**|  | |
| **sync_type** | **string**|  | [optional] |
| **direction** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SyncSummary**](../Model/SyncSummary.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateConnectionApi()`

```php
updateConnectionApi($connection_id, $update_connection_request): \OpenAPI\Client\Model\MarketplaceConnection
```

Update a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_id = 'connection_id_example'; // string
$update_connection_request = new \OpenAPI\Client\Model\UpdateConnectionRequest(); // \OpenAPI\Client\Model\UpdateConnectionRequest

try {
    $result = $apiInstance->updateConnectionApi($connection_id, $update_connection_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->updateConnectionApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_id** | **string**|  | |
| **update_connection_request** | [**\OpenAPI\Client\Model\UpdateConnectionRequest**](../Model/UpdateConnectionRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\MarketplaceConnection**](../Model/MarketplaceConnection.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateSyncDirectionApi()`

```php
updateSyncDirectionApi($connection_id, $update_sync_direction_request)
```

Update per-entity sync direction configuration for a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_id = 'connection_id_example'; // string
$update_sync_direction_request = new \OpenAPI\Client\Model\UpdateSyncDirectionRequest(); // \OpenAPI\Client\Model\UpdateSyncDirectionRequest

try {
    $apiInstance->updateSyncDirectionApi($connection_id, $update_sync_direction_request);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->updateSyncDirectionApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_id** | **string**|  | |
| **update_sync_direction_request** | [**\OpenAPI\Client\Model\UpdateSyncDirectionRequest**](../Model/UpdateSyncDirectionRequest.md)|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `webhookReceiverApi()`

```php
webhookReceiverApi($platform, $connection_id)
```

Webhook receiver

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\MarketplaceApiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$platform = 'platform_example'; // string
$connection_id = 'connection_id_example'; // string

try {
    $apiInstance->webhookReceiverApi($platform, $connection_id);
} catch (Exception $e) {
    echo 'Exception when calling MarketplaceApiApi->webhookReceiverApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **platform** | **string**|  | |
| **connection_id** | **string**|  | |

### Return type

void (empty response body)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
