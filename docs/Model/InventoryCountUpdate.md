# InventoryCountUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count_date** | **\DateTime** |  | [optional]
**count_number** | **string** |  | [optional]
**line_items** | **mixed** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. | [optional]
**notes** | **string** |  | [optional]
**status** | [**\OpenAPI\Client\Model\InventoryCountStatus**](InventoryCountStatus.md) | One of: draft | counting | reviewed | posted | [optional]
**warehouse_id** | **string** | References the warehouse entity. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
