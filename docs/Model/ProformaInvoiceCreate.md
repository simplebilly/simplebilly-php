# ProformaInvoiceCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**converted_at** | **\DateTime** |  | [optional]
**converted_to_invoice_id** | **string** | Set when the proforma was converted into a real invoice. References the invoice entity. | [optional]
**currency** | [**\OpenAPI\Client\Model\CurrencyCode**](CurrencyCode.md) |  |
**customer_id** | **string** | References the customer entity. | [optional]
**customer_snapshot** | **mixed** | Snapshot of the recipient at issue time (address, VAT id, …). | [optional]
**issue_date** | **\DateTime** |  |
**line_items** | **mixed** |  |
**notes** | **string** |  | [optional]
**order_number** | **string** | Reference to the order/quote this proforma belongs to. | [optional]
**payment_due_date** | **\DateTime** | Optional deadline the real invoice should carry after conversion. | [optional]
**quotation_id** | **string** | References the quotation entity. | [optional]
**status** | [**\OpenAPI\Client\Model\ProformaInvoiceStatus**](ProformaInvoiceStatus.md) | &#x60;draft&#x60; | &#x60;sent&#x60; | &#x60;converted&#x60;. |
**subtotal** | **string** |  |
**total_amount** | **string** |  |
**total_tax** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
