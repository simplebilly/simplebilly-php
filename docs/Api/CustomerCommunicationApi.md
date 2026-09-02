# OpenAPI\Client\CustomerCommunicationApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createCommunication()**](CustomerCommunicationApi.md#createCommunication) | **POST** /api/v1/communications |  |
| [**customercommunicationRestore()**](CustomerCommunicationApi.md#customercommunicationRestore) | **POST** /api/v1/communications/{communication_id}/restore |  |
| [**deleteCommunication()**](CustomerCommunicationApi.md#deleteCommunication) | **DELETE** /api/v1/communications/{communication_id} |  |
| [**getCommunication()**](CustomerCommunicationApi.md#getCommunication) | **GET** /api/v1/communications/{communication_id} |  |
| [**getContactHistory()**](CustomerCommunicationApi.md#getContactHistory) | **GET** /api/v1/contacts/{contact_id}/communications |  |
| [**listCommunications()**](CustomerCommunicationApi.md#listCommunications) | **GET** /api/v1/communications/ |  |
| [**updateCommunication()**](CustomerCommunicationApi.md#updateCommunication) | **PUT** /api/v1/communications/{communication_id} |  |


## `createCommunication()`

```php
createCommunication($customer_communication_create): \OpenAPI\Client\Model\CustomerCommunication
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerCommunicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$customer_communication_create = new \OpenAPI\Client\Model\CustomerCommunicationCreate(); // \OpenAPI\Client\Model\CustomerCommunicationCreate

try {
    $result = $apiInstance->createCommunication($customer_communication_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerCommunicationApi->createCommunication: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **customer_communication_create** | [**\OpenAPI\Client\Model\CustomerCommunicationCreate**](../Model/CustomerCommunicationCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CustomerCommunication**](../Model/CustomerCommunication.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `customercommunicationRestore()`

```php
customercommunicationRestore($communication_id): \OpenAPI\Client\Model\CustomerCommunication
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerCommunicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$communication_id = 'communication_id_example'; // string

try {
    $result = $apiInstance->customercommunicationRestore($communication_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerCommunicationApi->customercommunicationRestore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **communication_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\CustomerCommunication**](../Model/CustomerCommunication.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCommunication()`

```php
deleteCommunication($communication_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerCommunicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$communication_id = 'communication_id_example'; // string

try {
    $apiInstance->deleteCommunication($communication_id);
} catch (Exception $e) {
    echo 'Exception when calling CustomerCommunicationApi->deleteCommunication: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **communication_id** | **string**|  | |

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

## `getCommunication()`

```php
getCommunication($communication_id): \OpenAPI\Client\Model\CustomerCommunication
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerCommunicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$communication_id = 'communication_id_example'; // string

try {
    $result = $apiInstance->getCommunication($communication_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerCommunicationApi->getCommunication: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **communication_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\CustomerCommunication**](../Model/CustomerCommunication.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getContactHistory()`

```php
getContactHistory($contact_id): \OpenAPI\Client\Model\ContactHistoryResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerCommunicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$contact_id = 'contact_id_example'; // string

try {
    $result = $apiInstance->getContactHistory($contact_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerCommunicationApi->getContactHistory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **contact_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ContactHistoryResponse**](../Model/ContactHistoryResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCommunications()`

```php
listCommunications($page, $page_size, $contact_id, $channel, $direction, $from, $to): \OpenAPI\Client\Model\CustomerCommunication[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerCommunicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$contact_id = 'contact_id_example'; // string | Filter history to a single contact.
$channel = new \OpenAPI\Client\Model\\OpenAPIClientModelCommunicationChannel(); // \OpenAPIClientModelCommunicationChannel
$direction = new \OpenAPI\Client\Model\\OpenAPIClientModelCommunicationDirection(); // \OpenAPIClientModelCommunicationDirection
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Only include communications after this ISO date (inclusive).
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Only include communications before this ISO date (inclusive).

try {
    $result = $apiInstance->listCommunications($page, $page_size, $contact_id, $channel, $direction, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerCommunicationApi->listCommunications: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **contact_id** | **string**| Filter history to a single contact. | [optional] |
| **channel** | [**\OpenAPIClientModelCommunicationChannel**](../Model/.md)|  | [optional] |
| **direction** | [**\OpenAPIClientModelCommunicationDirection**](../Model/.md)|  | [optional] |
| **from** | **\DateTime**| Only include communications after this ISO date (inclusive). | [optional] |
| **to** | **\DateTime**| Only include communications before this ISO date (inclusive). | [optional] |

### Return type

[**\OpenAPI\Client\Model\CustomerCommunication[]**](../Model/CustomerCommunication.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCommunication()`

```php
updateCommunication($communication_id, $customer_communication_update): \OpenAPI\Client\Model\CustomerCommunication
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CustomerCommunicationApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$communication_id = 'communication_id_example'; // string
$customer_communication_update = new \OpenAPI\Client\Model\CustomerCommunicationUpdate(); // \OpenAPI\Client\Model\CustomerCommunicationUpdate

try {
    $result = $apiInstance->updateCommunication($communication_id, $customer_communication_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CustomerCommunicationApi->updateCommunication: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **communication_id** | **string**|  | |
| **customer_communication_update** | [**\OpenAPI\Client\Model\CustomerCommunicationUpdate**](../Model/CustomerCommunicationUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\CustomerCommunication**](../Model/CustomerCommunication.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
