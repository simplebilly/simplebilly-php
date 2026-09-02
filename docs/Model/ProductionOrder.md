# ProductionOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bom_id** | **string** | References the BOM entity. | [optional]
**components** | **mixed** | JSON snapshot of the BOM components at creation time. | [optional]
**end_date** | **\DateTime** |  | [optional]
**notes** | **string** |  | [optional]
**order_number** | **string** |  |
**product_id** | **string** | The finished product to manufacture. References the product entity. |
**quantity** | **int** | Quantity of finished product to produce. |
**source_warehouse_id** | **string** | Warehouse components are consumed from. References the warehouse entity. | [optional]
**start_date** | **\DateTime** |  | [optional]
**status** | [**\OpenAPI\Client\Model\ProductionOrderStatus**](ProductionOrderStatus.md) | One of: planned | in_production | completed | cancelled | [optional]
**target_warehouse_id** | **string** | Warehouse the finished product is added to. References the warehouse entity. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
