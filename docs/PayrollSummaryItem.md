# PayrollSummaryItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EmployeeCount** | **Int32** |  | 
**Month** | **String** |  | 
**Status** | [**PayrollRunStatus**](PayrollRunStatus.md) |  | 
**TotalEmployerCost** | **String** |  | 
**TotalGross** | **String** |  | 
**TotalNet** | **String** |  | 
**Year** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$PayrollSummaryItem = Initialize-PSOpenAPIToolsPayrollSummaryItem  -EmployeeCount null `
 -Month null `
 -Status null `
 -TotalEmployerCost null `
 -TotalGross null `
 -TotalNet null `
 -Year null
```

- Convert the resource to JSON
```powershell
$PayrollSummaryItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

