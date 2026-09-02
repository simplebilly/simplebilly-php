# PurchaseOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional]
**delivery_address** | **mixed** |  | [optional]
**expected_delivery_date** | **\DateTime** |  | [optional]
**line_items** | **mixed** | JSON array of &#x60;{product_id, name, quantity, unit_price_net, tax_rate, delivery_date}&#x60;. | [optional]
**notes** | **string** |  | [optional]
**order_date** | **\DateTime** |  |
**po_number** | **string** |  |
**status** | [**\OpenAPI\Client\Model\PurchaseOrderStatus**](PurchaseOrderStatus.md) | One of: draft | ordered | partially_received | received | cancelled |
**supplier_contact_id** | **string** | References the supplier entity. | [optional]
**supplier_name** | **string** |  | [optional]
**total_gross_amount** | **string** |  | [optional]
**total_net_amount** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
