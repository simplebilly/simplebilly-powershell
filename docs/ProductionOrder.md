# ProductionOrder
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BomId** | **String** | References the BOM entity. | [optional] 
**Components** | [**AnyType**](.md) | JSON snapshot of the BOM components at creation time. | [optional] 
**EndDate** | **System.DateTime** |  | [optional] 
**Notes** | **String** |  | [optional] 
**OrderNumber** | **String** |  | 
**ProductId** | **String** | The finished product to manufacture. References the product entity. | 
**Quantity** | **Int64** | Quantity of finished product to produce. | 
**SourceWarehouseId** | **String** | Warehouse components are consumed from. References the warehouse entity. | [optional] 
**StartDate** | **System.DateTime** |  | [optional] 
**Status** | [**ProductionOrderStatus**](ProductionOrderStatus.md) | One of: planned | in_production | completed | cancelled | [optional] 
**TargetWarehouseId** | **String** | Warehouse the finished product is added to. References the warehouse entity. | [optional] 

## Examples

- Prepare the resource
```powershell
$ProductionOrder = Initialize-PSOpenAPIToolsProductionOrder  -BomId null `
 -Components null `
 -EndDate null `
 -Notes null `
 -OrderNumber null `
 -ProductId null `
 -Quantity null `
 -SourceWarehouseId null `
 -StartDate null `
 -Status null `
 -TargetWarehouseId null
```

- Convert the resource to JSON
```powershell
$ProductionOrder | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

