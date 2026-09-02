# PackingVideoResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Message** | **String** |  | 
**RecordingUrl** | **String** |  | [optional] 
**Success** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$PackingVideoResponse = Initialize-PSOpenAPIToolsPackingVideoResponse  -Message null `
 -RecordingUrl null `
 -Success null
```

- Convert the resource to JSON
```powershell
$PackingVideoResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

