# RecurringTemplate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**CreatedAt** | **String** |  | [readonly] 
**DeletedAt** | **String** |  | [optional] [readonly] 
**EndDate** | **System.DateTime** |  | [optional] 
**ExecutionInterval** | **String** |  | 
**ExecutionStatus** | **String** |  | 
**Finalize** | **Boolean** |  | 
**LastExecutedAt** | **System.DateTime** |  | [optional] 
**Name** | **String** |  | 
**NextExecutionAt** | **System.DateTime** |  | [optional] 
**StartDate** | **System.DateTime** |  | 
**TemplateId** | **String** |  | 
**TemplateType** | **String** |  | 
**UpdatedAt** | **String** |  | [optional] [readonly] 
**VoucherData** | [**AnyType**](.md) |  | 

## Examples

- Prepare the resource
```powershell
$RecurringTemplate = Initialize-PSOpenAPIToolsRecurringTemplate  -CreatedAt null `
 -DeletedAt null `
 -EndDate null `
 -ExecutionInterval null `
 -ExecutionStatus null `
 -Finalize null `
 -LastExecutedAt null `
 -Name null `
 -NextExecutionAt null `
 -StartDate null `
 -TemplateId null `
 -TemplateType null `
 -UpdatedAt null `
 -VoucherData null
```

- Convert the resource to JSON
```powershell
$RecurringTemplate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

