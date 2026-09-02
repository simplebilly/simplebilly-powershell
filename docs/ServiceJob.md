# ServiceJob
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Address** | **String** | Street + zip + city of the job location. | [optional] 
**CustomerEmail** | **String** | Customer email for email notifications. | [optional] 
**CustomerId** | **String** | References the customer entity. | [optional] 
**CustomerName** | **String** | Denormalized customer name for quick display. | [optional] 
**CustomerPhone** | **String** | Customer phone for SMS notifications later. | [optional] 
**Description** | **String** | What work needs to be done. | [optional] 
**EstimatedDurationMinutes** | **Int32** | Estimated time for the job in minutes. | [optional] 
**Lat** | **Double** | Latitude for map display (OpenStreetMap). | [optional] 
**Lng** | **Double** | Longitude for map display (OpenStreetMap). | [optional] 
**Notes** | **String** |  | [optional] 
**Status** | [**ServiceJobStatus**](ServiceJobStatus.md) | Dispatch status: &quot;&quot;pending&quot;&quot;, &quot;&quot;assigned&quot;&quot;, &quot;&quot;en_route&quot;&quot;, &quot;&quot;in_progress&quot;&quot;, &quot;&quot;completed&quot;&quot;, &quot;&quot;cancelled&quot;&quot;. | [optional] 

## Examples

- Prepare the resource
```powershell
$ServiceJob = Initialize-PSOpenAPIToolsServiceJob  -Address null `
 -CustomerEmail null `
 -CustomerId null `
 -CustomerName null `
 -CustomerPhone null `
 -Description null `
 -EstimatedDurationMinutes null `
 -Lat null `
 -Lng null `
 -Notes null `
 -Status null
```

- Convert the resource to JSON
```powershell
$ServiceJob | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

