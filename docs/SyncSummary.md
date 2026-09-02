# SyncSummary
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ErrorMessage** | **String** |  | [optional] 
**ItemsFailed** | **Int32** |  | [optional] 
**ItemsSynced** | **Int32** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$SyncSummary = Initialize-PSOpenAPIToolsSyncSummary  -ErrorMessage null `
 -ItemsFailed null `
 -ItemsSynced null
```

- Convert the resource to JSON
```powershell
$SyncSummary | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

