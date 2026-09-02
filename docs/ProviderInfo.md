# ProviderInfo
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DisplayName** | **String** |  | 
**Name** | **String** |  | 
**RequiresApiKey** | **Boolean** |  | 
**Services** | **String[]** |  | 
**SupportsLabelCreation** | **Boolean** |  | 
**SupportsRateEstimation** | **Boolean** |  | 
**SupportsTracking** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$ProviderInfo = Initialize-PSOpenAPIToolsProviderInfo  -DisplayName null `
 -Name null `
 -RequiresApiKey null `
 -Services null `
 -SupportsLabelCreation null `
 -SupportsRateEstimation null `
 -SupportsTracking null
```

- Convert the resource to JSON
```powershell
$ProviderInfo | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

