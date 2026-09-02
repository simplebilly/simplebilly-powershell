# TrackingEvent
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **String** |  | 
**Description** | **String** |  | 
**Location** | **String** |  | 
**Status** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$TrackingEvent = Initialize-PSOpenAPIToolsTrackingEvent  -Date null `
 -Description null `
 -Location null `
 -Status null
```

- Convert the resource to JSON
```powershell
$TrackingEvent | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

