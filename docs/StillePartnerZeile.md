# StillePartnerZeile
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Auseinandersetzungsguthaben** | **String** |  | 
**Gewinnanteil** | **String** |  | 
**Gewinnvortrag** | **String** |  | 
**Hinweis** | **String** |  | [optional] 
**InstrumentType** | **String** |  | 
**Kest** | **String** |  | 
**Name** | **String** |  | 
**VerlustVerrechnungskonto** | **String** |  | 
**Verlustanteil** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$StillePartnerZeile = Initialize-PSOpenAPIToolsStillePartnerZeile  -Auseinandersetzungsguthaben null `
 -Gewinnanteil null `
 -Gewinnvortrag null `
 -Hinweis null `
 -InstrumentType null `
 -Kest null `
 -Name null `
 -VerlustVerrechnungskonto null `
 -Verlustanteil null
```

- Convert the resource to JSON
```powershell
$StillePartnerZeile | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

