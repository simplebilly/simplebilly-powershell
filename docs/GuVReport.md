# GuVReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Expenses** | [**GuVItem[]**](GuVItem.md) |  | 
**GeneratedAt** | **String** |  | 
**NetIncome** | **String** |  | 
**Period** | **String** |  | 
**Revenue** | [**GuVItem[]**](GuVItem.md) |  | 
**TotalExpenses** | **String** |  | 
**TotalRevenue** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GuVReport = Initialize-PSOpenAPIToolsGuVReport  -Expenses null `
 -GeneratedAt null `
 -NetIncome null `
 -Period null `
 -Revenue null `
 -TotalExpenses null `
 -TotalRevenue null
```

- Convert the resource to JSON
```powershell
$GuVReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

