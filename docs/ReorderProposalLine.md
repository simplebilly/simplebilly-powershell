# ReorderProposalLine
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CurrentStock** | **Int64** |  | 
**MaxStock** | **Int64** |  | [optional] 
**MinStock** | **Int64** |  | [optional] 
**ProductId** | **String** |  | 
**ProductName** | **String** |  | 
**ReorderQuantity** | **Int64** |  | [optional] 
**Sku** | **String** |  | 
**SuggestedQuantity** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$ReorderProposalLine = Initialize-PSOpenAPIToolsReorderProposalLine  -CurrentStock null `
 -MaxStock null `
 -MinStock null `
 -ProductId null `
 -ProductName null `
 -ReorderQuantity null `
 -Sku null `
 -SuggestedQuantity null
```

- Convert the resource to JSON
```powershell
$ReorderProposalLine | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

