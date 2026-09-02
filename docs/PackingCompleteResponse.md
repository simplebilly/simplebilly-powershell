# PackingCompleteResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **String** |  | 
**NewState** | **String** |  | 
**OrderNumber** | **String** |  | 
**Success** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$PackingCompleteResponse = Initialize-PSOpenAPIToolsPackingCompleteResponse  -Message null `
 -NewState null `
 -OrderNumber null `
 -Success null
```

- Convert the resource to JSON
```powershell
$PackingCompleteResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

