# CreateEmissionTarget
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BaseValue** | **String** |  | 
**BaseYear** | **Int32** |  | 
**Description** | **String** |  | 
**Scope** | **String** |  | 
**TargetValue** | **String** |  | 
**TargetYear** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$CreateEmissionTarget = Initialize-PSOpenAPIToolsCreateEmissionTarget  -BaseValue null `
 -BaseYear null `
 -Description null `
 -Scope null `
 -TargetValue null `
 -TargetYear null
```

- Convert the resource to JSON
```powershell
$CreateEmissionTarget | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

