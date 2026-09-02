# EmployeeUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **string** |  | [optional]
**backup_employee_id** | **string** | References another employee who covers when this employee is absent. | [optional]
**bic** | **string** |  | [optional]
**city** | **string** |  | [optional]
**country** | [**\OpenAPI\Client\Model\CountryCode**](CountryCode.md) |  | [optional]
**date_of_birth** | **\DateTime** |  | [optional]
**department_id** | **string** | References the department entity. | [optional]
**email** | **string** |  | [optional]
**first_name** | **string** |  | [optional]
**gender** | [**\OpenAPI\Client\Model\Gender**](Gender.md) | Gender for pay-transparency reporting: \&quot;male\&quot;, \&quot;female\&quot; or \&quot;diverse\&quot;. | [optional]
**hire_date** | **\DateTime** |  | [optional]
**hourly_cost** | **string** | Hourly cost rate in EUR for labor-cost reporting; when unset the rate is derived from &#x60;monthly_salary / (weekly_hours * 4.33)&#x60;. | [optional]
**iban** | **string** |  | [optional]
**job_title** | **string** |  | [optional]
**last_login** | **\DateTime** |  | [optional]
**last_name** | **string** |  | [optional]
**last_updated** | **\DateTime** |  | [optional]
**monthly_salary** | **string** | Gross monthly salary in EUR for pay-transparency reporting. | [optional]
**phone** | **string** |  | [optional]
**state** | **string** |  | [optional]
**status** | [**\OpenAPI\Client\Model\EmployeeStatus**](EmployeeStatus.md) |  | [optional]
**user_id** | **string** | References the user entity. | [optional]
**weekly_hours** | **string** | Contractual weekly working hours for pay-transparency normalization. | [optional]
**zip** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
