# EksErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Gesamtergebnis** | **String** |  | 
**Monate** | [**EksMonatsWert[]**](EksMonatsWert.md) |  | 
**PrognoseNaechste6Monate** | **String** |  | 
**SummeAusgaben** | **String** |  | 
**SummeEinnahmen** | **String** |  | 
**ZeitraumBis** | **String** |  | 
**ZeitraumVon** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$EksErgebnis = Initialize-PSOpenAPIToolsEksErgebnis  -Gesamtergebnis null `
 -Monate null `
 -PrognoseNaechste6Monate null `
 -SummeAusgaben null `
 -SummeEinnahmen null `
 -ZeitraumBis null `
 -ZeitraumVon null
```

- Convert the resource to JSON
```powershell
$EksErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

