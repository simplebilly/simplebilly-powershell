# PublicDeliveryAppointmentRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **String** |  | 
**Notes** | **String** |  | [optional] 
**RequestedDate** | **System.DateTime** |  | 
**SupplierName** | **String** |  | 
**TimeSlot** | **String** |  | [optional] 
**WarehouseCode** | **String** | Warehouse &#x60;code&#x60; — the supplier does not know the warehouse uuid. | 

## Examples

- Prepare the resource
```powershell
$PublicDeliveryAppointmentRequest = Initialize-PSOpenAPIToolsPublicDeliveryAppointmentRequest  -Email null `
 -Notes null `
 -RequestedDate null `
 -SupplierName null `
 -TimeSlot null `
 -WarehouseCode null
```

- Convert the resource to JSON
```powershell
$PublicDeliveryAppointmentRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

