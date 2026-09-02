# OssDependency
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DependencyType** | **String** |  | 
**License** | **String** |  | [optional] 
**Name** | **String** |  | 
**Version** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$OssDependency = Initialize-PSOpenAPIToolsOssDependency  -DependencyType null `
 -License null `
 -Name null `
 -Version null
```

- Convert the resource to JSON
```powershell
$OssDependency | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

