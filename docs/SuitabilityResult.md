# SuitabilityResult
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Methods** | [**MethodSuitability[]**](MethodSuitability.md) |  | 
**RecommendedBox** | [**BoxFit**](BoxFit.md) |  | [optional] 
**RequiresInsurance** | **Boolean** |  | 
**TotalValue** | **String** |  | 
**TotalWeightKg** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$SuitabilityResult = Initialize-PSOpenAPIToolsSuitabilityResult  -Methods null `
 -RecommendedBox null `
 -RequiresInsurance null `
 -TotalValue null `
 -TotalWeightKg null
```

- Convert the resource to JSON
```powershell
$SuitabilityResult | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

