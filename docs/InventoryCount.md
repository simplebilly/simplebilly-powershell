# InventoryCount
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CountDate** | **System.DateTime** |  | 
**CountNumber** | **String** |  | 
**LineItems** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, sku, expected_quantity, counted_quantity, bin_location?, batch_number?, variance}&#x60;. | 
**Notes** | **String** |  | [optional] 
**Status** | [**InventoryCountStatus**](InventoryCountStatus.md) | One of: draft | counting | reviewed | posted | 
**WarehouseId** | **String** | References the warehouse entity. | 

## Examples

- Prepare the resource
```powershell
$InventoryCount = Initialize-PSOpenAPIToolsInventoryCount  -CountDate null `
 -CountNumber null `
 -LineItems null `
 -Notes null `
 -Status null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$InventoryCount | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

