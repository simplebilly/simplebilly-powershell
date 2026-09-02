# ApplicationStatusDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**PostingId** | **String** |  | [optional] 
**Status** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$ApplicationStatusDto = Initialize-PSOpenAPIToolsApplicationStatusDto  -PostingId null `
 -Status null
```

- Convert the resource to JSON
```powershell
$ApplicationStatusDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

