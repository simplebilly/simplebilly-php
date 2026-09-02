# ActivityCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activity_type** | [**\OpenAPI\Client\Model\ActivityType**](ActivityType.md) | One of: call | email | meeting | task | note |
**assigned_to** | **string** | User responsible (&#x60;employee.employee_id&#x60;). | [optional]
**contact_id** | **string** | Contact this activity belongs to (&#x60;contact.contact_id&#x60;). References the contact entity. | [optional]
**description** | **string** |  | [optional]
**due_date** | **\DateTime** | Follow-up / Wiedervorlage date. Open activities with a due date in the past are overdue. | [optional]
**reminder_date** | **\DateTime** | When to remind about the follow-up. | [optional]
**status** | [**\OpenAPI\Client\Model\ActivityStatus**](ActivityStatus.md) | One of: open | done | cancelled |
**subject** | **string** | Short subject line. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
