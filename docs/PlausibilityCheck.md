# PlausibilityCheck
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Detail** | **String** |  | 
**Id** | **String** |  | 
**Name** | **String** |  | 
**Severity** | [**Severity**](Severity.md) |  | 
**Status** | [**CheckStatus**](CheckStatus.md) |  | 

## Examples

- Prepare the resource
```powershell
$PlausibilityCheck = Initialize-PSOpenAPIToolsPlausibilityCheck  -Detail null `
 -Id null `
 -Name null `
 -Severity null `
 -Status null
```

- Convert the resource to JSON
```powershell
$PlausibilityCheck | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

