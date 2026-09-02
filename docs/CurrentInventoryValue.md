# CurrentInventoryValue
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**History** | [**InventoryValuePoint[]**](InventoryValuePoint.md) |  | 
**ProductCount** | **Int64** |  | 
**TotalPurchaseValue** | **String** |  | 
**TotalSalesValue** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$CurrentInventoryValue = Initialize-PSOpenAPIToolsCurrentInventoryValue  -History null `
 -ProductCount null `
 -TotalPurchaseValue null `
 -TotalSalesValue null
```

- Convert the resource to JSON
```powershell
$CurrentInventoryValue | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

