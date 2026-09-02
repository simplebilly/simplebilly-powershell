# Shipment
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DeliveredAt** | **System.DateTime** |  | [optional] 
**LabelUrl** | **String** |  | [optional] 
**LineItemsShipment** | [**AnyType**](.md) |  | [optional] 
**OrderId** | **String** | References the order entity. | 
**RecipientAddress** | [**AnyType**](.md) |  | [optional] 
**ShipmentDate** | **System.DateTime** |  | 
**ShippingCarrier** | **String** |  | 
**ShippingCost** | **String** |  | [optional] 
**ShippingMethod** | **String** |  | [optional] 
**SignedBy** | **String** |  | [optional] 
**Status** | **String** |  | 
**TrackingEvents** | [**AnyType**](.md) | Latest carrier tracking events (from the live tracking API). | [optional] 
**TrackingNumber** | **String** |  | [optional] 
**TrackingUrl** | **String** |  | [optional] 
**WeightKg** | **Double** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$Shipment = Initialize-PSOpenAPIToolsShipment  -DeliveredAt null `
 -LabelUrl null `
 -LineItemsShipment null `
 -OrderId null `
 -RecipientAddress null `
 -ShipmentDate null `
 -ShippingCarrier null `
 -ShippingCost null `
 -ShippingMethod null `
 -SignedBy null `
 -Status null `
 -TrackingEvents null `
 -TrackingNumber null `
 -TrackingUrl null `
 -WeightKg null
```

- Convert the resource to JSON
```powershell
$Shipment | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

