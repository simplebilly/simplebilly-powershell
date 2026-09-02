# CashflowReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ClosingBalance** | **Double** |  | 
**FinancingCashflow** | **Double** |  | 
**InvestingCashflow** | **Double** |  | 
**NetCashflow** | **Double** |  | 
**OpeningBalance** | **Double** |  | 
**OperatingCashflow** | **Double** |  | 
**Period** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$CashflowReport = Initialize-PSOpenAPIToolsCashflowReport  -ClosingBalance null `
 -FinancingCashflow null `
 -InvestingCashflow null `
 -NetCashflow null `
 -OpeningBalance null `
 -OperatingCashflow null `
 -Period null
```

- Convert the resource to JSON
```powershell
$CashflowReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

