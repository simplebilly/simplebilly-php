# Job

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**attempts** | **int** |  | [optional]
**job_type** | **string** | Discriminator the worker dispatches on (e.g. \&quot;webhook.deliver\&quot;). |
**max_attempts** | **int** |  |
**payload** | **mixed** |  | [optional]
**run_at** | **\DateTime** | Earliest execution time; None &#x3D; run now. | [optional]
**status** | [**\OpenAPI\Client\Model\JobStatus**](JobStatus.md) | pending | running | done | failed |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
