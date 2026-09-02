# PostingCategory
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountNumber** | **String** |  | [optional] 
**AccountNumberSkr03** | **String** |  | [optional] 
**AccountNumberSkr04** | **String** |  | [optional] 
**AccountNumberSkr49** | **String** |  | [optional] 
**CategoryId** | **String** |  | 
**DefaultVatRate** | **Int32** |  | 
**Description** | **String** |  | [optional] 
**EksCategory** | **String** |  | [optional] 
**IsActive** | **Boolean** |  | 
**IsSystem** | **Boolean** |  | 
**Name** | **String** |  | 
**SkrVersion** | **String** |  | 
**Type** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$PostingCategory = Initialize-PSOpenAPIToolsPostingCategory  -AccountNumber null `
 -AccountNumberSkr03 null `
 -AccountNumberSkr04 null `
 -AccountNumberSkr49 null `
 -CategoryId null `
 -DefaultVatRate null `
 -Description null `
 -EksCategory null `
 -IsActive null `
 -IsSystem null `
 -Name null `
 -SkrVersion null `
 -Type null
```

- Convert the resource to JSON
```powershell
$PostingCategory | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

