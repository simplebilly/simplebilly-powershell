# SalesVolumeReport
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**GrandTotal** | **String** |  | 
**Items** | [**SalesVolumeItem[]**](SalesVolumeItem.md) |  | 
**TotalCount** | **Int64** |  | 

## Examples

- Prepare the resource
```powershell
$SalesVolumeReport = Initialize-PSOpenAPIToolsSalesVolumeReport  -GrandTotal null `
 -Items null `
 -TotalCount null
```

- Convert the resource to JSON
```powershell
$SalesVolumeReport | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

