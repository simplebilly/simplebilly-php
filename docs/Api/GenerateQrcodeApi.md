# OpenAPI\Client\GenerateQrcodeApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**generateQrcodeApi()**](GenerateQrcodeApi.md#generateQrcodeApi) | **GET** /api/v1/invoices/{id}/qrcode |  |


## `generateQrcodeApi()`

```php
generateQrcodeApi($iban, $id, $holder_name, $bic, $amount, $reference, $purpose): \OpenAPI\Client\Model\QRCodeResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\GenerateQrcodeApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$iban = 'iban_example'; // string
$id = 'id_example'; // string
$holder_name = 'holder_name_example'; // string
$bic = 'bic_example'; // string
$amount = 'amount_example'; // string
$reference = 'reference_example'; // string
$purpose = 'purpose_example'; // string

try {
    $result = $apiInstance->generateQrcodeApi($iban, $id, $holder_name, $bic, $amount, $reference, $purpose);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GenerateQrcodeApi->generateQrcodeApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **iban** | **string**|  | |
| **id** | **string**|  | |
| **holder_name** | **string**|  | [optional] |
| **bic** | **string**|  | [optional] |
| **amount** | **string**|  | [optional] |
| **reference** | **string**|  | [optional] |
| **purpose** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\QRCodeResponse**](../Model/QRCodeResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
