# EBilanzReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountOverview** | [**AccountOverview[]**](AccountOverview.md) |  | 
**BalanceSheet** | [**BalanceSheet**](BalanceSheet.md) |  | 
**GeneratedAt** | **String** |  | 
**IncomeStatement** | [**IncomeStatement**](IncomeStatement.md) |  | 
**Period** | **String** |  | 
**VatSummary** | [**VatSummary**](VatSummary.md) |  | 

## Examples

- Prepare the resource
```powershell
$EBilanzReport = Initialize-PSOpenAPIToolsEBilanzReport  -AccountOverview null `
 -BalanceSheet null `
 -GeneratedAt null `
 -IncomeStatement null `
 -Period null `
 -VatSummary null
```

- Convert the resource to JSON
```powershell
$EBilanzReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

