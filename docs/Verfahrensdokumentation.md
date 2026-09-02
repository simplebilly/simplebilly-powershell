# Verfahrensdokumentation
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Entries** | [**ComplianceEntry[]**](ComplianceEntry.md) |  | 
**GeneratedAt** | **String** |  | 
**Title** | **String** |  | 
**Version** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$Verfahrensdokumentation = Initialize-PSOpenAPIToolsVerfahrensdokumentation  -Entries null `
 -GeneratedAt null `
 -Title null `
 -Version null
```

- Convert the resource to JSON
```powershell
$Verfahrensdokumentation | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

