# OpenAPI\Client\GezApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**gezApi()**](GezApi.md#gezApi) | **GET** /api/v1/bookkeeping/gez |  |


## `gezApi()`

```php
gezApi($jahr, $betriebsstaetten, $kfz, $hotelzimmer, $beschaefigte): \OpenAPI\Client\Model\GezReport
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GezApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$jahr = 56; // int
$betriebsstaetten = 'betriebsstaetten_example'; // string | Liste der Betriebsstätten als JSON, z.B. `[{\"name\":\"Filiale 1\",\"beschaefigte\":12}]`.
$kfz = 56; // int | Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind).
$hotelzimmer = 56; // int | Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen.
$beschaefigte = 56; // int | Gesamtzahl der Beschäftigten (verwendet nur, wenn `betriebsstaetten` fehlt; dann wird eine einzelne Betriebsstätte angenommen).

try {
    $result = $apiInstance->gezApi($jahr, $betriebsstaetten, $kfz, $hotelzimmer, $beschaefigte);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GezApi->gezApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **jahr** | **int**|  | [optional] |
| **betriebsstaetten** | **string**| Liste der Betriebsstätten als JSON, z.B. &#x60;[{\&quot;name\&quot;:\&quot;Filiale 1\&quot;,\&quot;beschaefigte\&quot;:12}]&#x60;. | [optional] |
| **kfz** | **int**| Gesamtzahl der betrieblich genutzten Kfz (falls keine Betriebsstätten angegeben sind). | [optional] |
| **hotelzimmer** | **int**| Gesamtzahl der Hotel-/Gästezimmer und Ferienwohnungen. | [optional] |
| **beschaefigte** | **int**| Gesamtzahl der Beschäftigten (verwendet nur, wenn &#x60;betriebsstaetten&#x60; fehlt; dann wird eine einzelne Betriebsstätte angenommen). | [optional] |

### Return type

[**\OpenAPI\Client\Model\GezReport**](../Model/GezReport.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
