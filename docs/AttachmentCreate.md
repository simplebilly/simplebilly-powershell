# AttachmentCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ContactId** | **String** | Contact this attachment belongs to (per-contact DMS). References the contact entity. | [optional] 
**FileName** | **String** |  | 
**FileSize** | **Int64** |  | [optional] 
**MimeType** | **String** |  | [optional] 
**OriginalName** | **String** |  | 
**PdfaPath** | **String** |  | [optional] 
**Sha256Hash** | **String** |  | [optional] 
**UploadedBy** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$AttachmentCreate = Initialize-PSOpenAPIToolsAttachmentCreate  -ContactId null `
 -FileName null `
 -FileSize null `
 -MimeType null `
 -OriginalName null `
 -PdfaPath null `
 -Sha256Hash null `
 -UploadedBy null
```

- Convert the resource to JSON
```powershell
$AttachmentCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

