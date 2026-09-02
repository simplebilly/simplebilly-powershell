# QuotaOverride
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Features** | [**QuotaOverrideFeatures**](QuotaOverrideFeatures.md) |  | [optional] 
**MaxConnectors** | **Int32** |  | [optional] 
**MaxInvoicesPerMonth** | **Int64** |  | [optional] 
**MaxUsers** | **Int32** |  | [optional] 
**Metered** | **System.Collections.Hashtable** |  | [optional] 
**Plan** | **String** | Custom plan id; unknown ids resolve to enterprise limits. | [optional] 

## Examples

- Prepare the resource
```powershell
$QuotaOverride = Initialize-PSOpenAPIToolsQuotaOverride  -Features null `
 -MaxConnectors null `
 -MaxInvoicesPerMonth null `
 -MaxUsers null `
 -Metered null `
 -Plan null
```

- Convert the resource to JSON
```powershell
$QuotaOverride | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

