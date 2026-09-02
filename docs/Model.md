# Model
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BackupCodes** | **String[]** |  | 
**CreatedAt** | **System.DateTime** |  | 
**DeletedAt** | **System.DateTime** |  | [optional] 
**Email** | **String** |  | 
**EmailVerified** | **Boolean** |  | 
**Id** | **String** |  | 
**IsActive** | **Boolean** |  | 
**IsTotpEnabled** | **Boolean** |  | 
**LastLogin** | **System.DateTime** |  | [optional] 
**Name** | **String** |  | 
**OauthId** | **String** |  | [optional] 
**OauthProvider** | **String** |  | [optional] 
**PasswordChangedAt** | **System.DateTime** | Set on password change; auth/refresh tokens issued before this timestamp are rejected by the auth middleware. | [optional] 
**PasswordHash** | **String** |  | 
**Picture** | **String** |  | [optional] 
**PrivacyAcceptedAt** | **System.DateTime** | When the user accepted the data privacy policy (GDPR consent record). | [optional] 
**TotpSecret** | **String** |  | [optional] 
**UpdatedAt** | **System.DateTime** |  | 

## Examples

- Prepare the resource
```powershell
$Model = Initialize-PSOpenAPIToolsModel  -BackupCodes null `
 -CreatedAt null `
 -DeletedAt null `
 -Email null `
 -EmailVerified null `
 -Id null `
 -IsActive null `
 -IsTotpEnabled null `
 -LastLogin null `
 -Name null `
 -OauthId null `
 -OauthProvider null `
 -PasswordChangedAt null `
 -PasswordHash null `
 -Picture null `
 -PrivacyAcceptedAt null `
 -TotpSecret null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$Model | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

