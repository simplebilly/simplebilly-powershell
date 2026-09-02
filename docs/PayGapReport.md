# PayGapReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ByJobTitle** | [**JobTitleGap[]**](JobTitleGap.md) |  | 
**DiverseCount** | **Int32** |  | 
**EmployeeCount** | **Int32** |  | 
**FemaleCount** | **Int32** |  | 
**MaleCount** | **Int32** |  | 
**MeanGapPct** | **Double** |  | 
**MedianGapPct** | **Double** |  | 
**Quartiles** | [**QuartileBand[]**](QuartileBand.md) |  | 

## Examples

- Prepare the resource
```powershell
$PayGapReport = Initialize-PSOpenAPIToolsPayGapReport  -ByJobTitle null `
 -DiverseCount null `
 -EmployeeCount null `
 -FemaleCount null `
 -MaleCount null `
 -MeanGapPct null `
 -MedianGapPct null `
 -Quartiles null
```

- Convert the resource to JSON
```powershell
$PayGapReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

