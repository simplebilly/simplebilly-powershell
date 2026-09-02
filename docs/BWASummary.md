# BWASummary
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GrossProfit** | **String** |  | 
**NetProfit** | **String** |  | 
**OpenInvoicesCount** | **Int64** |  | 
**OpenInvoicesTotal** | **String** |  | 
**OverdueInvoicesCount** | **Int64** |  | 
**OverdueInvoicesTotal** | **String** |  | 
**ProfitMargin** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$BWASummary = Initialize-PSOpenAPIToolsBWASummary  -GrossProfit null `
 -NetProfit null `
 -OpenInvoicesCount null `
 -OpenInvoicesTotal null `
 -OverdueInvoicesCount null `
 -OverdueInvoicesTotal null `
 -ProfitMargin null
```

- Convert the resource to JSON
```powershell
$BWASummary | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

