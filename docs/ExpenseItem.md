# ExpenseItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **String** |  | 
**Category** | **String** |  | 
**Percentage** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$ExpenseItem = Initialize-PSOpenAPIToolsExpenseItem  -Amount null `
 -Category null `
 -Percentage null
```

- Convert the resource to JSON
```powershell
$ExpenseItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

