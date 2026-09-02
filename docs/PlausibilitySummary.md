# PlausibilitySummary
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Errors** | **Int32** |  | 
**OverallStatus** | [**CheckStatus**](CheckStatus.md) |  | 
**Passed** | **Int32** |  | 
**TotalChecks** | **Int32** |  | 
**Warnings** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$PlausibilitySummary = Initialize-PSOpenAPIToolsPlausibilitySummary  -Errors null `
 -OverallStatus null `
 -Passed null `
 -TotalChecks null `
 -Warnings null
```

- Convert the resource to JSON
```powershell
$PlausibilitySummary | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

