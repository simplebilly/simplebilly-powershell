# DatevExportResponse
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**BookingCount** | **Int32** |  | 
**CsvContent** | **String** |  | 
**Filename** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$DatevExportResponse = Initialize-PSOpenAPIToolsDatevExportResponse  -BookingCount null `
 -CsvContent null `
 -Filename null
```

- Convert the resource to JSON
```powershell
$DatevExportResponse | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

