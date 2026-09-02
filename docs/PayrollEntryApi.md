# PayrollEntryApi
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AvEmployee** | **String** |  | 
**AvEmployer** | **String** |  | 
**ChurchTaxAmount** | **String** |  | 
**Employee** | [**Employee**](Employee.md) |  | [optional] 
**EmployeeId** | **String** |  | 
**EntryId** | **String** |  | 
**ExtraPaymentReason** | **String** |  | [optional] 
**ExtraPayments** | **String** |  | 
**GrossSalary** | **String** |  | 
**KvEmployee** | **String** |  | 
**KvEmployer** | **String** |  | 
**Lohnsteuer** | **String** |  | 
**NetSalary** | **String** |  | 
**Notes** | **String** |  | [optional] 
**PvEmployee** | **String** |  | 
**PvEmployer** | **String** |  | 
**RunId** | **String** |  | 
**RvEmployee** | **String** |  | 
**RvEmployer** | **String** |  | 
**SickDays** | **Int32** |  | 
**Soli** | **String** |  | 
**Status** | [**PayrollRunStatus**](PayrollRunStatus.md) |  | 
**TotalDeductions** | **String** |  | 
**TotalEmployerCost** | **String** |  | 
**VacationDaysUsed** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$PayrollEntryApi = Initialize-PSOpenAPIToolsPayrollEntryApi  -AvEmployee null `
 -AvEmployer null `
 -ChurchTaxAmount null `
 -Employee null `
 -EmployeeId null `
 -EntryId null `
 -ExtraPaymentReason null `
 -ExtraPayments null `
 -GrossSalary null `
 -KvEmployee null `
 -KvEmployer null `
 -Lohnsteuer null `
 -NetSalary null `
 -Notes null `
 -PvEmployee null `
 -PvEmployer null `
 -RunId null `
 -RvEmployee null `
 -RvEmployer null `
 -SickDays null `
 -Soli null `
 -Status null `
 -TotalDeductions null `
 -TotalEmployerCost null `
 -VacationDaysUsed null
```

- Convert the resource to JSON
```powershell
$PayrollEntryApi | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

