# UpdateProfileRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AvatarUrl** | **String** |  | [optional] 
**FirstName** | **String** |  | [optional] 
**LastName** | **String** |  | [optional] 
**Name** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$UpdateProfileRequest = Initialize-PSOpenAPIToolsUpdateProfileRequest  -AvatarUrl null `
 -FirstName null `
 -LastName null `
 -Name null
```

- Convert the resource to JSON
```powershell
$UpdateProfileRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

