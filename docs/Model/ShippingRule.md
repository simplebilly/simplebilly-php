# ShippingRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**carrier** | **string** | Provider that auto-filled this rule (e.g. \&quot;ups\&quot;), if any. | [optional]
**country** | [**\OpenAPI\Client\Model\CountryCode**](CountryCode.md) | None &#x3D; applies to all countries. | [optional]
**delivery_time** | **string** | Delivery time text, e.g. \&quot;1-3\&quot;. | [optional]
**is_active** | **bool** |  | [optional]
**max_weight_kg** | **float** |  | [optional]
**min_weight_kg** | **float** |  | [optional]
**name** | **string** | Delivery-method label, e.g. \&quot;Standardversand\&quot;. |
**notes** | **string** |  | [optional]
**price** | **string** | Shipping cost in the shop&#39;s currency. |
**priority** | **int** | Lower wins when multiple rules match. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
