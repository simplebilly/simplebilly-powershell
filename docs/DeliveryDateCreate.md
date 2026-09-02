# DeliveryDateCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **String** | References the customer entity. | [optional] 
**FulfilledDate** | **System.DateTime** | Date actually delivered (set on fulfillment). | [optional] 
**Note** | **String** |  | [optional] 
**OrderNumber** | **String** | Sales order number (&#x60;order.order_number&#x60;). | 
**OriginalDate** | **System.DateTime** | Original date promised before rescheduling. | [optional] 
**ProductId** | **String** | Product line item this date applies to, if per-item. References the product entity. | [optional] 
**PromisedDate** | **System.DateTime** | Date promised to the customer. | 
**Status** | [**DeliveryDateStatus**](DeliveryDateStatus.md) | One of: promised | confirmed | rescheduled | fulfilled | late | cancelled | 

## Examples

- Prepare the resource
```powershell
$DeliveryDateCreate = Initialize-PSOpenAPIToolsDeliveryDateCreate  -CustomerId null `
 -FulfilledDate null `
 -Note null `
 -OrderNumber null `
 -OriginalDate null `
 -ProductId null `
 -PromisedDate null `
 -Status null
```

- Convert the resource to JSON
```powershell
$DeliveryDateCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

