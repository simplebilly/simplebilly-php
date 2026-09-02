# OpenAPI\Client\JobPostingApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createJobPosting()**](JobPostingApi.md#createJobPosting) | **POST** /api/v1/job-postings |  |
| [**deleteJobPosting()**](JobPostingApi.md#deleteJobPosting) | **DELETE** /api/v1/job-postings/{id} |  |
| [**getJobPosting()**](JobPostingApi.md#getJobPosting) | **GET** /api/v1/job-postings/{id} |  |
| [**listJobPostings()**](JobPostingApi.md#listJobPostings) | **GET** /api/v1/job-postings |  |
| [**updateJobPosting()**](JobPostingApi.md#updateJobPosting) | **PUT** /api/v1/job-postings/{id} |  |


## `createJobPosting()`

```php
createJobPosting($job_posting_create): \OpenAPI\Client\Model\JobPosting
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\JobPostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$job_posting_create = new \OpenAPI\Client\Model\JobPostingCreate(); // \OpenAPI\Client\Model\JobPostingCreate

try {
    $result = $apiInstance->createJobPosting($job_posting_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobPostingApi->createJobPosting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **job_posting_create** | [**\OpenAPI\Client\Model\JobPostingCreate**](../Model/JobPostingCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\JobPosting**](../Model/JobPosting.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteJobPosting()`

```php
deleteJobPosting($id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\JobPostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $apiInstance->deleteJobPosting($id);
} catch (Exception $e) {
    echo 'Exception when calling JobPostingApi->deleteJobPosting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

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

## `getJobPosting()`

```php
getJobPosting($id): \OpenAPI\Client\Model\JobPosting
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\JobPostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string

try {
    $result = $apiInstance->getJobPosting($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobPostingApi->getJobPosting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\JobPosting**](../Model/JobPosting.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listJobPostings()`

```php
listJobPostings($status, $page, $page_size): \OpenAPI\Client\Model\JobPosting[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\JobPostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = 'status_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->listJobPostings($status, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobPostingApi->listJobPostings: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\JobPosting[]**](../Model/JobPosting.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateJobPosting()`

```php
updateJobPosting($id, $job_posting_update): \OpenAPI\Client\Model\JobPosting
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\JobPostingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 'id_example'; // string
$job_posting_update = new \OpenAPI\Client\Model\JobPostingUpdate(); // \OpenAPI\Client\Model\JobPostingUpdate

try {
    $result = $apiInstance->updateJobPosting($id, $job_posting_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling JobPostingApi->updateJobPosting: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**|  | |
| **job_posting_update** | [**\OpenAPI\Client\Model\JobPostingUpdate**](../Model/JobPostingUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\JobPosting**](../Model/JobPosting.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
