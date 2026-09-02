# CustomerCommunication

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**body** | **string** | The message body, call summary or note text. | [optional]
**channel** | [**\OpenAPI\Client\Model\CommunicationChannel**](CommunicationChannel.md) |  |
**contact_id** | **string** | The contact (customer/supplier) this communication belongs to. References the contact entity. |
**counterparty** | **string** | Email/phone of the counterparty, if applicable. | [optional]
**direction** | [**\OpenAPI\Client\Model\CommunicationDirection**](CommunicationDirection.md) |  |
**occurred_at** | **\DateTime** | When the communication happened (defaults to now on create). | [optional]
**subject** | **string** |  | [optional]
**tags** | **mixed** | Free-form tags, e.g. &#x60;[\&quot;follow-up-required\&quot;]&#x60;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
