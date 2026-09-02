# StockTransfer

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**line_items** | **mixed** | JSON array of &#x60;{product_id, name, quantity, batch_number?}&#x60;. |
**notes** | **string** |  | [optional]
**source_warehouse_id** | **string** | References the warehouse entity. |
**status** | [**\OpenAPI\Client\Model\StockTransferStatus**](StockTransferStatus.md) | One of: draft | completed | cancelled |
**target_warehouse_id** | **string** | References the warehouse entity. |
**transfer_date** | **\DateTime** |  |
**transfer_number** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
