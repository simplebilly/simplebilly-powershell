# CostingLine
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**LineCost** | **String** | total_quantity × unit_purchase_price (0 when price unknown). | 
**Name** | **String** |  | 
**ProductId** | **String** |  | 
**QuantityPerUnit** | **Int64** | Component quantity required per finished unit. | 
**Sku** | **String** |  | 
**TotalQuantity** | **Int64** | Total component quantity consumed by this order. | 
**UnitPurchasePrice** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$CostingLine = Initialize-PSOpenAPIToolsCostingLine  -LineCost null `
 -Name null `
 -ProductId null `
 -QuantityPerUnit null `
 -Sku null `
 -TotalQuantity null `
 -UnitPurchasePrice null
```

- Convert the resource to JSON
```powershell
$CostingLine | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

