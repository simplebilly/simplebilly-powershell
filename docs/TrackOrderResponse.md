# TrackOrderResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**OrderNumber** | **String** |  | 
**OrderStatus** | **String** |  | 
**Shipments** | [**TrackedShipment[]**](TrackedShipment.md) |  | 

## Examples

- Prepare the resource
```powershell
$TrackOrderResponse = Initialize-PSOpenAPIToolsTrackOrderResponse  -OrderNumber null `
 -OrderStatus null `
 -Shipments null
```

- Convert the resource to JSON
```powershell
$TrackOrderResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

