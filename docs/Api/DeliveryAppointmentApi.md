# OpenAPI\Client\DeliveryAppointmentApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createDeliveryAppointment()**](DeliveryAppointmentApi.md#createDeliveryAppointment) | **POST** /api/v1/delivery-appointments |  |
| [**deleteDeliveryAppointment()**](DeliveryAppointmentApi.md#deleteDeliveryAppointment) | **DELETE** /api/v1/delivery-appointments/{appointment_id} |  |
| [**getDeliveryAppointment()**](DeliveryAppointmentApi.md#getDeliveryAppointment) | **GET** /api/v1/delivery-appointments/{appointment_id} |  |
| [**getPublicDeliveryAppointmentStatus()**](DeliveryAppointmentApi.md#getPublicDeliveryAppointmentStatus) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match. |
| [**listDeliveryAppointments()**](DeliveryAppointmentApi.md#listDeliveryAppointments) | **GET** /api/v1/delivery-appointments |  |
| [**requestPublicDeliveryAppointment()**](DeliveryAppointmentApi.md#requestPublicDeliveryAppointment) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request. |
| [**updateDeliveryAppointment()**](DeliveryAppointmentApi.md#updateDeliveryAppointment) | **PUT** /api/v1/delivery-appointments/{appointment_id} |  |
| [**updateDeliveryAppointmentStatus()**](DeliveryAppointmentApi.md#updateDeliveryAppointmentStatus) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status |  |


## `createDeliveryAppointment()`

```php
createDeliveryAppointment($delivery_appointment_create): \OpenAPI\Client\Model\DeliveryAppointment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryAppointmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$delivery_appointment_create = new \OpenAPI\Client\Model\DeliveryAppointmentCreate(); // \OpenAPI\Client\Model\DeliveryAppointmentCreate

try {
    $result = $apiInstance->createDeliveryAppointment($delivery_appointment_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryAppointmentApi->createDeliveryAppointment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **delivery_appointment_create** | [**\OpenAPI\Client\Model\DeliveryAppointmentCreate**](../Model/DeliveryAppointmentCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryAppointment**](../Model/DeliveryAppointment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteDeliveryAppointment()`

```php
deleteDeliveryAppointment($appointment_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryAppointmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$appointment_id = 'appointment_id_example'; // string

try {
    $apiInstance->deleteDeliveryAppointment($appointment_id);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryAppointmentApi->deleteDeliveryAppointment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **appointment_id** | **string**|  | |

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

## `getDeliveryAppointment()`

```php
getDeliveryAppointment($appointment_id): \OpenAPI\Client\Model\DeliveryAppointment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryAppointmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$appointment_id = 'appointment_id_example'; // string

try {
    $result = $apiInstance->getDeliveryAppointment($appointment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryAppointmentApi->getDeliveryAppointment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **appointment_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryAppointment**](../Model/DeliveryAppointment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getPublicDeliveryAppointmentStatus()`

```php
getPublicDeliveryAppointmentStatus($appointment_id, $email, $token): \OpenAPI\Client\Model\PublicDeliveryAppointmentStatusResponse
```

Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryAppointmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$appointment_id = 'appointment_id_example'; // string
$email = 'email_example'; // string
$token = 'token_example'; // string

try {
    $result = $apiInstance->getPublicDeliveryAppointmentStatus($appointment_id, $email, $token);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryAppointmentApi->getPublicDeliveryAppointmentStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **appointment_id** | **string**|  | |
| **email** | **string**|  | |
| **token** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\PublicDeliveryAppointmentStatusResponse**](../Model/PublicDeliveryAppointmentStatusResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDeliveryAppointments()`

```php
listDeliveryAppointments($page, $page_size, $status, $warehouse_id, $from, $to): \OpenAPI\Client\Model\DeliveryAppointment[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryAppointmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$status = 'status_example'; // string
$warehouse_id = 'warehouse_id_example'; // string
$from = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime
$to = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime

try {
    $result = $apiInstance->listDeliveryAppointments($page, $page_size, $status, $warehouse_id, $from, $to);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryAppointmentApi->listDeliveryAppointments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **status** | **string**|  | [optional] |
| **warehouse_id** | **string**|  | [optional] |
| **from** | **\DateTime**|  | [optional] |
| **to** | **\DateTime**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\DeliveryAppointment[]**](../Model/DeliveryAppointment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `requestPublicDeliveryAppointment()`

```php
requestPublicDeliveryAppointment($public_delivery_appointment_request): \OpenAPI\Client\Model\PublicDeliveryAppointmentResponse
```

Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryAppointmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$public_delivery_appointment_request = new \OpenAPI\Client\Model\PublicDeliveryAppointmentRequest(); // \OpenAPI\Client\Model\PublicDeliveryAppointmentRequest

try {
    $result = $apiInstance->requestPublicDeliveryAppointment($public_delivery_appointment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryAppointmentApi->requestPublicDeliveryAppointment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **public_delivery_appointment_request** | [**\OpenAPI\Client\Model\PublicDeliveryAppointmentRequest**](../Model/PublicDeliveryAppointmentRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\PublicDeliveryAppointmentResponse**](../Model/PublicDeliveryAppointmentResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDeliveryAppointment()`

```php
updateDeliveryAppointment($appointment_id, $body): \OpenAPI\Client\Model\DeliveryAppointment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryAppointmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$appointment_id = 'appointment_id_example'; // string
$body = NULL; // mixed

try {
    $result = $apiInstance->updateDeliveryAppointment($appointment_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryAppointmentApi->updateDeliveryAppointment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **appointment_id** | **string**|  | |
| **body** | **mixed**|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryAppointment**](../Model/DeliveryAppointment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateDeliveryAppointmentStatus()`

```php
updateDeliveryAppointmentStatus($appointment_id, $appointment_status_update): \OpenAPI\Client\Model\DeliveryAppointment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\DeliveryAppointmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$appointment_id = 'appointment_id_example'; // string
$appointment_status_update = new \OpenAPI\Client\Model\AppointmentStatusUpdate(); // \OpenAPI\Client\Model\AppointmentStatusUpdate

try {
    $result = $apiInstance->updateDeliveryAppointmentStatus($appointment_id, $appointment_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeliveryAppointmentApi->updateDeliveryAppointmentStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **appointment_id** | **string**|  | |
| **appointment_status_update** | [**\OpenAPI\Client\Model\AppointmentStatusUpdate**](../Model/AppointmentStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\DeliveryAppointment**](../Model/DeliveryAppointment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
