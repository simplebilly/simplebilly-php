# SupplierCondition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** | Currency for the minimum order value. |
**delivery_terms** | **string** | Incoterms, e.g. \&quot;EXW\&quot;, \&quot;DAP\&quot;. | [optional]
**early_payment_discount_percent** | **string** | Early-payment discount percentage (Skonto), e.g. 2.0. | [optional]
**is_default** | **bool** | Is this the default condition for the supplier? | [optional]
**minimum_order_value** | **string** | Minimum order value required for this supplier. | [optional]
**notes** | **string** |  | [optional]
**payment_due_days** | **int** | Number of days within which payment is due. | [optional]
**payment_terms** | **string** | Payment terms, e.g. \&quot;14 Tage, 2% Skonto\&quot;. | [optional]
**supplier_contact_id** | **string** | The supplier this condition applies to (&#x60;contact_id&#x60;). References the supplier entity. |
**supplier_name** | **string** | The name of the supplier, denormalized for easy listing. | [optional]
**volume_discount_tiers** | **mixed** | Tiered discounts: JSON array of &#x60;{min_quantity, discount_percent}&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
