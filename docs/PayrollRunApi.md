# PayrollRunApi
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ApprovedAt** | **System.DateTime** |  | [optional] 
**ApprovedBy** | **String** |  | [optional] 
**CreatedAt** | **System.DateTime** |  | 
**Entries** | [**PayrollEntryApi[]**](PayrollEntryApi.md) |  | 
**Month** | **Int32** |  | 
**PaymentDate** | **System.DateTime** |  | [optional] 
**PeriodLabel** | **String** |  | 
**RunId** | **String** |  | 
**Status** | [**PayrollRunStatus**](PayrollRunStatus.md) |  | 
**TenantId** | **String** |  | 
**TotalEmployeeCount** | **Int32** |  | 
**TotalEmployerCost** | **String** |  | 
**TotalGross** | **String** |  | 
**TotalNet** | **String** |  | 
**TotalSocialSecurity** | **String** |  | 
**TotalTaxes** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 
**Year** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$PayrollRunApi = Initialize-PSOpenAPIToolsPayrollRunApi  -ApprovedAt null `
 -ApprovedBy null `
 -CreatedAt null `
 -Entries null `
 -Month null `
 -PaymentDate null `
 -PeriodLabel null `
 -RunId null `
 -Status null `
 -TenantId null `
 -TotalEmployeeCount null `
 -TotalEmployerCost null `
 -TotalGross null `
 -TotalNet null `
 -TotalSocialSecurity null `
 -TotalTaxes null `
 -UpdatedAt null `
 -Year null
```

- Convert the resource to JSON
```powershell
$PayrollRunApi | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

