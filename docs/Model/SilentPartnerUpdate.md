# SilentPartnerUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**contract_date** | **\DateTime** | Datum des Vertragsabschlusses. | [optional]
**einlage** | **string** | Einlage (§ 230 HGB). | [optional]
**gewinnquote_pct** | **string** | Gewinnbeteiligungsquote in Prozent (§ 231 HGB). | [optional]
**gewinnvortrag** | **string** | Nicht erhobene Gewinne (§ 232 Abs. 3 HGB). | [optional]
**instrument_type** | [**\OpenAPI\Client\Model\InstrumentType**](InstrumentType.md) | Instrument: \&quot;typisch\&quot; | \&quot;atypisch\&quot; | \&quot;partiarisches_darlehen\&quot; | \&quot;genussrecht\&quot;. | [optional]
**kest_pflichtig** | **bool** | 25 % Kapitalertragsteuer einbehalten (§ 43 Abs. 1 Nr. 3 EStG; typisch + partiarisches Darlehen). | [optional]
**name** | **string** | Name des stillen Gesellschafters. | [optional]
**notes** | **string** | Freitext-Notizen. | [optional]
**verlust_verrechnungskonto** | **string** | Kumulierte Verluste gegen die Einlage (§ 232 Abs. 2 HGB, ≤ Einlage). | [optional]
**verlustbeteiligung** | **bool** | Verlustbeteiligung (§ 231 Abs. 2 HGB; kann ausgeschlossen werden). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
