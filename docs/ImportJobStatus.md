# ImportJobStatus
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**VarError** | **String** | Set only when the job failed. | [optional] 
**JobId** | **String** |  | 
**Processed** | **Int64** |  | 
**Progress** | **Int32** | 0–100 | 
**Provider** | **String** | Which competitor the import came from (lexoffice | billbee); the frontend uses it to label the job. Absent for legacy jobs. | [optional] 
**Stage** | **String** | queued | fetching | downloading | importing | done | 
**Status** | **String** | pending | running | done | failed | 
**Total** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$ImportJobStatus = Initialize-PSOpenAPIToolsImportJobStatus  -VarError null `
 -JobId null `
 -Processed null `
 -Progress null `
 -Provider null `
 -Stage null `
 -Status null `
 -Total null
```

- Convert the resource to JSON
```powershell
$ImportJobStatus | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

