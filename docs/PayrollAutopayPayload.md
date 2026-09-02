# PayrollAutopayPayload
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DebtorBic** | **String** |  | [optional] 
**DebtorIban** | **String** |  | [optional] 
**DebtorName** | **String** |  | [optional] 
**ExecutionDate** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PayrollAutopayPayload = Initialize-PSOpenAPIToolsPayrollAutopayPayload  -DebtorBic null `
 -DebtorIban null `
 -DebtorName null `
 -ExecutionDate null
```

- Convert the resource to JSON
```powershell
$PayrollAutopayPayload | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

