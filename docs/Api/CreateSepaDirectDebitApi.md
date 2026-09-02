# OpenAPI\Client\CreateSepaDirectDebitApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createSepaDirectDebitApi()**](CreateSepaDirectDebitApi.md#createSepaDirectDebitApi) | **POST** /api/v1/bookkeeping/sepa-direct-debit |  |


## `createSepaDirectDebitApi()`

```php
createSepaDirectDebitApi($creditor_name, $creditor_iban, $creditor_id, $mandate_id, $mandate_date, $debtor_name, $debtor_iban, $amount, $collection_date, $creditor_bic, $debtor_bic, $description): \OpenAPI\Client\Model\SepaDirectDebitResponse
```



### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\CreateSepaDirectDebitApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$creditor_name = 'creditor_name_example'; // string
$creditor_iban = 'creditor_iban_example'; // string
$creditor_id = 'creditor_id_example'; // string
$mandate_id = 'mandate_id_example'; // string
$mandate_date = 'mandate_date_example'; // string
$debtor_name = 'debtor_name_example'; // string
$debtor_iban = 'debtor_iban_example'; // string
$amount = 'amount_example'; // string
$collection_date = 'collection_date_example'; // string
$creditor_bic = 'creditor_bic_example'; // string
$debtor_bic = 'debtor_bic_example'; // string
$description = 'description_example'; // string

try {
    $result = $apiInstance->createSepaDirectDebitApi($creditor_name, $creditor_iban, $creditor_id, $mandate_id, $mandate_date, $debtor_name, $debtor_iban, $amount, $collection_date, $creditor_bic, $debtor_bic, $description);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CreateSepaDirectDebitApi->createSepaDirectDebitApi: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **creditor_name** | **string**|  | |
| **creditor_iban** | **string**|  | |
| **creditor_id** | **string**|  | |
| **mandate_id** | **string**|  | |
| **mandate_date** | **string**|  | |
| **debtor_name** | **string**|  | |
| **debtor_iban** | **string**|  | |
| **amount** | **string**|  | |
| **collection_date** | **string**|  | |
| **creditor_bic** | **string**|  | [optional] |
| **debtor_bic** | **string**|  | [optional] |
| **description** | **string**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\SepaDirectDebitResponse**](../Model/SepaDirectDebitResponse.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
