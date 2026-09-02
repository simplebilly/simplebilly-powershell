# ShipmentStatusUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DeliveredAt** | **String** |  | [optional] 
**SignedBy** | **String** |  | [optional] 
**Status** | **String** |  | 
**TrackingNumber** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ShipmentStatusUpdate = Initialize-PSOpenAPIToolsShipmentStatusUpdate  -DeliveredAt null `
 -SignedBy null `
 -Status null `
 -TrackingNumber null
```

- Convert the resource to JSON
```powershell
$ShipmentStatusUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

