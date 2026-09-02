# ProductVariant

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**barcode** | **string** |  | [optional]
**image_link** | **string** |  | [optional]
**is_active** | **bool** |  | [optional]
**name** | **string** | Human-readable variant label, e.g. \&quot;Red / M\&quot;. | [optional]
**option_values** | **mixed** | Option name → value map, e.g. &#x60;{\&quot;Color\&quot;: \&quot;Red\&quot;, \&quot;Size\&quot;: \&quot;M\&quot;}&#x60;. | [optional]
**price** | **string** | Explicit override price for this variant (takes precedence over parent price + delta). | [optional]
**price_delta** | **string** | Price adjustment relative to the parent product&#39;s &#x60;default_price&#x60;. | [optional]
**product_id** | **string** | The parent product this variant belongs to. References the product entity. |
**sku** | **string** | Variant-specific SKU (must be unique per tenant). |
**stock_quantity** | **int** | Variant-level stock (optional — may be tracked on the parent only). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
