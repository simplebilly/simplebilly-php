# SupplierInvoiceUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional]
**goods_receipt_id** | **string** | References the goods receipt entity. | [optional]
**invoice_date** | **\DateTime** |  | [optional]
**invoice_number** | **string** |  | [optional]
**line_items** | **mixed** | JSON array of &#x60;{product_id, name, quantity, unitPriceNet, taxRate}&#x60;. | [optional]
**notes** | **string** |  | [optional]
**purchase_order_id** | **string** | References the purchase order entity. | [optional]
**status** | [**\OpenAPI\Client\Model\SupplierInvoiceStatus**](SupplierInvoiceStatus.md) | One of: draft | matched | has_variances | posted | cancelled | [optional]
**supplier_contact_id** | **string** | References the supplier entity. | [optional]
**supplier_name** | **string** |  | [optional]
**total_gross_amount** | **string** |  | [optional]
**total_net_amount** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
