# Order
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AuditLog** | [**AnyType**](.md) |  | [optional] 
**Currency** | **String** |  | 
**CustomerId** | **String** | References the customer entity. | 
**ExternalReference** | **String** |  | [optional] 
**InvoiceAddress** | [**AnyType**](.md) |  | [optional] 
**Items** | [**AnyType**](.md) |  | [optional] 
**Language** | [**LanguageCode**](LanguageCode.md) |  | [optional] 
**OrderStatus** | [**OrderStatus**](OrderStatus.md) |  | 
**PaymentMethod** | [**PaymentMethod**](PaymentMethod.md) |  | 
**ShippingAddress** | [**AnyType**](.md) |  | [optional] 
**ShippingCost** | **String** |  | 
**ShippingMethod** | **String** |  | 
**ShippingWeight** | **String** |  | 
**Tags** | **String[]** |  | 
**TotalCost** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$Order = Initialize-PSOpenAPIToolsOrder  -AuditLog null `
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
$Order | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

