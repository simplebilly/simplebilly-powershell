# TrainingAssignmentUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssignedBy** | **String** |  | [optional] 
**DueDate** | **System.DateTime** |  | [optional] 
**EmployeeId** | **String** |  | [optional] 
**Notes** | **String** |  | [optional] 
**Status** | [**AssignmentStatus**](AssignmentStatus.md) |  | [optional] 
**TrainingId** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$TrainingAssignmentUpdate = Initialize-PSOpenAPIToolsTrainingAssignmentUpdate  -AssignedBy null `
 -DueDate null `
 -EmployeeId null `
 -Notes null `
 -Status null `
 -TrainingId null
```

- Convert the resource to JSON
```powershell
$TrainingAssignmentUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

