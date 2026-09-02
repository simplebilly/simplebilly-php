# WebhookEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **int** |  | [optional]
**channel** | **string** | source for inbound, target URL for outbound. | [optional]
**direction** | [**\OpenAPI\Client\Model\WebhookDirection**](WebhookDirection.md) | inbound | outbound |
**event_type** | **string** |  |
**last_error** | **string** |  | [optional]
**payload** | **mixed** |  | [optional]
**status** | [**\OpenAPI\Client\Model\WebhookEventStatus**](WebhookEventStatus.md) | accepted | delivered | failed | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
