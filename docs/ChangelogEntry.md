# ChangelogEntry
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Date** | **String** |  | 
**Notes** | **String** |  | 
**Version** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ChangelogEntry = Initialize-PSOpenAPIToolsChangelogEntry  -Date null `
 -Notes null `
 -Version null
```

- Convert the resource to JSON
```powershell
$ChangelogEntry | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

