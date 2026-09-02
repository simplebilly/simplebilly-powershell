# ReplenishmentResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GeneratedAt** | **System.DateTime** |  | 
**Lines** | [**ReplenishmentSuggestionLine[]**](ReplenishmentSuggestionLine.md) |  | 
**TargetWarehouseId** | **String** |  | 
**TotalSuggestedQuantity** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$ReplenishmentResponse = Initialize-PSOpenAPIToolsReplenishmentResponse  -GeneratedAt null `
 -Lines null `
 -TargetWarehouseId null `
 -TotalSuggestedQuantity null
```

- Convert the resource to JSON
```powershell
$ReplenishmentResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

