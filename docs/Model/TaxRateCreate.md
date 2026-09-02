# TaxRateCreate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country_code** | **string** | ISO 3166-1 alpha-2 country code. |
**effective_from** | **\DateTime** | Date this rate took effect; &#x60;None&#x60; &#x3D; not date-bound. | [optional]
**is_default** | **bool** | Default rate for the country (one per country); fallback for lookups when no dated rate applies. |
**name** | **string** | Human name, e.g. \&quot;VAT\&quot;. |
**rate_percent** | **int** | Rate in hundredths of a percent: 1900 &#x3D; 19.00%. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
