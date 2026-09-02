# EuerZeile
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Abschnitt** | **String** |  | 
**Betrag** | **String** |  | 
**Bezeichnung** | **String** |  | 
**Zeile** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$EuerZeile = Initialize-PSOpenAPIToolsEuerZeile  -Abschnitt null `
 -Betrag null `
 -Bezeichnung null `
 -Zeile null
```

- Convert the resource to JSON
```powershell
$EuerZeile | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

