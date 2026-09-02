# DatevImportResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Count** | **Int32** |  | 
**Filename** | **String** |  | 
**Rows** | [**DatevImportRow[]**](DatevImportRow.md) |  | 

## Examples

- Prepare the resource
```powershell
$DatevImportResponse = Initialize-PSOpenAPIToolsDatevImportResponse  -Count null `
 -Filename null `
 -Rows null
```

- Convert the resource to JSON
```powershell
$DatevImportResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

