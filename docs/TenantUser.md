# TenantUser
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **String** |  | 
**EmailVerified** | **Boolean** |  | 
**IsActive** | **Boolean** |  | 
**JoinedAt** | **System.DateTime** |  | 
**LastLogin** | **System.DateTime** |  | [optional] 
**Name** | **String** |  | 
**Permissions** | **String[]** |  | 
**Role** | **String** |  | 
**UserId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$TenantUser = Initialize-PSOpenAPIToolsTenantUser  -Email null `
 -EmailVerified null `
 -IsActive null `
 -JoinedAt null `
 -LastLogin null `
 -Name null `
 -Permissions null `
 -Role null `
 -UserId null
```

- Convert the resource to JSON
```powershell
$TenantUser | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

