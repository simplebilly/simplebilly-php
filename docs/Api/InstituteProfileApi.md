# OpenAPI\Client\InstituteProfileApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getInstituteProfile()**](InstituteProfileApi.md#getInstituteProfile) | **GET** /api/v1/institute-profile | Current institute profile (created with defaults when missing). |
| [**updateInstituteProfile()**](InstituteProfileApi.md#updateInstituteProfile) | **PUT** /api/v1/institute-profile | Update the institute profile (institute_type and/or kapitalmarktorientiert). |


## `getInstituteProfile()`

```php
getInstituteProfile(): \OpenAPI\Client\Model\InstituteProfile
```

Current institute profile (created with defaults when missing).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InstituteProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getInstituteProfile();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstituteProfileApi->getInstituteProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\InstituteProfile**](../Model/InstituteProfile.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateInstituteProfile()`

```php
updateInstituteProfile($institute_profile_update): \OpenAPI\Client\Model\InstituteProfile
```

Update the institute profile (institute_type and/or kapitalmarktorientiert).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\InstituteProfileApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$institute_profile_update = new \OpenAPI\Client\Model\InstituteProfileUpdate(); // \OpenAPI\Client\Model\InstituteProfileUpdate

try {
    $result = $apiInstance->updateInstituteProfile($institute_profile_update);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstituteProfileApi->updateInstituteProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **institute_profile_update** | [**\OpenAPI\Client\Model\InstituteProfileUpdate**](../Model/InstituteProfileUpdate.md)|  | |

### Return type

[**\OpenAPI\Client\Model\InstituteProfile**](../Model/InstituteProfile.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
