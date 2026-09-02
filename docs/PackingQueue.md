# PackingQueue
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Items** | [**PackingQueueItem[]**](PackingQueueItem.md) |  | 
**Page** | **Int32** |  | 
**PageSize** | **Int32** |  | 
**TotalCount** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$PackingQueue = Initialize-PSOpenAPIToolsPackingQueue  -Items null `
 -Page null `
 -PageSize null `
 -TotalCount null
```

- Convert the resource to JSON
```powershell
$PackingQueue | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

