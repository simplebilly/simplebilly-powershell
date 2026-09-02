# IncomeStatement
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExpenseItems** | [**PnLItem[]**](PnLItem.md) |  | 
**NetIncome** | **String** |  | 
**RevenueItems** | [**PnLItem[]**](PnLItem.md) |  | 
**TotalExpenses** | **String** |  | 
**TotalRevenue** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$IncomeStatement = Initialize-PSOpenAPIToolsIncomeStatement  -ExpenseItems null `
 -NetIncome null `
 -RevenueItems null `
 -TotalExpenses null `
 -TotalRevenue null
```

- Convert the resource to JSON
```powershell
$IncomeStatement | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

