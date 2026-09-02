# MarketplaceSyncLog
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CompletedAt** | **System.DateTime** |  | [optional] 
**ConnectionId** | **String** | References the marketplace connection entity. | 
**ErrorMessage** | **String** |  | [optional] 
**ItemsFailed** | **Int32** |  | 
**ItemsSynced** | **Int32** |  | 
**Platform** | **String** |  | 
**StartedAt** | **System.DateTime** |  | 
**Status** | [**SyncLogStatus**](SyncLogStatus.md) |  | 
**SyncType** | [**SyncType**](SyncType.md) |  | 

## Examples

- Prepare the resource
```powershell
$MarketplaceSyncLog = Initialize-PSOpenAPIToolsMarketplaceSyncLog  -CompletedAt null `
 -ConnectionId null `
 -ErrorMessage null `
 -ItemsFailed null `
 -ItemsSynced null `
 -Platform null `
 -StartedAt null `
 -Status null `
 -SyncType null
```

- Convert the resource to JSON
```powershell
$MarketplaceSyncLog | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

