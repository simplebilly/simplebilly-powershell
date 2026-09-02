# GewinnverwendungsZeile
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Betrag** | **String** | Betrag in EUR (2 Nachkommastellen, als String formatiert). | 
**Label** | **String** | Deutsche Bezeichnung der Zeile. | 

## Examples

- Prepare the resource
```powershell
$GewinnverwendungsZeile = Initialize-PSOpenAPIToolsGewinnverwendungsZeile  -Betrag null `
 -Label null
```

- Convert the resource to JSON
```powershell
$GewinnverwendungsZeile | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

