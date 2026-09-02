# TimeEntryClockOut
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ClockOut** | **System.DateTime** |  | 
**Hours** | **String** | Optional manual hours; when absent, derived from clock_in..clock_out. | [optional] 

## Examples

- Prepare the resource
```powershell
$TimeEntryClockOut = Initialize-PSOpenAPIToolsTimeEntryClockOut  -ClockOut null `
 -Hours null
```

- Convert the resource to JSON
```powershell
$TimeEntryClockOut | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

