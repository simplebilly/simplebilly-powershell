# PostingCategoryCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountNumber** | **String** |  | [optional] 
**AccountNumberSkr03** | **String** |  | [optional] 
**AccountNumberSkr04** | **String** |  | [optional] 
**AccountNumberSkr49** | **String** |  | [optional] 
**CategoryType** | [**PostingCategoryType**](PostingCategoryType.md) |  | 
**CreatedAt** | **System.DateTime** |  | 
**DefaultVatRate** | **Int32** |  | 
**Description** | **String** |  | [optional] 
**EksCategory** | **String** |  | [optional] 
**EuVatLine** | **Int32** |  | [optional] 
**InputVatPercentage** | **String** |  | 
**IsActive** | **Boolean** |  | 
**IsSystem** | **Boolean** |  | 
**Name** | **String** |  | 
**SkrVersion** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 
**UserModifiedSkr03** | **Boolean** |  | 
**UserModifiedSkr04** | **Boolean** |  | 

## Examples

- Prepare the resource
```powershell
$PostingCategoryCreate = Initialize-PSOpenAPIToolsPostingCategoryCreate  -AccountNumber null `
 -AccountNumberSkr03 null `
 -AccountNumberSkr04 null `
 -AccountNumberSkr49 null `
 -CategoryType null `
 -CreatedAt null `
 -DefaultVatRate null `
 -Description null `
 -EksCategory null `
 -EuVatLine null `
 -InputVatPercentage null `
 -IsActive null `
 -IsSystem null `
 -Name null `
 -SkrVersion null `
 -UpdatedAt null `
 -UserModifiedSkr03 null `
 -UserModifiedSkr04 null
```

- Convert the resource to JSON
```powershell
$PostingCategoryCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

