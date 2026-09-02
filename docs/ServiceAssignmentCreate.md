# ServiceAssignmentCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EmployeeId** | **String** | References the employees entity. | [optional] 
**JobId** | **String** | References the service_jobs entity. | [optional] 
**Notes** | **String** |  | [optional] 
**ScheduledDate** | **System.DateTime** | Work day the assignment is scheduled for. | [optional] 
**ScheduledEnd** | **String** | Planned end time of the assignment. | [optional] 
**ScheduledStart** | **String** | Planned start time of the assignment. | [optional] 
**Status** | [**ServiceAssignmentStatus**](ServiceAssignmentStatus.md) | Assignment lifecycle status: &quot;&quot;planned&quot;&quot;, &quot;&quot;confirmed&quot;&quot;, &quot;&quot;en_route&quot;&quot;, &quot;&quot;in_progress&quot;&quot;, &quot;&quot;completed&quot;&quot; or &quot;&quot;cancelled&quot;&quot;. | [optional] 

## Examples

- Prepare the resource
```powershell
$ServiceAssignmentCreate = Initialize-PSOpenAPIToolsServiceAssignmentCreate  -EmployeeId null `
 -JobId null `
 -Notes null `
 -ScheduledDate null `
 -ScheduledEnd null `
 -ScheduledStart null `
 -Status null
```

- Convert the resource to JSON
```powershell
$ServiceAssignmentCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

