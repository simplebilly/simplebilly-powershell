# MeteredUsage
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Limit** | **Int64** |  | 
**Meter** | **String** |  | 
**Used** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$MeteredUsage = Initialize-PSOpenAPIToolsMeteredUsage  -Limit null `
 -Meter null `
 -Used null
```

- Convert the resource to JSON
```powershell
$MeteredUsage | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

