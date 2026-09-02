# TrackOrderRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **String** |  | 
**OrderNumber** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$TrackOrderRequest = Initialize-PSOpenAPIToolsTrackOrderRequest  -Email null `
 -OrderNumber null
```

- Convert the resource to JSON
```powershell
$TrackOrderRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

