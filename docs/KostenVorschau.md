# KostenVorschau
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Eintraege** | [**KostenEintrag[]**](KostenEintrag.md) |  | 
**Gesamt** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$KostenVorschau = Initialize-PSOpenAPIToolsKostenVorschau  -Eintraege null `
 -Gesamt null
```

- Convert the resource to JSON
```powershell
$KostenVorschau | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

