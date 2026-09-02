# OrderUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AuditLog** | [**AnyType**](.md) |  | [optional] 
**Currency** | **String** |  | [optional] 
**CustomerId** | **String** | References the customer entity. | [optional] 
**ExternalReference** | **String** |  | [optional] 
**InvoiceAddress** | [**AnyType**](.md) |  | [optional] 
**Items** | [**AnyType**](.md) |  | [optional] 
**Language** | [**LanguageCode**](LanguageCode.md) |  | [optional] 
**OrderStatus** | [**OrderStatus**](OrderStatus.md) |  | [optional] 
**PaymentMethod** | [**PaymentMethod**](PaymentMethod.md) |  | [optional] 
**ShippingAddress** | [**AnyType**](.md) |  | [optional] 
**ShippingCost** | **String** |  | [optional] 
**ShippingMethod** | **String** |  | [optional] 
**ShippingWeight** | **String** |  | [optional] 
**Tags** | **String[]** |  | [optional] 
**TotalCost** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$OrderUpdate = Initialize-PSOpenAPIToolsOrderUpdate  -AuditLog null `
 -Currency null `
 -CustomerId null `
 -ExternalReference null `
 -InvoiceAddress null `
 -Items null `
 -Language null `
 -OrderStatus null `
 -PaymentMethod null `
 -ShippingAddress null `
 -ShippingCost null `
 -ShippingMethod null `
 -ShippingWeight null `
 -Tags null `
 -TotalCost null
```

- Convert the resource to JSON
```powershell
$OrderUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

