# KontoItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Anfangsbestand** | **String** |  | 
**HabenUmsatz** | **String** |  | 
**Konto** | **String** |  | 
**Name** | **String** |  | 
**Saldo** | **String** |  | 
**SollUmsatz** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$KontoItem = Initialize-PSOpenAPIToolsKontoItem  -Anfangsbestand null `
 -HabenUmsatz null `
 -Konto null `
 -Name null `
 -Saldo null `
 -SollUmsatz null
```

- Convert the resource to JSON
```powershell
$KontoItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

