# Participation
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AcquiredAt** | **System.DateTime** | Datum des Erwerbs der Beteiligung. | [optional] 
**BoardAppointment** | **Boolean** | Bestellungsrecht für Geschäftsführung/Aufsichtsrat (§ 290 Abs. 2 Nr. 2 HGB). | [optional] 
**CompanyName** | **String** | Name des Beteiligungsunternehmens (§ 271 HGB). | [optional] 
**ControlAgreement** | **Boolean** | Beherrschungsvertrag (§ 290 Abs. 2 Nr. 3 HGB). | [optional] 
**LegalForm** | **String** | Rechtsform, z. B. &quot;&quot;GmbH&quot;&quot;. | [optional] 
**OwnershipPct** | **String** | Anteilsquote in Prozent (§ 271 HGB; &gt; 20 % widerlegbare Vermutung). | [optional] 
**PurposeVehicle** | **Boolean** | Zweckgesellschaft (§ 290 Abs. 2 Nr. 4 HGB). | [optional] 
**VotingMajority** | **Boolean** | Stimmrechtsmehrheit (§ 290 Abs. 2 Nr. 1 HGB). | [optional] 

## Examples

- Prepare the resource
```powershell
$Participation = Initialize-PSOpenAPIToolsParticipation  -AcquiredAt null `
 -BoardAppointment null `
 -CompanyName null `
 -ControlAgreement null `
 -LegalForm null `
 -OwnershipPct null `
 -PurposeVehicle null `
 -VotingMajority null
```

- Convert the resource to JSON
```powershell
$Participation | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

