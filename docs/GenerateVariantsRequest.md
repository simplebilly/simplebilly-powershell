# GenerateVariantsRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Options** | [**System.Collections.Hashtable**](Array.md) | Option name → list of values, e.g. &#x60;{&quot;&quot;Color&quot;&quot;: [&quot;&quot;Red&quot;&quot;, &quot;&quot;Blue&quot;&quot;], &quot;&quot;Size&quot;&quot;: [&quot;&quot;S&quot;&quot;, &quot;&quot;M&quot;&quot;]}&#x60;. The cartesian product of these lists is generated. | [optional] 
**PriceDelta** | **String** | Optional per-variant price delta applied to every generated variant. | [optional] 
**ProductId** | **String** |  | 
**SkuPrefix** | **String** | Optional prefix for the generated SKUs (suffix is the option values joined by &#x60;-&#x60;). Falls back to the parent product&#39;s SKU. | [optional] 

## Examples

- Prepare the resource
```powershell
$GenerateVariantsRequest = Initialize-PSOpenAPIToolsGenerateVariantsRequest  -Options null `
 -PriceDelta null `
 -ProductId null `
 -SkuPrefix null
```

- Convert the resource to JSON
```powershell
$GenerateVariantsRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

