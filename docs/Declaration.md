# Declaration
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**DeclarationType** | [**DeclarationType**](DeclarationType.md) | Art der Erklärung: &quot;&quot;dcgk&quot;&quot; (Entsprechenserklärung § 161 AktG) oder &quot;&quot;unternehmensfuehrung&quot;&quot; (Erklärung zur Unternehmensführung § 289f HGB). | [optional] 
**IsCurrent** | **Boolean** | Kennzeichnet die aktuell gültige Fassung (max. eine je Mandant). | [optional] 
**Text** | **String** | Inhalt der Erklärung als Markdown. | [optional] 
**ValidFrom** | **System.DateTime** | Datum, ab dem die Erklärung gilt. | [optional] 
**Version** | **String** | Versionsbezeichnung der Erklärung (z.B. &quot;&quot;2025-01&quot;&quot;). | [optional] 

## Examples

- Prepare the resource
```powershell
$Declaration = Initialize-PSOpenAPIToolsDeclaration  -DeclarationType null `
 -IsCurrent null `
 -Text null `
 -ValidFrom null `
 -Version null
```

- Convert the resource to JSON
```powershell
$Declaration | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

