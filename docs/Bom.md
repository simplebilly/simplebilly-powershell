# Bom
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Components** | [**AnyType**](.md) | JSON array of &#x60;{product_id, name, quantity, unit, scrap_rate}&#x60;. | [optional] 
**Description** | **String** |  | [optional] 
**Name** | **String** |  | 
**OutputQuantity** | **Int64** | Output quantity per production run (defaults to 1). | [optional] 
**ProductId** | **String** | The finished product this BOM produces. References the product entity. | 
**Status** | [**BomStatus**](BomStatus.md) | One of: draft | active | archived | [optional] 

## Examples

- Prepare the resource
```powershell
$Bom = Initialize-PSOpenAPIToolsBom  -Components null `
 -Description null `
 -Name null `
 -OutputQuantity null `
 -ProductId null `
 -Status null
```

- Convert the resource to JSON
```powershell
$Bom | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

