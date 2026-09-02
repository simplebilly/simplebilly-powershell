# Plan
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Features** | [**PlanFeatures**](PlanFeatures.md) |  | 
**Id** | **String** |  | 
**Limits** | [**PlanLimits**](PlanLimits.md) |  | 
**Name** | **String** |  | 
**PriceEur** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$Plan = Initialize-PSOpenAPIToolsPlan  -Features null `
 -Id null `
 -Limits null `
 -Name null `
 -PriceEur null
```

- Convert the resource to JSON
```powershell
$Plan | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

