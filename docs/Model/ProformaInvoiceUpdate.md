# ProformaInvoiceUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**converted_at** | **\DateTime** |  | [optional]
**converted_to_invoice_id** | **string** | Set when the proforma was converted into a real invoice. References the invoice entity. | [optional]
**currency** | [**\OpenAPI\Client\Model\CurrencyCode**](CurrencyCode.md) |  | [optional]
**customer_id** | **string** | References the customer entity. | [optional]
**customer_snapshot** | **mixed** | Snapshot of the recipient at issue time (address, VAT id, …). | [optional]
**issue_date** | **\DateTime** |  | [optional]
**line_items** | **mixed** |  | [optional]
**notes** | **string** |  | [optional]
**order_number** | **string** | Reference to the order/quote this proforma belongs to. | [optional]
**payment_due_date** | **\DateTime** | Optional deadline the real invoice should carry after conversion. | [optional]
**quotation_id** | **string** | References the quotation entity. | [optional]
**status** | [**\OpenAPI\Client\Model\ProformaInvoiceStatus**](ProformaInvoiceStatus.md) | &#x60;draft&#x60; | &#x60;sent&#x60; | &#x60;converted&#x60;. | [optional]
**subtotal** | **string** |  | [optional]
**total_amount** | **string** |  | [optional]
**total_tax** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
