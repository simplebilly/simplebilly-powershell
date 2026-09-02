# PayrollCreatePayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EmployeeIds** | **String[]** |  | 
**ExtraPayments** | [**ExtraPayment[]**](ExtraPayment.md) |  | [optional] 
**Month** | **Int32** |  | 
**Year** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$PayrollCreatePayload = Initialize-PSOpenAPIToolsPayrollCreatePayload  -EmployeeIds null `
 -ExtraPayments null `
 -Month null `
 -Year null
```

- Convert the resource to JSON
```powershell
$PayrollCreatePayload | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

