# NewVersionRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FileName** | **String** | Storage key of the already-uploaded bytes. | 
**FileSize** | **Int64** |  | [optional] 
**MimeType** | **String** |  | [optional] 
**OriginalName** | **String** |  | [optional] 
**Sha256Hash** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$NewVersionRequest = Initialize-PSOpenAPIToolsNewVersionRequest  -FileName null `
 -FileSize null `
 -MimeType null `
 -OriginalName null `
 -Sha256Hash null
```

- Convert the resource to JSON
```powershell
$NewVersionRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

