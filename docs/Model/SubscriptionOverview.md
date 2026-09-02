# SubscriptionOverview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**current_period_end** | **\DateTime** |  | [optional]
**features** | [**\OpenAPI\Client\Model\PlanFeatures**](PlanFeatures.md) |  |
**is_trialing** | **bool** |  |
**limits** | [**\OpenAPI\Client\Model\PlanLimits**](PlanLimits.md) |  |
**manage_url** | **string** |  | [optional]
**plan** | **string** | Resolved plan id (free/starter/business/enterprise, or a custom override id). |
**plan_name** | **string** |  |
**price_eur** | **float** | Monthly price in EUR; &#x60;-1.0&#x60; &#x3D; custom pricing (enterprise). |
**quantity** | **int** |  | [optional]
**status** | **string** |  | [optional]
**subscription_id** | **string** |  | [optional]
**trial_ends_at** | **\DateTime** |  | [optional]
**usage** | [**\OpenAPI\Client\Model\UsageSnapshot**](UsageSnapshot.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
