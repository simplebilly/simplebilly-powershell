# SubmitResultDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Answers** | **Int32[]** | Selected answer indices (required for scored builtin trainings). | 
**AssignmentId** | **String** |  | [optional] 
**Score** | **Int32** | Score 0–100. Only trusted for plugin trainings without server-side scoring; builtin trainings are always re-scored from &#x60;answers&#x60;. | 
**TrainingCode** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$SubmitResultDto = Initialize-PSOpenAPIToolsSubmitResultDto  -Answers null `
 -AssignmentId null `
 -Score null `
 -TrainingCode null
```

- Convert the resource to JSON
```powershell
$SubmitResultDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

