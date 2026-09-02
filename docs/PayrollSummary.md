# PayrollSummary
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FirstName** | **String** |  | 
**HourlyGross** | **String** |  | [optional] 
**Id** | **String** |  | 
**JobTitle** | **String** |  | 
**LastName** | **String** |  | 
**MonthlySalary** | **String** |  | [optional] 
**Months** | [**PayrollMonth[]**](PayrollMonth.md) |  | 
**WeeklyHours** | **String** |  | [optional] 
**Year** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$PayrollSummary = Initialize-PSOpenAPIToolsPayrollSummary  -FirstName null `
 -HourlyGross null `
 -Id null `
 -JobTitle null `
 -LastName null `
 -MonthlySalary null `
 -Months null `
 -WeeklyHours null `
 -Year null
```

- Convert the resource to JSON
```powershell
$PayrollSummary | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

