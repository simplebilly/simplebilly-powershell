# ElsterStatus
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CertConfigured** | **Boolean** |  | 
**EricAvailable** | **Boolean** |  | 
**EricVersion** | **String** |  | [optional] 
**FeatureEnabled** | **Boolean** |  | 
**Hint** | **String** |  | 
**Mode** | **String** |  | 
**VendorIdConfigured** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$ElsterStatus = Initialize-PSOpenAPIToolsElsterStatus  -CertConfigured null `
 -EricAvailable null `
 -EricVersion null `
 -FeatureEnabled null `
 -Hint null `
 -Mode null `
 -VendorIdConfigured null
```

- Convert the resource to JSON
```powershell
$ElsterStatus | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

