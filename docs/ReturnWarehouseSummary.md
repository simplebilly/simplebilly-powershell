# ReturnWarehouseSummary
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ItemsRestocked** | **Int64** |  | 
**ItemsScrapped** | **Int64** |  | 
**Returns** | **Int64** |  | 
**WarehouseId** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ReturnWarehouseSummary = Initialize-PSOpenAPIToolsReturnWarehouseSummary  -ItemsRestocked null `
 -ItemsScrapped null `
 -Returns null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$ReturnWarehouseSummary | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

