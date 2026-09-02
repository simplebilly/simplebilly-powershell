# ProductAttributeCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**IsFilterable** | **Boolean** | Whether this attribute participates in the shop&#39;s faceted filters. | [optional] 
**Name** | **String** | Attribute name, e.g. &#x60;Material&#x60;, &#x60;Farbe&#x60;, &#x60;Gewicht&#x60;. | 
**Position** | **Int32** | Ordering position within the product&#39;s attribute list. | [optional] 
**ProductId** | **String** | The product this attribute belongs to. References the product entity. | 
**Unit** | **String** | Optional unit of measure for numeric attributes, e.g. &#x60;g&#x60;, &#x60;cm&#x60;. | [optional] 
**Value** | **String** | Attribute value, e.g. &#x60;Baumwolle&#x60;, &#x60;Rot&#x60;, &#x60;180g&#x60;. | 

## Examples

- Prepare the resource
```powershell
$ProductAttributeCreate = Initialize-PSOpenAPIToolsProductAttributeCreate  -IsFilterable null `
 -Name null `
 -Position null `
 -ProductId null `
 -Unit null `
 -Value null
```

- Convert the resource to JSON
```powershell
$ProductAttributeCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

