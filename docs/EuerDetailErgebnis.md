# EuerDetailErgebnis
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Jahr** | **Int32** |  | 
**Zeilen** | [**EuerZeileDetail[]**](EuerZeileDetail.md) |  | 

## Examples

- Prepare the resource
```powershell
$EuerDetailErgebnis = Initialize-PSOpenAPIToolsEuerDetailErgebnis  -Jahr null `
 -Zeilen null
```

- Convert the resource to JSON
```powershell
$EuerDetailErgebnis | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

