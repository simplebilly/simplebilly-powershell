# ProductCategoryUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Description** | **String** |  | [optional] 
**Name** | **String** |  | [optional] 
**ParentCategoryId** | **String** | References the category entity. | [optional] 
**SortOrder** | **Int32** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$ProductCategoryUpdate = Initialize-PSOpenAPIToolsProductCategoryUpdate  -Description null `
 -Name null `
 -ParentCategoryId null `
 -SortOrder null
```

- Convert the resource to JSON
```powershell
$ProductCategoryUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

