# HrTrainingOverview
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssignedCount** | **Int64** |  | 
**Code** | **String** |  | 
**CompletedCount** | **Int64** |  | 
**OverdueCount** | **Int64** |  | 
**Title** | **String** |  | 
**TrainingId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$HrTrainingOverview = Initialize-PSOpenAPIToolsHrTrainingOverview  -AssignedCount null `
 -Code null `
 -CompletedCount null `
 -OverdueCount null `
 -Title null `
 -TrainingId null
```

- Convert the resource to JSON
```powershell
$HrTrainingOverview | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

