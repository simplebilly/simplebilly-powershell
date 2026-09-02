# JobPostingFilter
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Page** | **Int32** |  | [optional] 
**PageSize** | **Int32** |  | [optional] 
**Status** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$JobPostingFilter = Initialize-PSOpenAPIToolsJobPostingFilter  -Page null `
 -PageSize null `
 -Status null
```

- Convert the resource to JSON
```powershell
$JobPostingFilter | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

