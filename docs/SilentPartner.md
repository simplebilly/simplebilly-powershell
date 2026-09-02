# SilentPartner
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContractDate** | **System.DateTime** | Datum des Vertragsabschlusses. | [optional] 
**Einlage** | **String** | Einlage (§ 230 HGB). | [optional] 
**GewinnquotePct** | **String** | Gewinnbeteiligungsquote in Prozent (§ 231 HGB). | [optional] 
**Gewinnvortrag** | **String** | Nicht erhobene Gewinne (§ 232 Abs. 3 HGB). | [optional] 
**InstrumentType** | [**InstrumentType**](InstrumentType.md) | Instrument: &quot;&quot;typisch&quot;&quot; | &quot;&quot;atypisch&quot;&quot; | &quot;&quot;partiarisches_darlehen&quot;&quot; | &quot;&quot;genussrecht&quot;&quot;. | 
**KestPflichtig** | **Boolean** | 25 % Kapitalertragsteuer einbehalten (§ 43 Abs. 1 Nr. 3 EStG; typisch + partiarisches Darlehen). | [optional] 
**Name** | **String** | Name des stillen Gesellschafters. | [optional] 
**Notes** | **String** | Freitext-Notizen. | [optional] 
**VerlustVerrechnungskonto** | **String** | Kumulierte Verluste gegen die Einlage (§ 232 Abs. 2 HGB, ≤ Einlage). | [optional] 
**Verlustbeteiligung** | **Boolean** | Verlustbeteiligung (§ 231 Abs. 2 HGB; kann ausgeschlossen werden). | [optional] 

## Examples

- Prepare the resource
```powershell
$SilentPartner = Initialize-PSOpenAPIToolsSilentPartner  -ContractDate null `
 -Einlage null `
 -GewinnquotePct null `
 -Gewinnvortrag null `
 -InstrumentType null `
 -KestPflichtig null `
 -Name null `
 -Notes null `
 -VerlustVerrechnungskonto null `
 -Verlustbeteiligung null
```

- Convert the resource to JSON
```powershell
$SilentPartner | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

