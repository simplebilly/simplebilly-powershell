# LiquidityPosition
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountsPayable** | **Double** |  | 
**AccountsReceivable** | **Double** |  | 
**CashAndEquivalents** | **Double** |  | 
**CurrentRatio** | **Double** |  | 
**QuickRatio** | **Double** |  | 
**WorkingCapital** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$LiquidityPosition = Initialize-PSOpenAPIToolsLiquidityPosition  -AccountsPayable null `
 -AccountsReceivable null `
 -CashAndEquivalents null `
 -CurrentRatio null `
 -QuickRatio null `
 -WorkingCapital null
```

- Convert the resource to JSON
```powershell
$LiquidityPosition | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

