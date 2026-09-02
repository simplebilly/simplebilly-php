# GoodsReceipt

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**gr_number** | **string** |  |
**line_items** | **mixed** | JSON array of &#x60;{product_id, name, quantity, batch_number?, expiry_date?, bin_location?}&#x60;. |
**notes** | **string** |  | [optional]
**purchase_order_id** | **string** | References the purchase order entity. | [optional]
**receipt_date** | **\DateTime** |  |
**supplier_contact_id** | **string** | References the supplier entity. | [optional]
**supplier_name** | **string** |  | [optional]
**warehouse_id** | **string** | References the warehouse entity. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
