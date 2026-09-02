# QuartileBand
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**FemaleSharePct** | **Double** |  | 
**HourlyMedian** | **String** |  | 
**MaleSharePct** | **Double** |  | 
**Quartile** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$QuartileBand = Initialize-PSOpenAPIToolsQuartileBand  -FemaleSharePct null `
 -HourlyMedian null `
 -MaleSharePct null `
 -Quartile null
```

- Convert the resource to JSON
```powershell
$QuartileBand | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

