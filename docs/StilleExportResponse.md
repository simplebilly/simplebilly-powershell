# StilleExportResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CsvContent** | **String** |  | 
**Filename** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$StilleExportResponse = Initialize-PSOpenAPIToolsStilleExportResponse  -CsvContent null `
 -Filename null
```

- Convert the resource to JSON
```powershell
$StilleExportResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

