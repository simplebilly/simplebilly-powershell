# PublicReturnRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **String** |  | 
**Items** | [**PublicReturnItem[]**](PublicReturnItem.md) |  | 
**Notes** | **String** |  | [optional] 
**OrderNumber** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PublicReturnRequest = Initialize-PSOpenAPIToolsPublicReturnRequest  -Email null `
 -Items null `
 -Notes null `
 -OrderNumber null
```

- Convert the resource to JSON
```powershell
$PublicReturnRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

