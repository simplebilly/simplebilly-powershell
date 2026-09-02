# TargetProgress
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BaseValue** | **Double** |  | 
**BaseYear** | **Int32** |  | 
**Description** | **String** |  | 
**Id** | **String** |  | 
**ProgressPct** | **Double** | Current year&#39;s emissions for the scope as % of the target. None when no data. | [optional] 
**Scope** | **String** |  | 
**TargetValue** | **Double** |  | 
**TargetYear** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$TargetProgress = Initialize-PSOpenAPIToolsTargetProgress  -BaseValue null `
 -BaseYear null `
 -Description null `
 -Id null `
 -ProgressPct null `
 -Scope null `
 -TargetValue null `
 -TargetYear null
```

- Convert the resource to JSON
```powershell
$TargetProgress | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

