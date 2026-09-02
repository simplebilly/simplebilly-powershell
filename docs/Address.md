# Address
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**City** | **String** |  | 
**Company** | **String** |  | [optional] 
**Country** | **String** | ISO 3166-1 alpha-2 country code (e.g. &quot;&quot;DE&quot;&quot;, &quot;&quot;PL&quot;&quot;, &quot;&quot;FR&quot;&quot;). | 
**Email** | **String** |  | [optional] 
**Name** | **String** |  | 
**Phone** | **String** |  | [optional] 
**Street** | **String** |  | 
**StreetNumber** | **String** |  | 
**Zip** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$Address = Initialize-PSOpenAPIToolsAddress  -City null `
 -Company null `
 -Country null `
 -Email null `
 -Name null `
 -Phone null `
 -Street null `
 -StreetNumber null `
 -Zip null
```

- Convert the resource to JSON
```powershell
$Address | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

