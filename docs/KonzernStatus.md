# KonzernStatus
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Groessenbefreit** | **Boolean** |  | 
**Kapitalmarktorientiert** | **Boolean** |  | 
**Konzernabschlusspflicht** | **Boolean** |  | 
**MissingGroupFigures** | **Boolean** | Keine group_figures-Zeile für das Jahr vorhanden → keine Größenbefreiung. | 
**Mutterunternehmen** | **Boolean** | Mutterunternehmen: mindestens eine beherrschte Beteiligung (§ 290 Abs. 1 HGB). | 
**ParentName** | **String** | Mutterunternehmen für die Zwischenholding-Befreiung (§ 291 HGB). | [optional] 
**ParentSitus** | **String** |  | [optional] 
**Participations** | [**KonzernBeteiligung[]**](KonzernBeteiligung.md) |  | 
**Thresholds** | [**KonzernThresholds**](KonzernThresholds.md) |  | 
**Year** | **Int32** |  | 
**ZwischenholdingBefreit** | **Boolean** |  | 
**ZwischenholdingHinweis** | **String** | Hinweis zu den § 291-Voraussetzungen (EU/EWR-Sitz, geprüfter Konzernabschluss). | [optional] 

## Examples

- Prepare the resource
```powershell
$KonzernStatus = Initialize-PSOpenAPIToolsKonzernStatus  -Groessenbefreit null `
 -Kapitalmarktorientiert null `
 -Konzernabschlusspflicht null `
 -MissingGroupFigures null `
 -Mutterunternehmen null `
 -ParentName null `
 -ParentSitus null `
 -Participations null `
 -Thresholds null `
 -Year null `
 -ZwischenholdingBefreit null `
 -ZwischenholdingHinweis null
```

- Convert the resource to JSON
```powershell
$KonzernStatus | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

