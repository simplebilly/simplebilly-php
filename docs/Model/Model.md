# Model

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backup_codes** | **string[]** |  |
**created_at** | **\DateTime** |  |
**deleted_at** | **\DateTime** |  | [optional]
**email** | **string** |  |
**email_verified** | **bool** |  |
**id** | **string** |  |
**is_active** | **bool** |  |
**is_totp_enabled** | **bool** |  |
**last_login** | **\DateTime** |  | [optional]
**name** | **string** |  |
**oauth_id** | **string** |  | [optional]
**oauth_provider** | **string** |  | [optional]
**password_changed_at** | **\DateTime** | Set on password change; auth/refresh tokens issued before this timestamp are rejected by the auth middleware. | [optional]
**password_hash** | **string** |  |
**picture** | **string** |  | [optional]
**privacy_accepted_at** | **\DateTime** | When the user accepted the data privacy policy (GDPR consent record). | [optional]
**totp_secret** | **string** |  | [optional]
**updated_at** | **\DateTime** |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
