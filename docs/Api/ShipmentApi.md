# OpenAPI\Client\ShipmentApi

Shipment management. Required permissions: shipment:read, shipment:write, shipment:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createShipment()**](ShipmentApi.md#createShipment) | **POST** /api/v1/shipments |  |
| [**createShipmentFromOrder()**](ShipmentApi.md#createShipmentFromOrder) | **POST** /api/v1/orders/{order_number}/shipments | Create a real shipment for an order: calls the configured carrier&#39;s label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped. |
| [**deleteShipment()**](ShipmentApi.md#deleteShipment) | **DELETE** /api/v1/shipments/{shipment_id} |  |
| [**getShipment()**](ShipmentApi.md#getShipment) | **GET** /api/v1/shipments/{shipment_id} |  |
| [**listShipments()**](ShipmentApi.md#listShipments) | **GET** /api/v1/shipments |  |
| [**trackOrderPublic()**](ShipmentApi.md#trackOrderPublic) | **POST** /api/v1/public/track | Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API). |
| [**trackShipmentApi()**](ShipmentApi.md#trackShipmentApi) | **GET** /api/v1/shipments/{shipment_id}/tracking |  |
| [**updateShipmentStatus()**](ShipmentApi.md#updateShipmentStatus) | **PUT** /api/v1/shipments/{shipment_id}/status |  |


## `createShipment()`

```php
createShipment($shipment): \OpenAPI\Client\Model\Shipment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShipmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipment = new \OpenAPI\Client\Model\Shipment(); // \OpenAPI\Client\Model\Shipment

try {
    $result = $apiInstance->createShipment($shipment);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentApi->createShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipment** | [**\OpenAPI\Client\Model\Shipment**](../Model/Shipment.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Shipment**](../Model/Shipment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createShipmentFromOrder()`

```php
createShipmentFromOrder($order_number, $create_shipment_request): \OpenAPI\Client\Model\Shipment
```

Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShipmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$order_number = 'order_number_example'; // string
$create_shipment_request = new \OpenAPI\Client\Model\CreateShipmentRequest(); // \OpenAPI\Client\Model\CreateShipmentRequest

try {
    $result = $apiInstance->createShipmentFromOrder($order_number, $create_shipment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentApi->createShipmentFromOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **order_number** | **string**|  | |
| **create_shipment_request** | [**\OpenAPI\Client\Model\CreateShipmentRequest**](../Model/CreateShipmentRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Shipment**](../Model/Shipment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteShipment()`

```php
deleteShipment($shipment_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShipmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipment_id = 'shipment_id_example'; // string

try {
    $apiInstance->deleteShipment($shipment_id);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentApi->deleteShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipment_id** | **string**|  | |

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

## `getShipment()`

```php
getShipment($shipment_id): \OpenAPI\Client\Model\Shipment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShipmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipment_id = 'shipment_id_example'; // string

try {
    $result = $apiInstance->getShipment($shipment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentApi->getShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipment_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Shipment**](../Model/Shipment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listShipments()`

```php
listShipments($page, $page_size, $search, $include_deleted): \OpenAPI\Client\Model\Shipment[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShipmentApi(
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
    $result = $apiInstance->listShipments($page, $page_size, $search, $include_deleted);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentApi->listShipments: ', $e->getMessage(), PHP_EOL;
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

[**\OpenAPI\Client\Model\Shipment[]**](../Model/Shipment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `trackOrderPublic()`

```php
trackOrderPublic($track_order_request): \OpenAPI\Client\Model\TrackOrderResponse
```

Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShipmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$track_order_request = new \OpenAPI\Client\Model\TrackOrderRequest(); // \OpenAPI\Client\Model\TrackOrderRequest

try {
    $result = $apiInstance->trackOrderPublic($track_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentApi->trackOrderPublic: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **track_order_request** | [**\OpenAPI\Client\Model\TrackOrderRequest**](../Model/TrackOrderRequest.md)|  | |

### Return type

[**\OpenAPI\Client\Model\TrackOrderResponse**](../Model/TrackOrderResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `trackShipmentApi()`

```php
trackShipmentApi($shipment_id): \OpenAPI\Client\Model\TrackingInfo
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShipmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipment_id = 'shipment_id_example'; // string

try {
    $result = $apiInstance->trackShipmentApi($shipment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentApi->trackShipmentApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipment_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\TrackingInfo**](../Model/TrackingInfo.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateShipmentStatus()`

```php
updateShipmentStatus($shipment_id, $shipment_status_update): \OpenAPI\Client\Model\Shipment
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShipmentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipment_id = 'shipment_id_example'; // string
$shipment_status_update = new \OpenAPI\Client\Model\ShipmentStatusUpdate(); // \OpenAPI\Client\Model\ShipmentStatusUpdate

try {
    $result = $apiInstance->updateShipmentStatus($shipment_id, $shipment_status_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentApi->updateShipmentStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipment_id** | **string**|  | |
| **shipment_status_update** | [**\OpenAPI\Client\Model\ShipmentStatusUpdate**](../Model/ShipmentStatusUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Shipment**](../Model/Shipment.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
