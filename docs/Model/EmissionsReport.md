# EmissionsReport

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**by_category** | [**\OpenAPI\Client\Model\CategoryTotal[]**](CategoryTotal.md) |  |
**by_scope** | [**\OpenAPI\Client\Model\ScopeTotal[]**](ScopeTotal.md) |  |
**by_year** | [**\OpenAPI\Client\Model\YearTotal[]**](YearTotal.md) |  |
**data_quality** | [**\OpenAPI\Client\Model\DataQuality**](DataQuality.md) |  |
**intensity_per_employee** | **float** |  | [optional]
**intensity_per_revenue_mio** | **float** | tCO2e per million EUR net revenue. | [optional]
**net_revenue** | **float** | Sum of paid/sent/partially-paid invoices (EUR net) in the year. | [optional]
**spend_based_estimate_tco2e** | **float** | Spend-based estimate from bookkeeping payments (EXIOBASE factor). | [optional]
**targets** | [**\OpenAPI\Client\Model\TargetProgress[]**](TargetProgress.md) |  |
**total_tco2e** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
