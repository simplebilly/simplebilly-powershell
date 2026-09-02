# KostenEintrag
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Beschreibung** | **String** |  | 
**Betrag** | **String** |  | 
**Datum** | **String** |  | 
**Typ** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$KostenEintrag = Initialize-PSOpenAPIToolsKostenEintrag  -Beschreibung null `
 -Betrag null `
 -Datum null `
 -Typ null
```

- Convert the resource to JSON
```powershell
$KostenEintrag | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

