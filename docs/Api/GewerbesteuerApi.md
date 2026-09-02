# OpenAPI\Client\GewerbesteuerApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**gewerbesteuerApi()**](GewerbesteuerApi.md#gewerbesteuerApi) | **GET** /api/v1/bookkeeping/gewerbesteuer |  |


## `gewerbesteuerApi()`

```php
gewerbesteuerApi($year, $hebesatz, $gewerbeertrag, $country, $gemeindeschluessel): \OpenAPI\Client\Model\GewerbesteuerErgebnis
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GewerbesteuerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$year = 56; // int
$hebesatz = 'hebesatz_example'; // string
$gewerbeertrag = 'gewerbeertrag_example'; // string
$country = 'country_example'; // string
$gemeindeschluessel = 'gemeindeschluessel_example'; // string

try {
    $result = $apiInstance->gewerbesteuerApi($year, $hebesatz, $gewerbeertrag, $country, $gemeindeschluessel);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GewerbesteuerApi->gewerbesteuerApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **year** | **int**|  | |
| **hebesatz** | **string**|  | [optional] |
| **gewerbeertrag** | **string**|  | [optional] |
| **country** | **string**|  | [optional] |
| **gemeindeschluessel** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GewerbesteuerErgebnis**](../Model/GewerbesteuerErgebnis.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
