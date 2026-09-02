# StockAdjustment
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BatchNumber** | **String** |  | [optional] 
**BinLocation** | **String** |  | [optional] 
**ExpiryDate** | **System.DateTime** |  | [optional] 
**ProductId** | **String** |  | [optional] 
**Quantity** | **Int64** |  | 
**SerialNumbers** | **String[]** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$StockAdjustment = Initialize-PSOpenAPIToolsStockAdjustment  -BatchNumber null `
 -BinLocation null `
 -ExpiryDate null `
 -ProductId null `
 -Quantity null `
 -SerialNumbers null
```

- Convert the resource to JSON
```powershell
$StockAdjustment | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

