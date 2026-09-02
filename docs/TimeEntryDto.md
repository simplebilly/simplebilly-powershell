# TimeEntryDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ClockIn** | **System.DateTime** |  | [optional] 
**ClockOut** | **System.DateTime** |  | [optional] 
**CreatedAt** | **System.DateTime** |  | 
**Date** | **System.DateTime** |  | 
**EmployeeId** | **String** |  | 
**Hours** | **String** |  | [optional] 
**Notes** | **String** |  | [optional] 
**TimeEntryId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$TimeEntryDto = Initialize-PSOpenAPIToolsTimeEntryDto  -ClockIn null `
 -ClockOut null `
 -CreatedAt null `
 -Date null `
 -EmployeeId null `
 -Hours null `
 -Notes null `
 -TimeEntryId null
```

- Convert the resource to JSON
```powershell
$TimeEntryDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

