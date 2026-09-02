# YearlyPayrollSummary
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AvgEmployeeCount** | **Int32** |  | 
**Months** | [**PayrollSummaryItem[]**](PayrollSummaryItem.md) |  | 
**Year** | **Int32** |  | 
**YearlyEmployerCost** | **String** |  | 
**YearlyGross** | **String** |  | 
**YearlyNet** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$YearlyPayrollSummary = Initialize-PSOpenAPIToolsYearlyPayrollSummary  -AvgEmployeeCount null `
 -Months null `
 -Year null `
 -YearlyEmployerCost null `
 -YearlyGross null `
 -YearlyNet null
```

- Convert the resource to JSON
```powershell
$YearlyPayrollSummary | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

