# PublicPosting
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Currency** | **String** |  | [optional] 
**Description** | **String** |  | 
**EmploymentType** | **String** |  | [optional] 
**Id** | **String** |  | 
**Location** | **String** |  | [optional] 
**Remote** | **Boolean** |  | 
**RequiredSkills** | **String[]** |  | 
**Requirements** | **String** |  | [optional] 
**SalaryMax** | **Int32** |  | [optional] 
**SalaryMin** | **Int32** |  | [optional] 
**Title** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PublicPosting = Initialize-PSOpenAPIToolsPublicPosting  -Currency null `
 -Description null `
 -EmploymentType null `
 -Id null `
 -Location null `
 -Remote null `
 -RequiredSkills null `
 -Requirements null `
 -SalaryMax null `
 -SalaryMin null `
 -Title null
```

- Convert the resource to JSON
```powershell
$PublicPosting | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

