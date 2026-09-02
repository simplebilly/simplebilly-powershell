# EuerErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AnlageZugaenge** | **String** |  | 
**GewinnVerlust** | **String** |  | 
**Jahr** | **Int32** |  | 
**SummeAusgaben** | **String** |  | 
**SummeEinnahmen** | **String** |  | 
**Zeilen** | [**EuerZeile[]**](EuerZeile.md) |  | 

## Examples

- Prepare the resource
```powershell
$EuerErgebnis = Initialize-PSOpenAPIToolsEuerErgebnis  -AnlageZugaenge null `
 -GewinnVerlust null `
 -Jahr null `
 -SummeAusgaben null `
 -SummeEinnahmen null `
 -Zeilen null
```

- Convert the resource to JSON
```powershell
$EuerErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

