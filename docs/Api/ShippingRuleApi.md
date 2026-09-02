# OpenAPI\Client\ShippingRuleApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createShippingRule()**](ShippingRuleApi.md#createShippingRule) | **POST** /api/v1/shipping-rules |  |
| [**deleteShippingRule()**](ShippingRuleApi.md#deleteShippingRule) | **DELETE** /api/v1/shipping-rules/{rule_id} |  |
| [**getShippingRule()**](ShippingRuleApi.md#getShippingRule) | **GET** /api/v1/shipping-rules/{rule_id} |  |
| [**listShippingRules()**](ShippingRuleApi.md#listShippingRules) | **GET** /api/v1/shipping-rules/ |  |
| [**updateShippingRule()**](ShippingRuleApi.md#updateShippingRule) | **PUT** /api/v1/shipping-rules/{rule_id} |  |


## `createShippingRule()`

```php
createShippingRule($shipping_rule_create): \OpenAPI\Client\Model\ShippingRule
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$shipping_rule_create = new \OpenAPI\Client\Model\ShippingRuleCreate(); // \OpenAPI\Client\Model\ShippingRuleCreate

try {
    $result = $apiInstance->createShippingRule($shipping_rule_create);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingRuleApi->createShippingRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **shipping_rule_create** | [**\OpenAPI\Client\Model\ShippingRuleCreate**](../Model/ShippingRuleCreate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ShippingRule**](../Model/ShippingRule.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteShippingRule()`

```php
deleteShippingRule($rule_id)
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string

try {
    $apiInstance->deleteShippingRule($rule_id);
} catch (Exception $e) {
    echo 'Exception when calling ShippingRuleApi->deleteShippingRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**|  | |

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

## `getShippingRule()`

```php
getShippingRule($rule_id): \OpenAPI\Client\Model\ShippingRule
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string

try {
    $result = $apiInstance->getShippingRule($rule_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingRuleApi->getShippingRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**|  | |

### Return type

[**\OpenAPI\Client\Model\ShippingRule**](../Model/ShippingRule.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listShippingRules()`

```php
listShippingRules($page, $page_size, $country): \OpenAPI\Client\Model\ShippingRule[]
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$page = 56; // int
$page_size = 56; // int
$country = 'country_example'; // string

try {
    $result = $apiInstance->listShippingRules($page, $page_size, $country);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingRuleApi->listShippingRules: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **page** | **int**|  | [optional] |
| **page_size** | **int**|  | [optional] |
| **country** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ShippingRule[]**](../Model/ShippingRule.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateShippingRule()`

```php
updateShippingRule($rule_id, $shipping_rule_update): \OpenAPI\Client\Model\ShippingRule
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\ShippingRuleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$rule_id = 'rule_id_example'; // string
$shipping_rule_update = new \OpenAPI\Client\Model\ShippingRuleUpdate(); // \OpenAPI\Client\Model\ShippingRuleUpdate

try {
    $result = $apiInstance->updateShippingRule($rule_id, $shipping_rule_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShippingRuleApi->updateShippingRule: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **rule_id** | **string**|  | |
| **shipping_rule_update** | [**\OpenAPI\Client\Model\ShippingRuleUpdate**](../Model/ShippingRuleUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\ShippingRule**](../Model/ShippingRule.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
