# Employee
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | **String** |  | [optional] 
**BackupEmployeeId** | **String** | References another employee who covers when this employee is absent. | [optional] 
**Bic** | **String** |  | [optional] 
**City** | **String** |  | [optional] 
**Country** | [**CountryCode**](CountryCode.md) |  | [optional] 
**CreatedAt** | **System.DateTime** |  | [optional] 
**DateOfBirth** | **System.DateTime** |  | [optional] 
**DeletedAt** | **System.DateTime** |  | [optional] 
**DepartmentId** | **String** | References the department entity. | [optional] 
**Email** | **String** |  | [optional] 
**FirstName** | **String** |  | [optional] 
**Gender** | [**Gender**](Gender.md) | Gender for pay-transparency reporting: &quot;&quot;male&quot;&quot;, &quot;&quot;female&quot;&quot; or &quot;&quot;diverse&quot;&quot;. | [optional] 
**HireDate** | **System.DateTime** |  | [optional] 
**HourlyCost** | **String** | Hourly cost rate in EUR for labor-cost reporting; when unset the rate is derived from &#x60;monthly_salary / (weekly_hours * 4.33)&#x60;. | [optional] 
**Iban** | **String** |  | [optional] 
**Id** | **String** |  | [optional] 
**JobTitle** | **String** |  | [optional] 
**LastLogin** | **System.DateTime** |  | [optional] 
**LastName** | **String** |  | [optional] 
**LastUpdated** | **System.DateTime** |  | [optional] 
**MonthlySalary** | **String** | Gross monthly salary in EUR for pay-transparency reporting. | [optional] 
**Phone** | **String** |  | [optional] 
**State** | **String** |  | [optional] 
**Status** | [**EmployeeStatus**](EmployeeStatus.md) |  | [optional] 
**TenantId** | **String** |  | [optional] 
**UpdatedAt** | **System.DateTime** |  | [optional] 
**UserId** | **String** | References the user entity. | [optional] 
**WeeklyHours** | **String** | Contractual weekly working hours for pay-transparency normalization. | [optional] 
**Zip** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Employee = Initialize-PSOpenAPIToolsEmployee  -Address null `
 -BackupEmployeeId null `
 -Bic null `
 -City null `
 -Country null `
 -CreatedAt null `
 -DateOfBirth null `
 -DeletedAt null `
 -DepartmentId null `
 -Email null `
 -FirstName null `
 -Gender null `
 -HireDate null `
 -HourlyCost null `
 -Iban null `
 -Id null `
 -JobTitle null `
 -LastLogin null `
 -LastName null `
 -LastUpdated null `
 -MonthlySalary null `
 -Phone null `
 -State null `
 -Status null `
 -TenantId null `
 -UpdatedAt null `
 -UserId null `
 -WeeklyHours null `
 -Zip null
```

- Convert the resource to JSON
```powershell
$Employee | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

