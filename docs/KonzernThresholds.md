# KonzernThresholds
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Bilanzsumme** | **String** |  | 
**Mitarbeiter** | **Int64** |  | 
**NettoUmsatz** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$KonzernThresholds = Initialize-PSOpenAPIToolsKonzernThresholds  -Bilanzsumme null `
 -Mitarbeiter null `
 -NettoUmsatz null
```

- Convert the resource to JSON
```powershell
$KonzernThresholds | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

