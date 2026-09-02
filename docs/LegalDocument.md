# LegalDocument
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Content** | **String** | Plain text, &#x60;\n\n&#x60; separates paragraphs. | 
**DocType** | [**LegalDocType**](LegalDocType.md) |  | 
**Lang** | [**LanguageCode**](LanguageCode.md) |  | 
**Title** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$LegalDocument = Initialize-PSOpenAPIToolsLegalDocument  -Content null `
 -DocType null `
 -Lang null `
 -Title null
```

- Convert the resource to JSON
```powershell
$LegalDocument | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

