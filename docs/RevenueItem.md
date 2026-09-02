# RevenueItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Amount** | **String** |  | 
**Category** | **String** |  | 
**Percentage** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$RevenueItem = Initialize-PSOpenAPIToolsRevenueItem  -Amount null `
 -Category null `
 -Percentage null
```

- Convert the resource to JSON
```powershell
$RevenueItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

