# OpenAPI\Client\AttachmentVersionApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createAttachmentVersion()**](AttachmentVersionApi.md#createAttachmentVersion) | **POST** /api/v1/attachments/{attachment_id}/versions |  |
| [**listAttachmentVersions()**](AttachmentVersionApi.md#listAttachmentVersions) | **GET** /api/v1/attachments/{attachment_id}/versions |  |
| [**restoreAttachmentVersion()**](AttachmentVersionApi.md#restoreAttachmentVersion) | **POST** /api/v1/attachments/{attachment_id}/versions/{version_id}/restore |  |


## `createAttachmentVersion()`

```php
createAttachmentVersion($attachment_id, $new_version_request): \OpenAPI\Client\Model\AttachmentVersion
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AttachmentVersionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$attachment_id = 'attachment_id_example'; // string
$new_version_request = new \OpenAPI\Client\Model\NewVersionRequest(); // \OpenAPI\Client\Model\NewVersionRequest

try {
    $result = $apiInstance->createAttachmentVersion($attachment_id, $new_version_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AttachmentVersionApi->createAttachmentVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attachment_id** | **string**|  | |
| **new_version_request** | [**\OpenAPI\Client\Model\NewVersionRequest**](../Model/NewVersionRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AttachmentVersion**](../Model/AttachmentVersion.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listAttachmentVersions()`

```php
listAttachmentVersions($attachment_id): \OpenAPI\Client\Model\AttachmentVersion[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AttachmentVersionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$attachment_id = 'attachment_id_example'; // string

try {
    $result = $apiInstance->listAttachmentVersions($attachment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AttachmentVersionApi->listAttachmentVersions: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attachment_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\AttachmentVersion[]**](../Model/AttachmentVersion.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `restoreAttachmentVersion()`

```php
restoreAttachmentVersion($attachment_id, $version_id): \OpenAPI\Client\Model\Attachment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AttachmentVersionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$attachment_id = 'attachment_id_example'; // string
$version_id = 'version_id_example'; // string

try {
    $result = $apiInstance->restoreAttachmentVersion($attachment_id, $version_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AttachmentVersionApi->restoreAttachmentVersion: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **attachment_id** | **string**|  | |
| **version_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Attachment**](../Model/Attachment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
