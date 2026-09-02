# FristenErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Anzahl** | **Int32** |  | 
**Fristen** | [**FristEintrag[]**](FristEintrag.md) |  | 

## Examples

- Prepare the resource
```powershell
$FristenErgebnis = Initialize-PSOpenAPIToolsFristenErgebnis  -Anzahl null `
 -Fristen null
```

- Convert the resource to JSON
```powershell
$FristenErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

