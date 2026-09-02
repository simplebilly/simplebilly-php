# OpenAPI\Client\SupportChannelApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createChannelApi()**](SupportChannelApi.md#createChannelApi) | **POST** /api/v1/support/channels |  |
| [**deleteChannelApi()**](SupportChannelApi.md#deleteChannelApi) | **DELETE** /api/v1/support/channels/{channel_id} |  |
| [**listChannelsApi()**](SupportChannelApi.md#listChannelsApi) | **GET** /api/v1/support/channels |  |
| [**updateChannelApi()**](SupportChannelApi.md#updateChannelApi) | **PUT** /api/v1/support/channels/{channel_id} |  |


## `createChannelApi()`

```php
createChannelApi($create_channel_dto): \OpenAPI\Client\Model\SupportChannel
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_channel_dto = new \OpenAPI\Client\Model\CreateChannelDto(); // \OpenAPI\Client\Model\CreateChannelDto

try {
    $result = $apiInstance->createChannelApi($create_channel_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupportChannelApi->createChannelApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_channel_dto** | [**\OpenAPI\Client\Model\CreateChannelDto**](../Model/CreateChannelDto.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SupportChannel**](../Model/SupportChannel.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteChannelApi()`

```php
deleteChannelApi($channel_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string

try {
    $apiInstance->deleteChannelApi($channel_id);
} catch (Exception $e) {
    echo 'Exception when calling SupportChannelApi->deleteChannelApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |

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

## `listChannelsApi()`

```php
listChannelsApi(): \OpenAPI\Client\Model\SupportChannel[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listChannelsApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupportChannelApi->listChannelsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\SupportChannel[]**](../Model/SupportChannel.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateChannelApi()`

```php
updateChannelApi($channel_id, $update_channel_dto): \OpenAPI\Client\Model\SupportChannel
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$channel_id = 'channel_id_example'; // string
$update_channel_dto = new \OpenAPI\Client\Model\UpdateChannelDto(); // \OpenAPI\Client\Model\UpdateChannelDto

try {
    $result = $apiInstance->updateChannelApi($channel_id, $update_channel_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupportChannelApi->updateChannelApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **channel_id** | **string**|  | |
| **update_channel_dto** | [**\OpenAPI\Client\Model\UpdateChannelDto**](../Model/UpdateChannelDto.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SupportChannel**](../Model/SupportChannel.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
