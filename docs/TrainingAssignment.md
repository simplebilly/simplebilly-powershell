# TrainingAssignment
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssignedBy** | **String** |  | [optional] 
**CreatedAt** | **System.DateTime** |  | [optional] 
**DeletedAt** | **System.DateTime** |  | [optional] 
**DueDate** | **System.DateTime** |  | [optional] 
**EmployeeId** | **String** |  | [optional] 
**Id** | **String** |  | [optional] 
**Notes** | **String** |  | [optional] 
**Status** | [**AssignmentStatus**](AssignmentStatus.md) |  | [optional] 
**TenantId** | **String** |  | [optional] 
**TrainingId** | **String** |  | [optional] 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$TrainingAssignment = Initialize-PSOpenAPIToolsTrainingAssignment  -AssignedBy null `
 -CreatedAt null `
 -DeletedAt null `
 -DueDate null `
 -EmployeeId null `
 -Id null `
 -Notes null `
 -Status null `
 -TenantId null `
 -TrainingId null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$TrainingAssignment | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

