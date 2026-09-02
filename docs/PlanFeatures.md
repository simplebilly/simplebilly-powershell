# PlanFeatures
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Connectors** | **Boolean** |  | 
**Erp** | **Boolean** |  | 
**FancyReports** | **Boolean** |  | 
**TaxAutomations** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$PlanFeatures = Initialize-PSOpenAPIToolsPlanFeatures  -Connectors null `
 -Erp null `
 -FancyReports null `
 -TaxAutomations null
```

- Convert the resource to JSON
```powershell
$PlanFeatures | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

