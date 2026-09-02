# EmissionsReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ByCategory** | [**CategoryTotal[]**](CategoryTotal.md) |  | 
**ByScope** | [**ScopeTotal[]**](ScopeTotal.md) |  | 
**ByYear** | [**YearTotal[]**](YearTotal.md) |  | 
**DataQuality** | [**DataQuality**](DataQuality.md) |  | 
**IntensityPerEmployee** | **Double** |  | [optional] 
**IntensityPerRevenueMio** | **Double** | tCO2e per million EUR net revenue. | [optional] 
**NetRevenue** | **Double** | Sum of paid/sent/partially-paid invoices (EUR net) in the year. | [optional] 
**SpendBasedEstimateTco2e** | **Double** | Spend-based estimate from bookkeeping payments (EXIOBASE factor). | [optional] 
**Targets** | [**TargetProgress[]**](TargetProgress.md) |  | 
**TotalTco2e** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$EmissionsReport = Initialize-PSOpenAPIToolsEmissionsReport  -ByCategory null `
 -ByScope null `
 -ByYear null `
 -DataQuality null `
 -IntensityPerEmployee null `
 -IntensityPerRevenueMio null `
 -NetRevenue null `
 -SpendBasedEstimateTco2e null `
 -Targets null `
 -TotalTco2e null
```

- Convert the resource to JSON
```powershell
$EmissionsReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

