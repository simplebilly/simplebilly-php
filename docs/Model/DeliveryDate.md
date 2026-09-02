# DeliveryDate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | **string** | References the customer entity. | [optional]
**fulfilled_date** | **\DateTime** | Date actually delivered (set on fulfillment). | [optional]
**note** | **string** |  | [optional]
**order_number** | **string** | Sales order number (&#x60;order.order_number&#x60;). |
**original_date** | **\DateTime** | Original date promised before rescheduling. | [optional]
**product_id** | **string** | Product line item this date applies to, if per-item. References the product entity. | [optional]
**promised_date** | **\DateTime** | Date promised to the customer. |
**status** | [**\OpenAPI\Client\Model\DeliveryDateStatus**](DeliveryDateStatus.md) | One of: promised | confirmed | rescheduled | fulfilled | late | cancelled |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
