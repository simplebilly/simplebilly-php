# Rfq

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional]
**line_items** | **mixed** | JSON array of &#x60;{product_id, name, sku, quantity, requested_unit_price?, quoted_unit_price?}&#x60;. |
**notes** | **string** |  | [optional]
**requested_date** | **\DateTime** |  |
**response_date** | **\DateTime** |  | [optional]
**rfq_number** | **string** |  |
**status** | [**\OpenAPI\Client\Model\RfqStatus**](RfqStatus.md) | One of: draft | sent | offer_received | rejected | converted |
**supplier_contact_id** | **string** | References the supplier entity. | [optional]
**supplier_name** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
