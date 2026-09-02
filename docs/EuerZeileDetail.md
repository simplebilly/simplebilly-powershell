# EuerZeileDetail
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Abschnitt** | **String** |  | 
**BetragGesamt** | **String** |  | 
**Bezeichnung** | **String** |  | 
**Kategorien** | [**EuerKatSumme[]**](EuerKatSumme.md) |  | 
**Zeile** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$EuerZeileDetail = Initialize-PSOpenAPIToolsEuerZeileDetail  -Abschnitt null `
 -BetragGesamt null `
 -Bezeichnung null `
 -Kategorien null `
 -Zeile null
```

- Convert the resource to JSON
```powershell
$EuerZeileDetail | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

