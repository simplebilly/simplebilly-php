# StockMovement

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**delta** | **int** | Signed movement: positive &#x3D; into stock, negative &#x3D; out of stock. |
**movement_type** | [**\OpenAPI\Client\Model\MovementType**](MovementType.md) | One of the &#x60;MOVEMENT_*&#x60; constants. |
**product_id** | **string** | References the product entity. |
**quantity** | **int** | Absolute quantity moved (always &gt;&#x3D; 0). |
**reason** | **string** |  | [optional]
**reference_id** | **string** | Primary-key of the referencing entity. | [optional]
**reference_type** | [**\OpenAPI\Client\Model\ReferenceType**](ReferenceType.md) | Entity that caused the movement, e.g. &#x60;goods_receipt&#x60;, &#x60;stock_transfer&#x60;. | [optional]
**warehouse_id** | **string** | References the warehouse entity. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
