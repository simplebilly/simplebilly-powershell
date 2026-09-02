# PlausibilityReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Checks** | [**PlausibilityCheck[]**](PlausibilityCheck.md) |  | 
**GeneratedAt** | **String** |  | 
**Summary** | [**PlausibilitySummary**](PlausibilitySummary.md) |  | 

## Examples

- Prepare the resource
```powershell
$PlausibilityReport = Initialize-PSOpenAPIToolsPlausibilityReport  -Checks null `
 -GeneratedAt null `
 -Summary null
```

- Convert the resource to JSON
```powershell
$PlausibilityReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

