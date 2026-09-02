# GenerateCountRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Notes** | **String** |  | [optional] 
**ProductIds** | **String[]** |  | [optional] 
**WarehouseId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$GenerateCountRequest = Initialize-PSOpenAPIToolsGenerateCountRequest  -Notes null `
 -ProductIds null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$GenerateCountRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

