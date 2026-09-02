# Declaration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**declaration_type** | [**\OpenAPI\Client\Model\DeclarationType**](DeclarationType.md) | Art der Erklärung: \&quot;dcgk\&quot; (Entsprechenserklärung § 161 AktG) oder \&quot;unternehmensfuehrung\&quot; (Erklärung zur Unternehmensführung § 289f HGB). | [optional]
**is_current** | **bool** | Kennzeichnet die aktuell gültige Fassung (max. eine je Mandant). | [optional]
**text** | **string** | Inhalt der Erklärung als Markdown. | [optional]
**valid_from** | **\DateTime** | Datum, ab dem die Erklärung gilt. | [optional]
**version** | **string** | Versionsbezeichnung der Erklärung (z.B. \&quot;2025-01\&quot;). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
