# ApiResponseGdprExportData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activity_log** | [**\OpenAPI\Client\Model\GdprActivity[]**](GdprActivity.md) |  |
**api_keys** | [**\OpenAPI\Client\Model\GdprApiKey[]**](GdprApiKey.md) | Key identifiers and names only — never a usable credential. |
**billing** | [**\OpenAPI\Client\Model\GdprBillingInfo[]**](GdprBillingInfo.md) |  |
**exported_at** | **\DateTime** |  |
**generated_by_ai** | **bool** | Honesty field: this document is a plain data dump, never AI-generated. |
**notifications** | [**\OpenAPI\Client\Model\GdprNotification[]**](GdprNotification.md) |  |
**refresh_tokens** | [**\OpenAPI\Client\Model\GdprRefreshToken[]**](GdprRefreshToken.md) | Session records: metadata only, never the token hash. |
**tenants** | [**\OpenAPI\Client\Model\GdprTenant[]**](GdprTenant.md) |  |
**usage_events** | [**\OpenAPI\Client\Model\GdprUsageEvent[]**](GdprUsageEvent.md) |  |
**user** | [**\OpenAPI\Client\Model\GdprUser**](GdprUser.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
