# GroupFigureUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Bilanzsumme** | **String** | Bilanzsumme in EUR (§ 293 Abs. 1 Nr. 1 HGB). | [optional] 
**ExemptionClaimed** | **Boolean** | § 291-Befreiung in Anspruch genommen. | [optional] 
**Mitarbeiter** | **Int64** | Durchschnittliche Arbeitnehmerzahl (§ 293 Abs. 1 Nr. 3 HGB). | [optional] 
**NettoUmsatz** | **String** | Netto-Umsatzerlöse in EUR (§ 293 Abs. 1 Nr. 2 HGB). | [optional] 
**ParentName** | **String** | Name des Mutterunternehmens (§ 291 HGB, Zwischenholding). | [optional] 
**ParentSitus** | **String** | Sitz des Mutterunternehmens, z. B. &quot;&quot;EU/EWR&quot;&quot; (§ 291 HGB). | [optional] 

## Examples

- Prepare the resource
```powershell
$GroupFigureUpdate = Initialize-PSOpenAPIToolsGroupFigureUpdate  -Bilanzsumme null `
 -ExemptionClaimed null `
 -Mitarbeiter null `
 -NettoUmsatz null `
 -ParentName null `
 -ParentSitus null
```

- Convert the resource to JSON
```powershell
$GroupFigureUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

