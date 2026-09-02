# TrackingInfo
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Carrier** | **String** |  | 
**EstimatedDelivery** | **String** |  | [optional] 
**Events** | [**TrackingEvent[]**](TrackingEvent.md) |  | 
**RawResponse** | [**AnyType**](.md) |  | [optional] 
**Status** | **String** |  | 
**TrackingNumber** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$TrackingInfo = Initialize-PSOpenAPIToolsTrackingInfo  -Carrier null `
 -EstimatedDelivery null `
 -Events null `
 -RawResponse null `
 -Status null `
 -TrackingNumber null
```

- Convert the resource to JSON
```powershell
$TrackingInfo | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

