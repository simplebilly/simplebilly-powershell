# ProductVariantUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Barcode** | **String** |  | [optional] 
**ImageLink** | **String** |  | [optional] 
**IsActive** | **Boolean** |  | [optional] 
**Name** | **String** | Human-readable variant label, e.g. &quot;&quot;Red / M&quot;&quot;. | [optional] 
**OptionValues** | [**AnyType**](.md) | Option name → value map, e.g. &#x60;{&quot;&quot;Color&quot;&quot;: &quot;&quot;Red&quot;&quot;, &quot;&quot;Size&quot;&quot;: &quot;&quot;M&quot;&quot;}&#x60;. | [optional] 
**Price** | **String** | Explicit override price for this variant (takes precedence over parent price + delta). | [optional] 
**PriceDelta** | **String** | Price adjustment relative to the parent product&#39;s &#x60;default_price&#x60;. | [optional] 
**ProductId** | **String** | The parent product this variant belongs to. References the product entity. | [optional] 
**Sku** | **String** | Variant-specific SKU (must be unique per tenant). | [optional] 
**StockQuantity** | **Int64** | Variant-level stock (optional — may be tracked on the parent only). | [optional] 

## Examples

- Prepare the resource
```powershell
$ProductVariantUpdate = Initialize-PSOpenAPIToolsProductVariantUpdate  -Barcode null `
 -ImageLink null `
 -IsActive null `
 -Name null `
 -OptionValues null `
 -Price null `
 -PriceDelta null `
 -ProductId null `
 -Sku null `
 -StockQuantity null
```

- Convert the resource to JSON
```powershell
$ProductVariantUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

