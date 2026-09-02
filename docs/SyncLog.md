# SyncLog
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CompletedAt** | **System.DateTime** |  | [optional] 
**ConnectionId** | **String** |  | 
**ErrorMessage** | **String** |  | [optional] 
**ItemsFailed** | **Int32** |  | 
**ItemsSynced** | **Int32** |  | 
**LogId** | **String** |  | 
**Platform** | **String** |  | 
**StartedAt** | **System.DateTime** |  | 
**Status** | **String** |  | 
**SyncType** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$SyncLog = Initialize-PSOpenAPIToolsSyncLog  -CompletedAt null `
 -ConnectionId null `
 -ErrorMessage null `
 -ItemsFailed null `
 -ItemsSynced null `
 -LogId null `
 -Platform null `
 -StartedAt null `
 -Status null `
 -SyncType null
```

- Convert the resource to JSON
```powershell
$SyncLog | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

