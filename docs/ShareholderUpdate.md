# ShareholderUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | **String** | Anschrift des Aktionärs (§ 67 Abs. 1 AktG). | [optional] 
**BirthDate** | **System.DateTime** | Geburtsdatum des Aktionärs (§ 67 Abs. 1 AktG). | [optional] 
**Email** | **String** | Elektronische Adresse (E-Mail) für die Kommunikation der Gesellschaft. | [optional] 
**FirstName** | **String** | Vorname des Aktionärs (§ 67 Abs. 1 AktG). | [optional] 
**LastName** | **String** | Nachname des Aktionärs (§ 67 Abs. 1 AktG). | [optional] 
**ShareNumber** | **String** | Aktiennummer bzw. Sammelurkunde (bei Nennbetragsaktien). | [optional] 
**Shares** | **String** | Stückzahl der gehaltenen Stückaktien (§ 67 Abs. 1 AktG). | [optional] 

## Examples

- Prepare the resource
```powershell
$ShareholderUpdate = Initialize-PSOpenAPIToolsShareholderUpdate  -Address null `
 -BirthDate null `
 -Email null `
 -FirstName null `
 -LastName null `
 -ShareNumber null `
 -Shares null
```

- Convert the resource to JSON
```powershell
$ShareholderUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

