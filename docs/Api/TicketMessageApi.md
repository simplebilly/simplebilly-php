# OpenAPI\Client\TicketMessageApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listMessagesApi()**](TicketMessageApi.md#listMessagesApi) | **GET** /api/v1/support/tickets/{ticket_id}/messages |  |
| [**sendMessageApi()**](TicketMessageApi.md#sendMessageApi) | **POST** /api/v1/support/tickets/{ticket_id}/messages |  |


## `listMessagesApi()`

```php
listMessagesApi($ticket_id): \OpenAPI\Client\Model\TicketMessage[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TicketMessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ticket_id = 'ticket_id_example'; // string

try {
    $result = $apiInstance->listMessagesApi($ticket_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketMessageApi->listMessagesApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ticket_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\TicketMessage[]**](../Model/TicketMessage.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendMessageApi()`

```php
sendMessageApi($ticket_id, $send_message_dto): \OpenAPI\Client\Model\TicketMessage
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\TicketMessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$ticket_id = 'ticket_id_example'; // string
$send_message_dto = new \OpenAPI\Client\Model\SendMessageDto(); // \OpenAPI\Client\Model\SendMessageDto

try {
    $result = $apiInstance->sendMessageApi($ticket_id, $send_message_dto);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TicketMessageApi->sendMessageApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **ticket_id** | **string**|  | |
| **send_message_dto** | [**\OpenAPI\Client\Model\SendMessageDto**](../Model/SendMessageDto.md)|  | |

### Return type

[**\OpenAPI\Client\Model\TicketMessage**](../Model/TicketMessage.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
