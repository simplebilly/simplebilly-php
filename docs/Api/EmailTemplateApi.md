# OpenAPI\Client\EmailTemplateApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createEmailTemplate()**](EmailTemplateApi.md#createEmailTemplate) | **POST** /api/v1/email-templates |  |
| [**deleteEmailTemplate()**](EmailTemplateApi.md#deleteEmailTemplate) | **DELETE** /api/v1/email-templates/{email_template_id} |  |
| [**getEmailTemplate()**](EmailTemplateApi.md#getEmailTemplate) | **GET** /api/v1/email-templates/{email_template_id} |  |
| [**listEmailTemplates()**](EmailTemplateApi.md#listEmailTemplates) | **GET** /api/v1/email-templates/ |  |
| [**renderEmailTemplate()**](EmailTemplateApi.md#renderEmailTemplate) | **POST** /api/v1/email-templates/{email_template_id}/render |  |
| [**updateEmailTemplate()**](EmailTemplateApi.md#updateEmailTemplate) | **PUT** /api/v1/email-templates/{email_template_id} |  |


## `createEmailTemplate()`

```php
createEmailTemplate($email_template_create): \OpenAPI\Client\Model\EmailTemplate
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email_template_create = new \OpenAPI\Client\Model\EmailTemplateCreate(); // \OpenAPI\Client\Model\EmailTemplateCreate

try {
    $result = $apiInstance->createEmailTemplate($email_template_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->createEmailTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email_template_create** | [**\OpenAPI\Client\Model\EmailTemplateCreate**](../Model/EmailTemplateCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\EmailTemplate**](../Model/EmailTemplate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteEmailTemplate()`

```php
deleteEmailTemplate($email_template_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email_template_id = 'email_template_id_example'; // string

try {
    $apiInstance->deleteEmailTemplate($email_template_id);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->deleteEmailTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email_template_id** | **string**|  | |

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

## `getEmailTemplate()`

```php
getEmailTemplate($email_template_id): \OpenAPI\Client\Model\EmailTemplate
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email_template_id = 'email_template_id_example'; // string

try {
    $result = $apiInstance->getEmailTemplate($email_template_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->getEmailTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email_template_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\EmailTemplate**](../Model/EmailTemplate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listEmailTemplates()`

```php
listEmailTemplates($page, $page_size, $status, $search): \OpenAPI\Client\Model\EmailTemplate[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$status = 'status_example'; // string
$search = 'search_example'; // string

try {
    $result = $apiInstance->listEmailTemplates($page, $page_size, $status, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->listEmailTemplates: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |
| **search** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\EmailTemplate[]**](../Model/EmailTemplate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `renderEmailTemplate()`

```php
renderEmailTemplate($email_template_id, $body): mixed
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email_template_id = 'email_template_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->renderEmailTemplate($email_template_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->renderEmailTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email_template_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

**mixed**

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateEmailTemplate()`

```php
updateEmailTemplate($email_template_id, $email_template_update): \OpenAPI\Client\Model\EmailTemplate
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\EmailTemplateApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$email_template_id = 'email_template_id_example'; // string
$email_template_update = new \OpenAPI\Client\Model\EmailTemplateUpdate(); // \OpenAPI\Client\Model\EmailTemplateUpdate

try {
    $result = $apiInstance->updateEmailTemplate($email_template_id, $email_template_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EmailTemplateApi->updateEmailTemplate: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **email_template_id** | **string**|  | |
| **email_template_update** | [**\OpenAPI\Client\Model\EmailTemplateUpdate**](../Model/EmailTemplateUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\EmailTemplate**](../Model/EmailTemplate.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
