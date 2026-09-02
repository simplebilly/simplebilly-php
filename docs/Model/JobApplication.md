# JobApplication

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cv_file** | **string** | Relative path of the stored CV file under the upload dir. | [optional]
**cv_text** | **string** | Extracted CV text, used for match-scoring. | [optional]
**email** | **string** |  | [optional]
**match_reason** | **string** |  | [optional]
**match_score** | **int** | 0-100 LLM match score against the posting&#39;s required profile. | [optional]
**name** | **string** |  | [optional]
**phone** | **string** |  | [optional]
**posting_id** | **string** | References the job_posting entity. | [optional]
**source** | **string** | website | email | board |
**status** | [**\OpenAPI\Client\Model\ApplicationStatus**](ApplicationStatus.md) | new | reviewing | interview | hired | rejected |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
