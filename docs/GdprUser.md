# GdprUser
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **System.DateTime** |  | 
**Email** | **String** |  | 
**Id** | **String** |  | 
**Name** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GdprUser = Initialize-PSOpenAPIToolsGdprUser  -CreatedAt null `
 -Email null `
 -Id null `
 -Name null
```

- Convert the resource to JSON
```powershell
$GdprUser | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

