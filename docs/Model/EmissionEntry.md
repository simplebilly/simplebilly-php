# EmissionEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**activity_value** | **string** | Activity amount in &#x60;unit&#x60; (kWh, l, km, t, tkm, EUR). |
**category_id** | **string** | GHG-Protocol category key, e.g. \&quot;purchased_goods\&quot;, \&quot;business_travel\&quot;. |
**description** | **string** |  |
**ef_source** | **string** | Emission-factor source, e.g. \&quot;UBA-2024\&quot;, \&quot;DEFRA-2024\&quot;. |
**ef_version** | **string** |  |
**method** | [**\OpenAPI\Client\Model\EmissionMethod**](EmissionMethod.md) | \&quot;activity\&quot; | \&quot;spend\&quot; | \&quot;supplier\&quot;. |
**scope** | [**\OpenAPI\Client\Model\GhgScope**](GhgScope.md) | GHG scope: \&quot;1\&quot; | \&quot;2\&quot; | \&quot;3\&quot;. |
**tco2e** | **string** | Computed server-side: activity * factor / 1000, rounded to 4 dp. |
**unit** | **string** | Unit of the activity value. |
**updated_at** | **\DateTime** |  | [optional]
**year** | **int** | Reporting year. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
