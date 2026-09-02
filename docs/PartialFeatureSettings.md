# PartialFeatureSettings
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Onlineshop** | **Boolean** |  | [optional] 
**ReportBilanz** | **Boolean** |  | [optional] 
**ReportBwa** | **Boolean** |  | [optional] 
**ReportEuer** | **Boolean** |  | [optional] 
**ReportGewerbesteuer** | **Boolean** |  | [optional] 
**ReportGuv** | **Boolean** |  | [optional] 
**ReportKst** | **Boolean** |  | [optional] 
**ReportUstva** | **Boolean** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PartialFeatureSettings = Initialize-PSOpenAPIToolsPartialFeatureSettings  -Onlineshop null `
 -ReportBilanz null `
 -ReportBwa null `
 -ReportEuer null `
 -ReportGewerbesteuer null `
 -ReportGuv null `
 -ReportKst null `
 -ReportUstva null
```

- Convert the resource to JSON
```powershell
$PartialFeatureSettings | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

