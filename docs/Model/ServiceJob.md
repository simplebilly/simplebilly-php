# ServiceJob

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**address** | **string** | Street + zip + city of the job location. | [optional]
**customer_email** | **string** | Customer email for email notifications. | [optional]
**customer_id** | **string** | References the customer entity. | [optional]
**customer_name** | **string** | Denormalized customer name for quick display. | [optional]
**customer_phone** | **string** | Customer phone for SMS notifications later. | [optional]
**description** | **string** | What work needs to be done. | [optional]
**estimated_duration_minutes** | **int** | Estimated time for the job in minutes. | [optional]
**lat** | **float** | Latitude for map display (OpenStreetMap). | [optional]
**lng** | **float** | Longitude for map display (OpenStreetMap). | [optional]
**notes** | **string** |  | [optional]
**status** | [**\OpenAPI\Client\Model\ServiceJobStatus**](ServiceJobStatus.md) | Dispatch status: \&quot;pending\&quot;, \&quot;assigned\&quot;, \&quot;en_route\&quot;, \&quot;in_progress\&quot;, \&quot;completed\&quot;, \&quot;cancelled\&quot;. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
