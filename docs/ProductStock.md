# ProductStock
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **String** |  | 
**ProductId** | **String** |  | 
**Sku** | **String** |  | 
**StockQuantity** | **Int64** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ProductStock = Initialize-PSOpenAPIToolsProductStock  -Name null `
 -ProductId null `
 -Sku null `
 -StockQuantity null
```

- Convert the resource to JSON
```powershell
$ProductStock | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

