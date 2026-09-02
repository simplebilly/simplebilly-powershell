# LegalDocumentUpsert
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Content** | **String** |  | 
**DocType** | **String** |  | 
**Lang** | **String** |  | 
**Title** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$LegalDocumentUpsert = Initialize-PSOpenAPIToolsLegalDocumentUpsert  -Content null `
 -DocType null `
 -Lang null `
 -Title null
```

- Convert the resource to JSON
```powershell
$LegalDocumentUpsert | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

