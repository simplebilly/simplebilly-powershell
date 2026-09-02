# ReorderProposalResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GeneratedAt** | **System.DateTime** |  | 
**Lines** | [**ReorderProposalLine[]**](ReorderProposalLine.md) |  | 
**TotalSuggestedQuantity** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$ReorderProposalResponse = Initialize-PSOpenAPIToolsReorderProposalResponse  -GeneratedAt null `
 -Lines null `
 -TotalSuggestedQuantity null
```

- Convert the resource to JSON
```powershell
$ReorderProposalResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

