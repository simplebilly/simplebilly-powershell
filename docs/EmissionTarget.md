# EmissionTarget
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BaseValue** | **String** |  | 
**BaseYear** | **Int32** | tCO2e in the base year (actuals). | 
**Description** | **String** | Transition-plan narrative (ESRS E1-1 light), may be empty. | 
**Scope** | [**EmissionTargetScope**](EmissionTargetScope.md) | &quot;&quot;total&quot;&quot; | &quot;&quot;1&quot;&quot; | &quot;&quot;2&quot;&quot; | &quot;&quot;3&quot;&quot;. | 
**TargetValue** | **String** |  | 
**TargetYear** | **Int32** | tCO2e target for the target year. | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$EmissionTarget = Initialize-PSOpenAPIToolsEmissionTarget  -BaseValue null `
 -BaseYear null `
 -Description null `
 -Scope null `
 -TargetValue null `
 -TargetYear null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$EmissionTarget | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

