# JobPostingUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **String** |  | [optional] 
**Department** | **String** |  | [optional] 
**Description** | **String** | What the job is; markdown/HTML. | [optional] 
**EmploymentType** | [**EmploymentType**](EmploymentType.md) | full_time | part_time | contract | internship | temporary | [optional] 
**Location** | **String** |  | [optional] 
**Remote** | **Boolean** |  | [optional] 
**RequiredSkills** | [**AnyType**](.md) | List of required skill names (JSON array of strings). | [optional] 
**Requirements** | **String** | Structured profile of the required candidate (skills, experience). | [optional] 
**SalaryMax** | **Int32** |  | [optional] 
**SalaryMin** | **Int32** |  | [optional] 
**Status** | [**JobPostingStatus**](JobPostingStatus.md) | draft | published | closed | [optional] 
**Title** | **String** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$JobPostingUpdate = Initialize-PSOpenAPIToolsJobPostingUpdate  -Currency null `
 -Department null `
 -Description null `
 -EmploymentType null `
 -Location null `
 -Remote null `
 -RequiredSkills null `
 -Requirements null `
 -SalaryMax null `
 -SalaryMin null `
 -Status null `
 -Title null
```

- Convert the resource to JSON
```powershell
$JobPostingUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

