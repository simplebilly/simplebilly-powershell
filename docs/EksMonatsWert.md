# EksMonatsWert
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Ausgaben** | **String** |  | 
**Einnahmen** | **String** |  | 
**Ergebnis** | **String** |  | 
**Monat** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$EksMonatsWert = Initialize-PSOpenAPIToolsEksMonatsWert  -Ausgaben null `
 -Einnahmen null `
 -Ergebnis null `
 -Monat null
```

- Convert the resource to JSON
```powershell
$EksMonatsWert | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

