# QuizQuestion
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **String** |  | 
**Options** | **String[]** |  | 
**OptionsEn** | **String[]** |  | 
**Question** | **String** |  | 
**QuestionEn** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$QuizQuestion = Initialize-PSOpenAPIToolsQuizQuestion  -Id null `
 -Options null `
 -OptionsEn null `
 -Question null `
 -QuestionEn null
```

- Convert the resource to JSON
```powershell
$QuizQuestion | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

