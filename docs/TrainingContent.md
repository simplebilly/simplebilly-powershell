# TrainingContent
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Code** | **String** |  | 
**Contact** | [**ContactInfo**](ContactInfo.md) |  | 
**PassScore** | **Int32** |  | 
**Quiz** | [**QuizQuestion[]**](QuizQuestion.md) |  | 
**Sections** | [**Section[]**](Section.md) |  | 
**Title** | **String** |  | 
**TitleEn** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$TrainingContent = Initialize-PSOpenAPIToolsTrainingContent  -Code null `
 -Contact null `
 -PassScore null `
 -Quiz null `
 -Sections null `
 -Title null `
 -TitleEn null
```

- Convert the resource to JSON
```powershell
$TrainingContent | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

