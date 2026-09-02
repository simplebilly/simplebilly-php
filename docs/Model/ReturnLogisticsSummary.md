# ReturnLogisticsSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**by_status** | **mixed** | Number of return orders per status. |
**by_warehouse** | [**\OpenAPI\Client\Model\ReturnWarehouseSummary[]**](ReturnWarehouseSummary.md) | Per-warehouse aggregation. |
**items_restocked** | **int** | Sum of &#x60;restock: true&#x60; line-item quantities. |
**items_scrapped** | **int** | Sum of &#x60;restock: false&#x60; line-item quantities (scrapped/disposed). |
**total_items** | **int** | Sum of all line-item quantities across returns. |
**total_returns** | **int** | Total number of return orders (excluding soft-deleted). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
