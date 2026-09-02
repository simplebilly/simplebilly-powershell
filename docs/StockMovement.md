# StockMovement
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Delta** | **Int64** | Signed movement: positive &#x3D; into stock, negative &#x3D; out of stock. | 
**MovementType** | [**MovementType**](MovementType.md) | One of the &#x60;MOVEMENT_*&#x60; constants. | 
**ProductId** | **String** | References the product entity. | 
**Quantity** | **Int64** | Absolute quantity moved (always &gt;&#x3D; 0). | 
**Reason** | **String** |  | [optional] 
**ReferenceId** | **String** | Primary-key of the referencing entity. | [optional] 
**ReferenceType** | [**ReferenceType**](ReferenceType.md) | Entity that caused the movement, e.g. &#x60;goods_receipt&#x60;, &#x60;stock_transfer&#x60;. | [optional] 
**WarehouseId** | **String** | References the warehouse entity. | 

## Examples

- Prepare the resource
```powershell
$StockMovement = Initialize-PSOpenAPIToolsStockMovement  -Delta null `
 -MovementType null `
 -ProductId null `
 -Quantity null `
 -Reason null `
 -ReferenceId null `
 -ReferenceType null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$StockMovement | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

