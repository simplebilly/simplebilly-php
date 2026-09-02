# OpenAPI\Client\CouponApi

Coupon management. Required permissions: coupons:read, coupons:write, coupons:delete.

All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**couponRestore()**](CouponApi.md#couponRestore) | **POST** /api/v1/coupons/{coupon_id}/restore |  |
| [**createCoupon()**](CouponApi.md#createCoupon) | **POST** /api/v1/coupons |  |
| [**deleteCoupon()**](CouponApi.md#deleteCoupon) | **DELETE** /api/v1/coupons/{coupon_id} |  |
| [**getCoupon()**](CouponApi.md#getCoupon) | **GET** /api/v1/coupons/{coupon_id} |  |
| [**listCoupons()**](CouponApi.md#listCoupons) | **GET** /api/v1/coupons/ |  |
| [**updateCoupon()**](CouponApi.md#updateCoupon) | **PUT** /api/v1/coupons/{coupon_id} |  |


## `couponRestore()`

```php
couponRestore($coupon_id): \OpenAPI\Client\Model\Coupon
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CouponApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$coupon_id = 'coupon_id_example'; // string

try {
    $result = $apiInstance->couponRestore($coupon_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponApi->couponRestore: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **coupon_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Coupon**](../Model/Coupon.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createCoupon()`

```php
createCoupon($coupon_create): \OpenAPI\Client\Model\Coupon
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CouponApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$coupon_create = new \OpenAPI\Client\Model\CouponCreate(); // \OpenAPI\Client\Model\CouponCreate

try {
    $result = $apiInstance->createCoupon($coupon_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponApi->createCoupon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **coupon_create** | [**\OpenAPI\Client\Model\CouponCreate**](../Model/CouponCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Coupon**](../Model/Coupon.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteCoupon()`

```php
deleteCoupon($coupon_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CouponApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$coupon_id = 'coupon_id_example'; // string

try {
    $apiInstance->deleteCoupon($coupon_id);
} catch (Exception $e) {
    echo 'Exception when calling CouponApi->deleteCoupon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **coupon_id** | **string**|  | |

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

## `getCoupon()`

```php
getCoupon($coupon_id): \OpenAPI\Client\Model\Coupon
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CouponApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$coupon_id = 'coupon_id_example'; // string

try {
    $result = $apiInstance->getCoupon($coupon_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponApi->getCoupon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **coupon_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\Coupon**](../Model/Coupon.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCoupons()`

```php
listCoupons($page, $page_size, $is_active, $code, $discount_type): \OpenAPI\Client\Model\Coupon[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CouponApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$is_active = True; // bool
$code = 'code_example'; // string
$discount_type = 'discount_type_example'; // string

try {
    $result = $apiInstance->listCoupons($page, $page_size, $is_active, $code, $discount_type);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponApi->listCoupons: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **is_active** | **bool**|  | [optional] |
| **code** | **string**|  | [optional] |
| **discount_type** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\Coupon[]**](../Model/Coupon.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCoupon()`

```php
updateCoupon($coupon_id, $coupon_update): \OpenAPI\Client\Model\Coupon
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CouponApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$coupon_id = 'coupon_id_example'; // string
$coupon_update = new \OpenAPI\Client\Model\CouponUpdate(); // \OpenAPI\Client\Model\CouponUpdate

try {
    $result = $apiInstance->updateCoupon($coupon_id, $coupon_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CouponApi->updateCoupon: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **coupon_id** | **string**|  | |
| **coupon_update** | [**\OpenAPI\Client\Model\CouponUpdate**](../Model/CouponUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\Coupon**](../Model/Coupon.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
