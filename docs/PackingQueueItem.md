# PackingQueueItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **String** |  | 
**CustomerId** | **String** |  | 
**DeliveryNotePrinted** | **Boolean** |  | 
**Items** | [**AnyType**](.md) |  | 
**ItemsCount** | **Int32** |  | 
**LabelPrinted** | **Boolean** |  | 
**OrderNumber** | **String** |  | 
**OrderStatus** | **String** |  | 
**ShipmentId** | **String** |  | [optional] 
**ShippingAddress** | [**AnyType**](.md) |  | [optional] 
**ShippingMethod** | **String** |  | 
**TrackingNumber** | **String** |  | [optional] 
**VideoRecording** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PackingQueueItem = Initialize-PSOpenAPIToolsPackingQueueItem  -CreatedAt null `
 -CustomerId null `
 -DeliveryNotePrinted null `
 -Items null `
 -ItemsCount null `
 -LabelPrinted null `
 -OrderNumber null `
 -OrderStatus null `
 -ShipmentId null `
 -ShippingAddress null `
 -ShippingMethod null `
 -TrackingNumber null `
 -VideoRecording null
```

- Convert the resource to JSON
```powershell
$PackingQueueItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

