# ComplianceEntry
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **String** |  | 
**Module** | **String** |  | 
**Regulations** | **String[]** |  | 

## Examples

- Prepare the resource
```powershell
$ComplianceEntry = Initialize-PSOpenAPIToolsComplianceEntry  -Description null `
 -Module null `
 -Regulations null
```

- Convert the resource to JSON
```powershell
$ComplianceEntry | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

