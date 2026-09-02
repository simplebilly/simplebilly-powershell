# MyTrainingItem
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AssignmentId** | **String** |  | 
**CertificateId** | **String** |  | [optional] 
**Code** | **String** |  | 
**Description** | **String** |  | [optional] 
**DueDate** | **System.DateTime** |  | [optional] 
**LastScore** | **Int32** |  | [optional] 
**PassScore** | **Int32** |  | 
**Passed** | **Boolean** |  | [optional] 
**Status** | [**AssignmentStatus**](AssignmentStatus.md) |  | 
**Title** | **String** |  | 
**TrainingId** | **String** |  | 
**ValidUntil** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$MyTrainingItem = Initialize-PSOpenAPIToolsMyTrainingItem  -AssignmentId null `
 -CertificateId null `
 -Code null `
 -Description null `
 -DueDate null `
 -LastScore null `
 -PassScore null `
 -Passed null `
 -Status null `
 -Title null `
 -TrainingId null `
 -ValidUntil null
```

- Convert the resource to JSON
```powershell
$MyTrainingItem | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

