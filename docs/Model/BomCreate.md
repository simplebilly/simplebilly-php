# BomCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**components** | **mixed** | JSON array of &#x60;{product_id, name, quantity, unit, scrap_rate}&#x60;. | [optional]
**description** | **string** |  | [optional]
**name** | **string** |  |
**output_quantity** | **int** | Output quantity per production run (defaults to 1). | [optional]
**product_id** | **string** | The finished product this BOM produces. References the product entity. |
**status** | [**\OpenAPI\Client\Model\BomStatus**](BomStatus.md) | One of: draft | active | archived | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
