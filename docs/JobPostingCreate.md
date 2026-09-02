# JobPostingCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **String** |  | [optional] 
**Department** | **String** |  | [optional] 
**Description** | **String** | What the job is; markdown/HTML. | 
**EmploymentType** | [**EmploymentType**](EmploymentType.md) | full_time | part_time | contract | internship | temporary | [optional] 
**Location** | **String** |  | [optional] 
**Remote** | **Boolean** |  | 
**RequiredSkills** | [**AnyType**](.md) | List of required skill names (JSON array of strings). | 
**Requirements** | **String** | Structured profile of the required candidate (skills, experience). | [optional] 
**SalaryMax** | **Int32** |  | [optional] 
**SalaryMin** | **Int32** |  | [optional] 
**Status** | [**JobPostingStatus**](JobPostingStatus.md) | draft | published | closed | 
**Title** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$JobPostingCreate = Initialize-PSOpenAPIToolsJobPostingCreate  -Currency null `
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
$JobPostingCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

