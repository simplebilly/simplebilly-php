# WebhookSubscription

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_type** | **string** | Event type to react to (e.g. \&quot;order.created\&quot;); \&quot;*\&quot; &#x3D; all events. |
**is_active** | **bool** |  | [optional]
**name** | **string** | Human label (e.g. \&quot;Warehouse app\&quot;). |
**secret** | **string** | Shared secret for HMAC-SHA256 signature, sent as X-Signature. |
**url** | **string** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
