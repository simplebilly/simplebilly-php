# OpenAPI\Client\LegalDocumentApi



All URIs are relative to https://demo.simplebilly.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getLegalDocuments()**](LegalDocumentApi.md#getLegalDocuments) | **GET** /api/v1/legal/documents | List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access. |
| [**resetLegalDocuments()**](LegalDocumentApi.md#resetLegalDocuments) | **POST** /api/v1/legal/documents/reset | Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list. |
| [**upsertLegalDocuments()**](LegalDocumentApi.md#upsertLegalDocuments) | **PUT** /api/v1/legal/documents | Upsert legal documents per (doc_type, lang). Returns the full tenant list. |


## `getLegalDocuments()`

```php
getLegalDocuments(): \OpenAPI\Client\Model\LegalDocument[]
```

List all legal documents of the tenant. Missing documents are seeded from the default texts (with tenant placeholders replaced) on first access.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LegalDocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->getLegalDocuments();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalDocumentApi->getLegalDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\LegalDocument[]**](../Model/LegalDocument.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `resetLegalDocuments()`

```php
resetLegalDocuments($legal_document_reset): \OpenAPI\Client\Model\LegalDocument[]
```

Restore default texts for all documents (or a single doc_type/lang when the optional filter is given). Returns the full tenant list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LegalDocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$legal_document_reset = new \OpenAPI\Client\Model\LegalDocumentReset(); // \OpenAPI\Client\Model\LegalDocumentReset

try {
    $result = $apiInstance->resetLegalDocuments($legal_document_reset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalDocumentApi->resetLegalDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **legal_document_reset** | [**\OpenAPI\Client\Model\LegalDocumentReset**](../Model/LegalDocumentReset.md)|  | |

### Return type

[**\OpenAPI\Client\Model\LegalDocument[]**](../Model/LegalDocument.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `upsertLegalDocuments()`

```php
upsertLegalDocuments($legal_document_upsert): \OpenAPI\Client\Model\LegalDocument[]
```

Upsert legal documents per (doc_type, lang). Returns the full tenant list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearer_token
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\LegalDocumentApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$legal_document_upsert = array(new \OpenAPI\Client\Model\LegalDocumentUpsert()); // \OpenAPI\Client\Model\LegalDocumentUpsert[]

try {
    $result = $apiInstance->upsertLegalDocuments($legal_document_upsert);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling LegalDocumentApi->upsertLegalDocuments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **legal_document_upsert** | [**\OpenAPI\Client\Model\LegalDocumentUpsert[]**](../Model/LegalDocumentUpsert.md)|  | |

### Return type

[**\OpenAPI\Client\Model\LegalDocument[]**](../Model/LegalDocument.md)

### Authorization

[bearer_token](../../README.md#bearer_token)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
