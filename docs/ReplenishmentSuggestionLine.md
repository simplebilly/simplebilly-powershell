# ReplenishmentSuggestionLine
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CurrentStock** | **Int64** | Current stock in the target warehouse. | 
**MaxStock** | **Int64** |  | [optional] 
**MinStock** | **Int64** |  | [optional] 
**ProductId** | **String** |  | 
**ProductName** | **String** |  | 
**Sku** | **String** |  | 
**SourceAvailable** | **Int64** | Surplus available in the source warehouse (above its target). | 
**SourceWarehouseId** | **String** |  | 
**SuggestedQuantity** | **Int64** |  | 
**TargetWarehouseId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ReplenishmentSuggestionLine = Initialize-PSOpenAPIToolsReplenishmentSuggestionLine  -CurrentStock null `
 -MaxStock null `
 -MinStock null `
 -ProductId null `
 -ProductName null `
 -Sku null `
 -SourceAvailable null `
 -SourceWarehouseId null `
 -SuggestedQuantity null `
 -TargetWarehouseId null
```

- Convert the resource to JSON
```powershell
$ReplenishmentSuggestionLine | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

