# JobPostingUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**currency** | **string** |  | [optional]
**department** | **string** |  | [optional]
**description** | **string** | What the job is; markdown/HTML. | [optional]
**employment_type** | [**\OpenAPI\Client\Model\EmploymentType**](EmploymentType.md) | full_time | part_time | contract | internship | temporary | [optional]
**location** | **string** |  | [optional]
**remote** | **bool** |  | [optional]
**required_skills** | **mixed** | List of required skill names (JSON array of strings). | [optional]
**requirements** | **string** | Structured profile of the required candidate (skills, experience). | [optional]
**salary_max** | **int** |  | [optional]
**salary_min** | **int** |  | [optional]
**status** | [**\OpenAPI\Client\Model\JobPostingStatus**](JobPostingStatus.md) | draft | published | closed | [optional]
**title** | **string** |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
