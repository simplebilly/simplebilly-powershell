# BalanceSheet
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Assets** | [**BalanceItem[]**](BalanceItem.md) |  | 
**Balanced** | **Boolean** |  | 
**EquityLiabilities** | [**BalanceItem[]**](BalanceItem.md) |  | 
**TotalAssets** | **String** |  | 
**TotalEquityLiabilities** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$BalanceSheet = Initialize-PSOpenAPIToolsBalanceSheet  -Assets null `
 -Balanced null `
 -EquityLiabilities null `
 -TotalAssets null `
 -TotalEquityLiabilities null
```

- Convert the resource to JSON
```powershell
$BalanceSheet | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

