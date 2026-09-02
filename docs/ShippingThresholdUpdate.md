# ShippingThresholdUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsActive** | **Boolean** |  | [optional] 
**MaxSellable** | **Int64** | Optional ceiling for the deliverable quantity. | [optional] 
**Name** | **String** |  | [optional] 
**Notes** | **String** |  | [optional] 
**ProductId** | **String** | None &#x3D; applies to all products. References the product entity. | [optional] 
**ReserveStock** | **Int64** | Buffer of stock that must not be sold. | [optional] 
**WarehouseId** | **String** | None &#x3D; applies to all warehouses. References the warehouse entity. | [optional] 

## Examples

- Prepare the resource
```powershell
$ShippingThresholdUpdate = Initialize-PSOpenAPIToolsShippingThresholdUpdate  -IsActive null `
 -MaxSellable null `
 -Name null `
 -Notes null `
 -ProductId null `
 -ReserveStock null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$ShippingThresholdUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

