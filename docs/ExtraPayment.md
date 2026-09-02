# ExtraPayment
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **String** |  | 
**EmployeeId** | **String** |  | 
**Reason** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ExtraPayment = Initialize-PSOpenAPIToolsExtraPayment  -Amount null `
 -EmployeeId null `
 -Reason null
```

- Convert the resource to JSON
```powershell
$ExtraPayment | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

