# InventoryValuePoint
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProductCount** | **Int64** |  | 
**RecordedAt** | **System.DateTime** |  | 
**TotalPurchaseValue** | **String** |  | 
**TotalSalesValue** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$InventoryValuePoint = Initialize-PSOpenAPIToolsInventoryValuePoint  -ProductCount null `
 -RecordedAt null `
 -TotalPurchaseValue null `
 -TotalSalesValue null
```

- Convert the resource to JSON
```powershell
$InventoryValuePoint | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

