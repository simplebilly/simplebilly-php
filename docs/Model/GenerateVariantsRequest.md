# GenerateVariantsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**options** | **array<string,string[]>** | Option name → list of values, e.g. &#x60;{\&quot;Color\&quot;: [\&quot;Red\&quot;, \&quot;Blue\&quot;], \&quot;Size\&quot;: [\&quot;S\&quot;, \&quot;M\&quot;]}&#x60;. The cartesian product of these lists is generated. | [optional]
**price_delta** | **string** | Optional per-variant price delta applied to every generated variant. | [optional]
**product_id** | **string** |  |
**sku_prefix** | **string** | Optional prefix for the generated SKUs (suffix is the option values joined by &#x60;-&#x60;). Falls back to the parent product&#39;s SKU. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
