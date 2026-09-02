# KycRecord
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CustomerId** | **String** | Referenz auf den Kunden/Kontakt. | [optional] 
**CustomerName** | **String** | Name des Kunden (für die Suche). | [optional] 
**KycDate** | **System.DateTime** | Datum der KYC-Prüfung (GwG § 8). | [optional] 
**Notes** | **String** | Freitext-Notizen. | [optional] 
**RetentionUntil** | **System.DateTime** | Aufbewahrungsfrist (GwG § 8 Abs. 4: 5 Jahre). | [optional] 
**RiskAssessment** | **String** | Risikoeinschätzung (z. B. Risikoklasse). | [optional] 

## Examples

- Prepare the resource
```powershell
$KycRecord = Initialize-PSOpenAPIToolsKycRecord  -CustomerId null `
 -CustomerName null `
 -KycDate null `
 -Notes null `
 -RetentionUntil null `
 -RiskAssessment null
```

- Convert the resource to JSON
```powershell
$KycRecord | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

