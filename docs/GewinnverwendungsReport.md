# GewinnverwendungsReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Bilanzgewinn** | **String** | Bilanzgewinn nach Einstellung (§ 174 AktG, Beschluss der HV). | 
**GesetzlicheRuecklageBestand** | **String** |  | 
**GesetzlicheRuecklageCap** | **String** | Deckel: 10 % des Grundkapitals (§ 150 Abs. 2 AktG). | 
**GesetzlicheRuecklageNach** | **String** | Rücklage nach Einstellung. | 
**GesetzlicheRuecklageSoll** | **String** | Vorgeschlagene Einstellung in die gesetzliche Rücklage (§ 150 Abs. 2 AktG). | 
**GezeichnetesKapital** | **String** |  | 
**Jahresueberschuss** | **String** |  | 
**Year** | **Int32** |  | 
**Zeilen** | [**GewinnverwendungsZeile[]**](GewinnverwendungsZeile.md) |  | 

## Examples

- Prepare the resource
```powershell
$GewinnverwendungsReport = Initialize-PSOpenAPIToolsGewinnverwendungsReport  -Bilanzgewinn null `
 -GesetzlicheRuecklageBestand null `
 -GesetzlicheRuecklageCap null `
 -GesetzlicheRuecklageNach null `
 -GesetzlicheRuecklageSoll null `
 -GezeichnetesKapital null `
 -Jahresueberschuss null `
 -Year null `
 -Zeilen null
```

- Convert the resource to JSON
```powershell
$GewinnverwendungsReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

