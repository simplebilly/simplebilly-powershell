# AttachmentVersion
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AttachmentId** | **String** | Parent attachment whose history this row records. | 
**FileName** | **String** | Storage key of this version&#39;s bytes. | 
**FileSize** | **Int64** |  | [optional] 
**MimeType** | **String** |  | [optional] 
**OriginalName** | **String** |  | [optional] 
**Sha256Hash** | **String** |  | [optional] 
**UploadedBy** | **String** |  | [optional] 
**VersionNumber** | **Int32** | 1-based; ascending per attachment in upload order. | 

## Examples

- Prepare the resource
```powershell
$AttachmentVersion = Initialize-PSOpenAPIToolsAttachmentVersion  -AttachmentId null `
 -FileName null `
 -FileSize null `
 -MimeType null `
 -OriginalName null `
 -Sha256Hash null `
 -UploadedBy null `
 -VersionNumber null
```

- Convert the resource to JSON
```powershell
$AttachmentVersion | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

