# QuotaOverrideFeatures
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Erp** | **Boolean** |  | [optional] 
**FancyReports** | **Boolean** |  | [optional] 
**TaxAutomations** | **Boolean** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$QuotaOverrideFeatures = Initialize-PSOpenAPIToolsQuotaOverrideFeatures  -Erp null `
 -FancyReports null `
 -TaxAutomations null
```

- Convert the resource to JSON
```powershell
$QuotaOverrideFeatures | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

