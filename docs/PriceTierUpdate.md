# PriceTierUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerGroupId** | **String** | None &#x3D; tier applies to all customers; otherwise a customer group id. | [optional] 
**MinQuantity** | **Int64** | Quantity from which this tier applies (inclusive). | [optional] 
**ProductId** | **String** | References the product entity. | [optional] 
**UnitPrice** | **String** | Net unit price once &#x60;min_quantity&#x60; is reached. | 

## Examples

- Prepare the resource
```powershell
$PriceTierUpdate = Initialize-PSOpenAPIToolsPriceTierUpdate  -CustomerGroupId null `
 -MinQuantity null `
 -ProductId null `
 -UnitPrice null
```

- Convert the resource to JSON
```powershell
$PriceTierUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

