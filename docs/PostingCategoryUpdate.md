# PostingCategoryUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountNumber** | **String** |  | [optional] 
**AccountNumberSkr03** | **String** |  | [optional] 
**AccountNumberSkr04** | **String** |  | [optional] 
**AccountNumberSkr49** | **String** |  | [optional] 
**CategoryType** | [**PostingCategoryType**](PostingCategoryType.md) |  | [optional] 
**CreatedAt** | **System.DateTime** |  | [optional] 
**DefaultVatRate** | **Int32** |  | [optional] 
**Description** | **String** |  | [optional] 
**EksCategory** | **String** |  | [optional] 
**EuVatLine** | **Int32** |  | [optional] 
**InputVatPercentage** | **String** |  | [optional] 
**IsActive** | **Boolean** |  | [optional] 
**IsSystem** | **Boolean** |  | [optional] 
**Name** | **String** |  | [optional] 
**SkrVersion** | **String** |  | [optional] 
**UpdatedAt** | **System.DateTime** |  | [optional] 
**UserModifiedSkr03** | **Boolean** |  | [optional] 
**UserModifiedSkr04** | **Boolean** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$PostingCategoryUpdate = Initialize-PSOpenAPIToolsPostingCategoryUpdate  -AccountNumber null `
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
$PostingCategoryUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

