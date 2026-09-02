# BWAExpenses
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExpenseBreakdown** | [**ExpenseItem[]**](ExpenseItem.md) |  | 
**TotalExpenses** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$BWAExpenses = Initialize-PSOpenAPIToolsBWAExpenses  -ExpenseBreakdown null `
 -TotalExpenses null
```

- Convert the resource to JSON
```powershell
$BWAExpenses | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

