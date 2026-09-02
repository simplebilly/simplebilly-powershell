# PublicReturnItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Name** | **String** |  | [optional] 
**ProductId** | **String** |  | 
**Quantity** | **Int64** |  | 
**Reason** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PublicReturnItem = Initialize-PSOpenAPIToolsPublicReturnItem  -Name null `
 -ProductId null `
 -Quantity null `
 -Reason null
```

- Convert the resource to JSON
```powershell
$PublicReturnItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

