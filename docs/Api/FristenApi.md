# OpenAPI\Client\FristenApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**fristenApi()**](FristenApi.md#fristenApi) | **GET** /api/v1/bookkeeping/fristen |  |


## `fristenApi()`

```php
fristenApi($bundesland, $voranmeldungsrhythmus, $dauerfristverlaengerung, $est_aktiv, $gewst_aktiv, $monate): \OpenAPI\Client\Model\FristenErgebnis
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\FristenApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$bundesland = 'bundesland_example'; // string
$voranmeldungsrhythmus = 'voranmeldungsrhythmus_example'; // string
$dauerfristverlaengerung = True; // bool
$est_aktiv = True; // bool
$gewst_aktiv = True; // bool
$monate = 56; // int

try {
    $result = $apiInstance->fristenApi($bundesland, $voranmeldungsrhythmus, $dauerfristverlaengerung, $est_aktiv, $gewst_aktiv, $monate);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling FristenApi->fristenApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **bundesland** | **string**|  | [optional] |
| **voranmeldungsrhythmus** | **string**|  | [optional] |
| **dauerfristverlaengerung** | **bool**|  | [optional] |
| **est_aktiv** | **bool**|  | [optional] |
| **gewst_aktiv** | **bool**|  | [optional] |
| **monate** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\FristenErgebnis**](../Model/FristenErgebnis.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
