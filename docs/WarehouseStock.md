# WarehouseStock
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BatchNumber** | **String** | Batch/lot number (Chargennummer) — &#x60;None&#x60; for non-batched goods. | [optional] 
**BinLocation** | **String** |  | [optional] 
**ExpiryDate** | **System.DateTime** | Expiry date for batch-tracked goods. | [optional] 
**ProductId** | **String** |  | 
**Quantity** | **Int64** |  | 
**SerialNumbers** | [**AnyType**](.md) | JSON array of serial numbers (Seriennummern) in this stock row. | [optional] 
**WarehouseId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$WarehouseStock = Initialize-PSOpenAPIToolsWarehouseStock  -BatchNumber null `
 -BinLocation null `
 -ExpiryDate null `
 -ProductId null `
 -Quantity null `
 -SerialNumbers null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$WarehouseStock | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

