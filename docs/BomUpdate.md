# BomUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Components** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, quantity, unit, scrap_rate}&#x60;. | [optional] 
**Description** | **String** |  | [optional] 
**Name** | **String** |  | [optional] 
**OutputQuantity** | **Int64** | Output quantity per production run (defaults to 1). | [optional] 
**ProductId** | **String** | The finished product this BOM produces. References the product entity. | [optional] 
**Status** | [**BomStatus**](BomStatus.md) | One of: draft | active | archived | [optional] 

## Examples

- Prepare the resource
```powershell
$BomUpdate = Initialize-PSOpenAPIToolsBomUpdate  -Components null `
 -Description null `
 -Name null `
 -OutputQuantity null `
 -ProductId null `
 -Status null
```

- Convert the resource to JSON
```powershell
$BomUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

