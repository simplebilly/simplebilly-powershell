# ProductionOrderCosting
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CostPerUnit** | **String** | material_cost_total ÷ quantity. | 
**CostSource** | **String** | &quot;&quot;actual&quot;&quot; when costed from stock-movement consumption, else &quot;&quot;planned&quot;&quot;. | 
**Lines** | [**CostingLine[]**](CostingLine.md) |  | 
**MarginPerUnit** | **String** | sale_price − cost_per_unit. | [optional] 
**MarginPercent** | **String** | margin_per_unit ÷ cost_per_unit as a percentage. | [optional] 
**MaterialCostTotal** | **String** | Total material cost for the whole order. | 
**OrderNumber** | **String** |  | 
**ProductionOrderId** | **String** |  | 
**Quantity** | **Int64** |  | 
**SalePrice** | **String** | Finished product&#39;s sale price per unit (used to compute margin). | [optional] 
**Status** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ProductionOrderCosting = Initialize-PSOpenAPIToolsProductionOrderCosting  -CostPerUnit null `
 -CostSource null `
 -Lines null `
 -MarginPerUnit null `
 -MarginPercent null `
 -MaterialCostTotal null `
 -OrderNumber null `
 -ProductionOrderId null `
 -Quantity null `
 -SalePrice null `
 -Status null
```

- Convert the resource to JSON
```powershell
$ProductionOrderCosting | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

