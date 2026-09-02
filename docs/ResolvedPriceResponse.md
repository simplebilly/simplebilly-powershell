# ResolvedPriceResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsListPrice** | **Boolean** | True when no tier matched and the product list price was used. | 
**PriceTierId** | **String** | Applied tier, if any matched. | [optional] 
**ProductId** | **String** |  | 
**Quantity** | **Int64** |  | 
**UnitPrice** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ResolvedPriceResponse = Initialize-PSOpenAPIToolsResolvedPriceResponse  -IsListPrice null `
 -PriceTierId null `
 -ProductId null `
 -Quantity null `
 -UnitPrice null
```

- Convert the resource to JSON
```powershell
$ResolvedPriceResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

