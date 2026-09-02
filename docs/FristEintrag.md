# FristEintrag
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Bezeichnung** | **String** |  | 
**Faellig** | **String** |  | 
**FaelligOriginal** | **String** |  | 
**Hinweis** | **String** |  | [optional] 
**Typ** | **String** |  | 
**Zeitraum** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$FristEintrag = Initialize-PSOpenAPIToolsFristEintrag  -Bezeichnung null `
 -Faellig null `
 -FaelligOriginal null `
 -Hinweis null `
 -Typ null `
 -Zeitraum null
```

- Convert the resource to JSON
```powershell
$FristEintrag | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

