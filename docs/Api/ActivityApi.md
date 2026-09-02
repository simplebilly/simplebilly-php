# OpenAPI\Client\ActivityApi

Activity management. Required permissions: activity:read, activity:write, activity:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createActivity()**](ActivityApi.md#createActivity) | **POST** /api/v1/activities |  |
| [**deleteActivity()**](ActivityApi.md#deleteActivity) | **DELETE** /api/v1/activities/{activity_id} |  |
| [**getActivity()**](ActivityApi.md#getActivity) | **GET** /api/v1/activities/{activity_id} |  |
| [**listActivities()**](ActivityApi.md#listActivities) | **GET** /api/v1/activities/ |  |
| [**updateActivity()**](ActivityApi.md#updateActivity) | **PUT** /api/v1/activities/{activity_id} |  |
| [**updateActivityStatus()**](ActivityApi.md#updateActivityStatus) | **PUT** /api/v1/activities/{activity_id}/status |  |


## `createActivity()`

```php
createActivity($activity): \OpenAPI\Client\Model\Activity
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$activity = new \OpenAPI\Client\Model\Activity(); // \OpenAPI\Client\Model\Activity

try {
    $result = $apiInstance->createActivity($activity);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->createActivity: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **activity** | [**\OpenAPI\Client\Model\Activity**](../Model/Activity.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Activity**](../Model/Activity.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteActivity()`

```php
deleteActivity($activity_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$activity_id = 'activity_id_example'; // string

try {
    $apiInstance->deleteActivity($activity_id);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->deleteActivity: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **activity_id** | **string**|  | |

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

## `getActivity()`

```php
getActivity($activity_id): \OpenAPI\Client\Model\Activity
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$activity_id = 'activity_id_example'; // string

try {
    $result = $apiInstance->getActivity($activity_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->getActivity: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **activity_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Activity**](../Model/Activity.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listActivities()`

```php
listActivities($page, $page_size, $contact_id, $activity_type, $status, $assigned_to, $overdue_only): \OpenAPI\Client\Model\Activity[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$contact_id = 'contact_id_example'; // string
$activity_type = 'activity_type_example'; // string
$status = 'status_example'; // string
$assigned_to = 'assigned_to_example'; // string
$overdue_only = True; // bool | Only show overdue follow-ups.

try {
    $result = $apiInstance->listActivities($page, $page_size, $contact_id, $activity_type, $status, $assigned_to, $overdue_only);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->listActivities: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **contact_id** | **string**|  | [optional] |
| **activity_type** | **string**|  | [optional] |
| **status** | **string**|  | [optional] |
| **assigned_to** | **string**|  | [optional] |
| **overdue_only** | **bool**| Only show overdue follow-ups. | [optional] |

### Return type

[**\OpenAPI\Client\Model\Activity[]**](../Model/Activity.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateActivity()`

```php
updateActivity($activity_id, $body): \OpenAPI\Client\Model\Activity
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$activity_id = 'activity_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateActivity($activity_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->updateActivity: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **activity_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\Activity**](../Model/Activity.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateActivityStatus()`

```php
updateActivityStatus($activity_id, $activity_status_update): \OpenAPI\Client\Model\Activity
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ActivityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$activity_id = 'activity_id_example'; // string
$activity_status_update = new \OpenAPI\Client\Model\ActivityStatusUpdate(); // \OpenAPI\Client\Model\ActivityStatusUpdate

try {
    $result = $apiInstance->updateActivityStatus($activity_id, $activity_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ActivityApi->updateActivityStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **activity_id** | **string**|  | |
| **activity_status_update** | [**\OpenAPI\Client\Model\ActivityStatusUpdate**](../Model/ActivityStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Activity**](../Model/Activity.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
