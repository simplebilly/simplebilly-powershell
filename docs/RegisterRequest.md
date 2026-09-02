# RegisterRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CompanyName** | **String** |  | 
**Email** | **String** |  | 
**FirstName** | **String** |  | 
**LastName** | **String** |  | 
**Password** | **String** |  | 
**PrivacyAccepted** | **Boolean** | GDPR consent — registration is rejected unless true. | 

## Examples

- Prepare the resource
```powershell
$RegisterRequest = Initialize-PSOpenAPIToolsRegisterRequest  -CompanyName null `
 -Email null `
 -FirstName null `
 -LastName null `
 -Password null `
 -PrivacyAccepted null
```

- Convert the resource to JSON
```powershell
$RegisterRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

