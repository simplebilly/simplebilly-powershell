# AcceptInviteRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FirstName** | **String** |  | 
**LastName** | **String** |  | 
**Password** | **String** |  | 
**PrivacyAccepted** | **Boolean** | GDPR consent — rejected unless true. | 
**Token** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$AcceptInviteRequest = Initialize-PSOpenAPIToolsAcceptInviteRequest  -FirstName null `
 -LastName null `
 -Password null `
 -PrivacyAccepted null `
 -Token null
```

- Convert the resource to JSON
```powershell
$AcceptInviteRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

