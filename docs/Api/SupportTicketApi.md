# OpenAPI\Client\SupportTicketApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createTicketApi()**](SupportTicketApi.md#createTicketApi) | **POST** /api/v1/support/tickets |  |
| [**deleteTicketApi()**](SupportTicketApi.md#deleteTicketApi) | **DELETE** /api/v1/support/tickets/{ticket_id} |  |
| [**getTicketApi()**](SupportTicketApi.md#getTicketApi) | **GET** /api/v1/support/tickets/{ticket_id} |  |
| [**listTicketsApi()**](SupportTicketApi.md#listTicketsApi) | **GET** /api/v1/support/tickets |  |
| [**updateTicketApi()**](SupportTicketApi.md#updateTicketApi) | **PUT** /api/v1/support/tickets/{ticket_id} |  |


## `createTicketApi()`

```php
createTicketApi($create_ticket_request): \OpenAPI\Client\Model\SupportTicket
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportTicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_ticket_request = new \OpenAPI\Client\Model\CreateTicketRequest(); // \OpenAPI\Client\Model\CreateTicketRequest

try {
    $result = $apiInstance->createTicketApi($create_ticket_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupportTicketApi->createTicketApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_ticket_request** | [**\OpenAPI\Client\Model\CreateTicketRequest**](../Model/CreateTicketRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SupportTicket**](../Model/SupportTicket.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteTicketApi()`

```php
deleteTicketApi($ticket_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportTicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ticket_id = 'ticket_id_example'; // string

try {
    $apiInstance->deleteTicketApi($ticket_id);
} catch (Exception $e) {
    echo 'Exception when calling SupportTicketApi->deleteTicketApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ticket_id** | **string**|  | |

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

## `getTicketApi()`

```php
getTicketApi($ticket_id): \OpenAPI\Client\Model\SupportTicket
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportTicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ticket_id = 'ticket_id_example'; // string

try {
    $result = $apiInstance->getTicketApi($ticket_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupportTicketApi->getTicketApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ticket_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\SupportTicket**](../Model/SupportTicket.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listTicketsApi()`

```php
listTicketsApi($status, $priority, $assigned_to, $channel_type, $customer_id, $search, $page, $page_size): \OpenAPI\Client\Model\SupportTicket[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportTicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$status = 'status_example'; // string
$priority = 'priority_example'; // string
$assigned_to = 'assigned_to_example'; // string
$channel_type = 'channel_type_example'; // string
$customer_id = 'customer_id_example'; // string
$search = 'search_example'; // string
$page = 56; // int
$page_size = 56; // int

try {
    $result = $apiInstance->listTicketsApi($status, $priority, $assigned_to, $channel_type, $customer_id, $search, $page, $page_size);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupportTicketApi->listTicketsApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **status** | **string**|  | [optional] |
| **priority** | **string**|  | [optional] |
| **assigned_to** | **string**|  | [optional] |
| **channel_type** | **string**|  | [optional] |
| **customer_id** | **string**|  | [optional] |
| **search** | **string**|  | [optional] |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SupportTicket[]**](../Model/SupportTicket.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateTicketApi()`

```php
updateTicketApi($ticket_id, $support_ticket_update): \OpenAPI\Client\Model\SupportTicket
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\SupportTicketApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ticket_id = 'ticket_id_example'; // string
$support_ticket_update = new \OpenAPI\Client\Model\SupportTicketUpdate(); // \OpenAPI\Client\Model\SupportTicketUpdate

try {
    $result = $apiInstance->updateTicketApi($ticket_id, $support_ticket_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SupportTicketApi->updateTicketApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ticket_id** | **string**|  | |
| **support_ticket_update** | [**\OpenAPI\Client\Model\SupportTicketUpdate**](../Model/SupportTicketUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\SupportTicket**](../Model/SupportTicket.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
