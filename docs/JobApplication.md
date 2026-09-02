# JobApplication
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CvFile** | **String** | Relative path of the stored CV file under the upload dir. | [optional] 
**CvText** | **String** | Extracted CV text, used for match-scoring. | [optional] 
**Email** | **String** |  | [optional] 
**MatchReason** | **String** |  | [optional] 
**MatchScore** | **Int32** | 0-100 LLM match score against the posting&#39;s required profile. | [optional] 
**Name** | **String** |  | [optional] 
**Phone** | **String** |  | [optional] 
**PostingId** | **String** | References the job_posting entity. | [optional] 
**Source** | **String** | website | email | board | 
**Status** | [**ApplicationStatus**](ApplicationStatus.md) | new | reviewing | interview | hired | rejected | 

## Examples

- Prepare the resource
```powershell
$JobApplication = Initialize-PSOpenAPIToolsJobApplication  -CvFile null `
 -CvText null `
 -Email null `
 -MatchReason null `
 -MatchScore null `
 -Name null `
 -Phone null `
 -PostingId null `
 -Source null `
 -Status null
```

- Convert the resource to JSON
```powershell
$JobApplication | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

