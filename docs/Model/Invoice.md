# Invoice

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attachments** | **mixed** |  | [optional]
**billing_period_end** | **\DateTime** |  | [optional]
**billing_period_start** | **\DateTime** |  | [optional]
**cancellation_date** | **\DateTime** |  | [optional]
**cancellation_invoice_id** | **string** | References the invoice entity. | [optional]
**cancellation_reason** | **string** |  | [optional]
**contract_id** | **string** | References the contract entity. | [optional]
**currency** | [**\OpenAPI\Client\Model\CurrencyCode**](CurrencyCode.md) |  |
**customer_id** | **string** | References the customer entity. | [optional]
**discount_amount** | **string** |  | [optional]
**discount_days** | **int** |  | [optional]
**discount_percentage** | **string** |  | [optional]
**document_type** | [**\OpenAPI\Client\Model\DocumentType**](DocumentType.md) |  | [optional]
**dunning_level** | **int** |  | [optional]
**input_vat_amount** | **string** |  | [optional]
**input_vat_deductible** | **bool** |  | [optional]
**input_vat_percentage** | **string** |  | [optional]
**introduction_text** | **string** |  | [optional]
**invoice_type** | [**\OpenAPI\Client\Model\InvoiceType**](InvoiceType.md) |  |
**is_cancelled** | **bool** |  | [optional]
**is_draft** | **bool** |  | [optional]
**is_eu_acquisition** | **bool** |  | [optional]
**is_eu_delivery** | **bool** |  | [optional]
**is_intra_community_acquisition** | **bool** |  | [optional]
**is_reverse_charge** | **bool** |  | [optional]
**issue_date** | **\DateTime** |  |
**ledger_account** | **string** |  | [optional]
**line_items** | **mixed** |  |
**margin25a** | **bool** |  | [optional]
**margin25a_gross** | **string** |  | [optional]
**margin25a_purchase_price** | **string** |  | [optional]
**notes** | **string** |  | [optional]
**order_number** | **string** |  | [optional]
**original_pdf_path** | **string** |  | [optional]
**paid_amount** | **string** |  | [optional]
**payment_due_date** | **\DateTime** |  | [optional]
**payment_status** | [**\OpenAPI\Client\Model\PaymentStatus**](PaymentStatus.md) |  | [optional]
**payment_terms_text** | **string** |  | [optional]
**preceding_sales_voucher_id** | **string** | References the preceding sales voucher entity. | [optional]
**preceding_sales_voucher_type** | [**\OpenAPI\Client\Model\PrecedingSalesVoucherType**](PrecedingSalesVoucherType.md) |  | [optional]
**receipt_confirmation_available** | **bool** |  | [optional]
**related_invoice_id** | **string** | References the invoice entity. | [optional]
**relationship_type** | **string** |  | [optional]
**sender_snapshot** | **mixed** |  | [optional]
**sent_at** | **\DateTime** |  | [optional]
**service_period_end** | **\DateTime** |  | [optional]
**service_period_start** | **\DateTime** |  | [optional]
**status** | [**\OpenAPI\Client\Model\InvoiceStatus**](InvoiceStatus.md) |  |
**subtotal** | **string** |  |
**supplier_id** | **string** | References the supplier entity. | [optional]
**tax_exemption_reason** | **string** |  | [optional]
**total_amount** | **string** |  |
**total_tax** | **string** |  |
**vat_country** | [**\OpenAPI\Client\Model\CountryCode**](CountryCode.md) |  | [optional]
**vat_special_case** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
