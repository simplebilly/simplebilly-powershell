# KstErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gesamt** | **String** |  | 
**Gesamtbelastung** | **String** |  | 
**Gewerbesteuer** | **String** |  | 
**Gewinn** | **String** |  | 
**IstKapitalgesellschaft** | **Boolean** |  | 
**Jahr** | **Int32** |  | 
**Koerperschaftsteuer** | **String** |  | 
**Solidaritaetszuschlag** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$KstErgebnis = Initialize-PSOpenAPIToolsKstErgebnis  -Gesamt null `
 -Gesamtbelastung null `
 -Gewerbesteuer null `
 -Gewinn null `
 -IstKapitalgesellschaft null `
 -Jahr null `
 -Koerperschaftsteuer null `
 -Solidaritaetszuschlag null
```

- Convert the resource to JSON
```powershell
$KstErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

