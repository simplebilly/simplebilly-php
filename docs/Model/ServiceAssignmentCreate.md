# ServiceAssignmentCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**employee_id** | **string** | References the employees entity. | [optional]
**job_id** | **string** | References the service_jobs entity. | [optional]
**notes** | **string** |  | [optional]
**scheduled_date** | **\DateTime** | Work day the assignment is scheduled for. | [optional]
**scheduled_end** | **string** | Planned end time of the assignment. | [optional]
**scheduled_start** | **string** | Planned start time of the assignment. | [optional]
**status** | [**\OpenAPI\Client\Model\ServiceAssignmentStatus**](ServiceAssignmentStatus.md) | Assignment lifecycle status: \&quot;planned\&quot;, \&quot;confirmed\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot; or \&quot;cancelled\&quot;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
