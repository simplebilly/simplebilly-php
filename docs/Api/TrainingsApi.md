# OpenAPI\Client\TrainingsApi

Compliance Schulungen (required trainings). Permissions: training:read, training:write, training:complete

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getMyTrainings()**](TrainingsApi.md#getMyTrainings) | **GET** /api/v1/trainings/me |  |
| [**getTrainingContent()**](TrainingsApi.md#getTrainingContent) | **GET** /api/v1/trainings/content/{code} |  |
| [**getTrainingOverview()**](TrainingsApi.md#getTrainingOverview) | **GET** /api/v1/trainings/overview |  |
| [**submitTrainingResult()**](TrainingsApi.md#submitTrainingResult) | **POST** /api/v1/trainings/submit-result |  |


## `getMyTrainings()`

```php
getMyTrainings(): \OpenAPI\Client\Model\MyTrainingItem[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TrainingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getMyTrainings();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TrainingsApi->getMyTrainings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\MyTrainingItem[]**](../Model/MyTrainingItem.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTrainingContent()`

```php
getTrainingContent($code): \OpenAPI\Client\Model\TrainingContent
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TrainingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$code = 'code_example'; // string | Training code, e.g. data_privacy

try {
    $result = $apiInstance->getTrainingContent($code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TrainingsApi->getTrainingContent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **code** | **string**| Training code, e.g. data_privacy | |

### Return type

[**\OpenAPI\Client\Model\TrainingContent**](../Model/TrainingContent.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTrainingOverview()`

```php
getTrainingOverview(): \OpenAPI\Client\Model\HrTrainingOverview[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TrainingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getTrainingOverview();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TrainingsApi->getTrainingOverview: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\HrTrainingOverview[]**](../Model/HrTrainingOverview.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `submitTrainingResult()`

```php
submitTrainingResult($submit_result_dto): \OpenAPI\Client\Model\SubmitResultResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TrainingsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$submit_result_dto = new \OpenAPI\Client\Model\SubmitResultDto(); // \OpenAPI\Client\Model\SubmitResultDto

try {
    $result = $apiInstance->submitTrainingResult($submit_result_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TrainingsApi->submitTrainingResult: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **submit_result_dto** | [**\OpenAPI\Client\Model\SubmitResultDto**](../Model/SubmitResultDto.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SubmitResultResponse**](../Model/SubmitResultResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
