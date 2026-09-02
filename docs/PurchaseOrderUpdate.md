# PurchaseOrderUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **String** |  | [optional] 
**DeliveryAddress** | [**AnyType**](.md) |  | [optional] 
**ExpectedDeliveryDate** | **System.DateTime** |  | [optional] 
**LineItems** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, quantity, unit_price_net, tax_rate, delivery_date}&#x60;. | [optional] 
**Notes** | **String** |  | [optional] 
**OrderDate** | **System.DateTime** |  | [optional] 
**PoNumber** | **String** |  | [optional] 
**Status** | [**PurchaseOrderStatus**](PurchaseOrderStatus.md) | One of: draft | ordered | partially_received | received | cancelled | [optional] 
**SupplierContactId** | **String** | References the supplier entity. | [optional] 
**SupplierName** | **String** |  | [optional] 
**TotalGrossAmount** | **String** |  | [optional] 
**TotalNetAmount** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PurchaseOrderUpdate = Initialize-PSOpenAPIToolsPurchaseOrderUpdate  -Currency null `
 -DeliveryAddress null `
 -ExpectedDeliveryDate null `
 -LineItems null `
 -Notes null `
 -OrderDate null `
 -PoNumber null `
 -Status null `
 -SupplierContactId null `
 -SupplierName null `
 -TotalGrossAmount null `
 -TotalNetAmount null
```

- Convert the resource to JSON
```powershell
$PurchaseOrderUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

