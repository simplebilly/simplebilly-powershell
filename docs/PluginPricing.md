# PluginPricing
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **String** |  | 
**Price** | **Double** |  | 
**PricePerMonth** | **Double** |  | 

## Examples

- Prepare the resource
```powershell
$PluginPricing = Initialize-PSOpenAPIToolsPluginPricing  -Type null `
 -Price null `
 -PricePerMonth null
```

- Convert the resource to JSON
```powershell
$PluginPricing | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

