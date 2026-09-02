# KontoReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GeneratedAt** | **String** |  | 
**Konten** | [**KontoItem[]**](KontoItem.md) |  | 
**Period** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$KontoReport = Initialize-PSOpenAPIToolsKontoReport  -GeneratedAt null `
 -Konten null `
 -Period null
```

- Convert the resource to JSON
```powershell
$KontoReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

