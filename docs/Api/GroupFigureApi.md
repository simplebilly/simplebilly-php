# OpenAPI\Client\GroupFigureApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createGroupFigure()**](GroupFigureApi.md#createGroupFigure) | **POST** /api/v1/group-figures |  |
| [**deleteGroupFigure()**](GroupFigureApi.md#deleteGroupFigure) | **DELETE** /api/v1/group-figures/{year} |  |
| [**getGroupFigure()**](GroupFigureApi.md#getGroupFigure) | **GET** /api/v1/group-figures/{year} |  |
| [**getGroupFigures()**](GroupFigureApi.md#getGroupFigures) | **GET** /api/v1/group-figures/ |  |
| [**updateGroupFigure()**](GroupFigureApi.md#updateGroupFigure) | **PUT** /api/v1/group-figures/{year} |  |


## `createGroupFigure()`

```php
createGroupFigure($group_figure_create): \OpenAPI\Client\Model\GroupFigure
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GroupFigureApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group_figure_create = new \OpenAPI\Client\Model\GroupFigureCreate(); // \OpenAPI\Client\Model\GroupFigureCreate

try {
    $result = $apiInstance->createGroupFigure($group_figure_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupFigureApi->createGroupFigure: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_figure_create** | [**\OpenAPI\Client\Model\GroupFigureCreate**](../Model/GroupFigureCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\GroupFigure**](../Model/GroupFigure.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteGroupFigure()`

```php
deleteGroupFigure($year)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GroupFigureApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int

try {
    $apiInstance->deleteGroupFigure($year);
} catch (Exception $e) {
    echo 'Exception when calling GroupFigureApi->deleteGroupFigure: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |

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

## `getGroupFigure()`

```php
getGroupFigure($year): \OpenAPI\Client\Model\GroupFigure
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GroupFigureApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int

try {
    $result = $apiInstance->getGroupFigure($year);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupFigureApi->getGroupFigure: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |

### Return type

[**\OpenAPI\Client\Model\GroupFigure**](../Model/GroupFigure.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGroupFigures()`

```php
getGroupFigures($page, $page_size, $search, $include_deleted): \OpenAPI\Client\Model\GroupFigure[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GroupFigureApi(
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
    $result = $apiInstance->getGroupFigures($page, $page_size, $search, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupFigureApi->getGroupFigures: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\GroupFigure[]**](../Model/GroupFigure.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateGroupFigure()`

```php
updateGroupFigure($year, $group_figure_update): \OpenAPI\Client\Model\GroupFigure
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GroupFigureApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$group_figure_update = new \OpenAPI\Client\Model\GroupFigureUpdate(); // \OpenAPI\Client\Model\GroupFigureUpdate

try {
    $result = $apiInstance->updateGroupFigure($year, $group_figure_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupFigureApi->updateGroupFigure: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |
| **group_figure_update** | [**\OpenAPI\Client\Model\GroupFigureUpdate**](../Model/GroupFigureUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\GroupFigure**](../Model/GroupFigure.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
