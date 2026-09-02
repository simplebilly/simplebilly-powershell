# DeliveryAppointment
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **String** |  | 
**Notes** | **String** |  | [optional] 
**Phone** | **String** |  | [optional] 
**RequestedDate** | **System.DateTime** |  | 
**Status** | [**DeliveryAppointmentStatus**](DeliveryAppointmentStatus.md) | One of: requested | confirmed | arrived | cancelled | completed | 
**SupplierName** | **String** |  | 
**TimeSlot** | **String** | e.g. &quot;&quot;08:00-10:00&quot;&quot; | [optional] 
**WarehouseId** | **String** | References the warehouse entity. | 

## Examples

- Prepare the resource
```powershell
$DeliveryAppointment = Initialize-PSOpenAPIToolsDeliveryAppointment  -Email null `
 -Notes null `
 -Phone null `
 -RequestedDate null `
 -Status null `
 -SupplierName null `
 -TimeSlot null `
 -WarehouseId null
```

- Convert the resource to JSON
```powershell
$DeliveryAppointment | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

