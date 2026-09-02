# ConfigFieldInfo
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Kind** | [**ConfigFieldKind**](ConfigFieldKind.md) |  | 
**Label** | **String** |  | 
**Name** | **String** |  | 
**Placeholder** | **String** |  | [optional] 
**Required** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$ConfigFieldInfo = Initialize-PSOpenAPIToolsConfigFieldInfo  -Kind null `
 -Label null `
 -Name null `
 -Placeholder null `
 -Required null
```

- Convert the resource to JSON
```powershell
$ConfigFieldInfo | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

