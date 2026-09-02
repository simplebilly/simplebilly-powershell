# OssReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Dependencies** | [**OssDependency[]**](OssDependency.md) |  | 
**TotalCount** | **Int32** |  | 

## Examples

- Prepare the resource
```powershell
$OssReport = Initialize-PSOpenAPIToolsOssReport  -Dependencies null `
 -TotalCount null
```

- Convert the resource to JSON
```powershell
$OssReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

