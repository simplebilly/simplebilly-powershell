# PublicDeliveryAppointmentStatusResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AppointmentId** | **String** |  | 
**RequestedDate** | **System.DateTime** |  | 
**Status** | **String** |  | 
**TimeSlot** | **String** |  | [optional] 
**WarehouseName** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PublicDeliveryAppointmentStatusResponse = Initialize-PSOpenAPIToolsPublicDeliveryAppointmentStatusResponse  -AppointmentId null `
 -RequestedDate null `
 -Status null `
 -TimeSlot null `
 -WarehouseName null
```

- Convert the resource to JSON
```powershell
$PublicDeliveryAppointmentStatusResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

