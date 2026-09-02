# ApplicationFilter
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Page** | **Int32** |  | [optional] 
**PageSize** | **Int32** |  | [optional] 
**PostingId** | **String** |  | [optional] 
**Status** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ApplicationFilter = Initialize-PSOpenAPIToolsApplicationFilter  -Page null `
 -PageSize null `
 -PostingId null `
 -Status null
```

- Convert the resource to JSON
```powershell
$ApplicationFilter | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

