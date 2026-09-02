# AbsenceCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**absence_type** | [**\OpenAPI\Client\Model\AbsenceType**](AbsenceType.md) | One of \&quot;vacation\&quot;, \&quot;sick\&quot;, \&quot;sabbatical\&quot;, \&quot;parental\&quot;, \&quot;other\&quot;. | [optional]
**approved_at** | **\DateTime** |  | [optional]
**approved_by** | **string** | References the user entity. | [optional]
**employee_id** | **string** | References the employee entity. | [optional]
**end_date** | **\DateTime** |  | [optional]
**notes** | **string** |  | [optional]
**start_date** | **\DateTime** |  | [optional]
**status** | [**\OpenAPI\Client\Model\AbsenceStatus**](AbsenceStatus.md) | One of \&quot;pending\&quot;, \&quot;approved\&quot;, \&quot;rejected\&quot;, \&quot;cancelled\&quot;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
