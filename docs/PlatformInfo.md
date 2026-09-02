# PlatformInfo
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Author** | **String** |  | 
**Changelog** | [**ChangelogEntry[]**](ChangelogEntry.md) |  | 
**ConfigFieldNames** | **String[]** |  | 
**ConfigFields** | [**ConfigFieldInfo[]**](ConfigFieldInfo.md) |  | 
**DisplayName** | **String** |  | 
**Platform** | **String** |  | 
**Pricing** | [**PluginPricing**](PluginPricing.md) |  | 
**SupportedEntities** | **String[]** |  | 
**SupportsExport** | **Boolean** |  | 
**SupportsImport** | **Boolean** |  | 
**SupportsOauth** | **Boolean** |  | 
**Version** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PlatformInfo = Initialize-PSOpenAPIToolsPlatformInfo  -Author null `
 -Changelog null `
 -ConfigFieldNames null `
 -ConfigFields null `
 -DisplayName null `
 -Platform null `
 -Pricing null `
 -SupportedEntities null `
 -SupportsExport null `
 -SupportsImport null `
 -SupportsOauth null `
 -Version null
```

- Convert the resource to JSON
```powershell
$PlatformInfo | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

