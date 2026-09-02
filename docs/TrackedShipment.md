# TrackedShipment
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Carrier** | **String** |  | 
**Events** | [**TrackingEvent[]**](TrackingEvent.md) |  | 
**LabelUrl** | **String** |  | [optional] 
**Status** | **String** |  | 
**TrackingNumber** | **String** |  | [optional] 
**TrackingUrl** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$TrackedShipment = Initialize-PSOpenAPIToolsTrackedShipment  -Carrier null `
 -Events null `
 -LabelUrl null `
 -Status null `
 -TrackingNumber null `
 -TrackingUrl null
```

- Convert the resource to JSON
```powershell
$TrackedShipment | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

