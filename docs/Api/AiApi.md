# OpenAPI\Client\AiApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**aiSuggestApi()**](AiApi.md#aiSuggestApi) | **POST** /api/v1/support/ai/suggest |  |
| [**createWorkerApi()**](AiApi.md#createWorkerApi) | **POST** /api/v1/support/ai/workers |  |
| [**listWorkersApi()**](AiApi.md#listWorkersApi) | **GET** /api/v1/support/ai/workers |  |
| [**runWorkerApi()**](AiApi.md#runWorkerApi) | **POST** /api/v1/support/ai/workers/{worker_id}/run |  |


## `aiSuggestApi()`

```php
aiSuggestApi($ai_suggestion_request): \OpenAPI\Client\Model\AiSuggestion
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ai_suggestion_request = new \OpenAPI\Client\Model\AiSuggestionRequest(); // \OpenAPI\Client\Model\AiSuggestionRequest

try {
    $result = $apiInstance->aiSuggestApi($ai_suggestion_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AiApi->aiSuggestApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ai_suggestion_request** | [**\OpenAPI\Client\Model\AiSuggestionRequest**](../Model/AiSuggestionRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AiSuggestion**](../Model/AiSuggestion.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createWorkerApi()`

```php
createWorkerApi($ai_config_dto): \OpenAPI\Client\Model\AiWorkerConfig
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ai_config_dto = new \OpenAPI\Client\Model\AiConfigDto(); // \OpenAPI\Client\Model\AiConfigDto

try {
    $result = $apiInstance->createWorkerApi($ai_config_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AiApi->createWorkerApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ai_config_dto** | [**\OpenAPI\Client\Model\AiConfigDto**](../Model/AiConfigDto.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AiWorkerConfig**](../Model/AiWorkerConfig.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listWorkersApi()`

```php
listWorkersApi(): \OpenAPI\Client\Model\AiWorkerConfig[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listWorkersApi();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AiApi->listWorkersApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\AiWorkerConfig[]**](../Model/AiWorkerConfig.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `runWorkerApi()`

```php
runWorkerApi($worker_id, $ai_suggestion_request): \OpenAPI\Client\Model\AiSuggestion
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\AiApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$worker_id = 'worker_id_example'; // string
$ai_suggestion_request = new \OpenAPI\Client\Model\AiSuggestionRequest(); // \OpenAPI\Client\Model\AiSuggestionRequest

try {
    $result = $apiInstance->runWorkerApi($worker_id, $ai_suggestion_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AiApi->runWorkerApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **worker_id** | **string**|  | |
| **ai_suggestion_request** | [**\OpenAPI\Client\Model\AiSuggestionRequest**](../Model/AiSuggestionRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\AiSuggestion**](../Model/AiSuggestion.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
