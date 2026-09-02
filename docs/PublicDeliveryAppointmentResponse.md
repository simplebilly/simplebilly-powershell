# PublicDeliveryAppointmentResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AppointmentId** | **String** |  | 
**ConfirmationHint** | **String** | Carries the status-check token (email is out of scope for now). | 
**Message** | **String** |  | 
**Status** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PublicDeliveryAppointmentResponse = Initialize-PSOpenAPIToolsPublicDeliveryAppointmentResponse  -AppointmentId null `
 -ConfirmationHint null `
 -Message null `
 -Status null
```

- Convert the resource to JSON
```powershell
$PublicDeliveryAppointmentResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

