# InventoryCountCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**count_date** | **\DateTime** |  |
**count_number** | **string** |  |
**line_items** | **mixed** | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. |
**notes** | **string** |  | [optional]
**status** | [**\OpenAPI\Client\Model\InventoryCountStatus**](InventoryCountStatus.md) | One of: draft | counting | reviewed | posted |
**warehouse_id** | **string** | References the warehouse entity. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
