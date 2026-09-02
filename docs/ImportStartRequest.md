# ImportStartRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ApiKey** | **String** |  | 
**Provider** | **String** |  | 
**Years** | **Int32[]** |  | 

## Examples

- Prepare the resource
```powershell
$ImportStartRequest = Initialize-PSOpenAPIToolsImportStartRequest  -ApiKey null `
 -Provider null `
 -Years null
```

- Convert the resource to JSON
```powershell
$ImportStartRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

