# ApiResponseUserProfileData
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**Email** | **String** |  | 
**EmailVerified** | **Boolean** |  | 
**FirstName** | **String** |  | 
**FullName** | **String** |  | 
**Id** | **String** |  | 
**LastName** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ApiResponseUserProfileData = Initialize-PSOpenAPIToolsApiResponseUserProfileData  -CreatedAt null `
 -Email null `
 -EmailVerified null `
 -FirstName null `
 -FullName null `
 -Id null `
 -LastName null
```

- Convert the resource to JSON
```powershell
$ApiResponseUserProfileData | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

