# RecurringTemplateCreate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EndDate** | **System.DateTime** |  | [optional] 
**ExecutionInterval** | **String** |  | 
**ExecutionStatus** | [**ExecutionStatus**](ExecutionStatus.md) |  | 
**Finalize** | **Boolean** |  | [optional] 
**LastExecutedAt** | **System.DateTime** |  | [optional] 
**Name** | **String** |  | 
**NextExecutionAt** | **System.DateTime** |  | [optional] 
**StartDate** | **System.DateTime** |  | 
**TemplateType** | [**RecurringTemplateType**](RecurringTemplateType.md) |  | 
**VoucherData** | [**AnyType**](.md) |  | [optional] 

## Examples

- Prepare the resource
```powershell
$RecurringTemplateCreate = Initialize-PSOpenAPIToolsRecurringTemplateCreate  -EndDate null `
 -ExecutionInterval null `
 -ExecutionStatus null `
 -Finalize null `
 -LastExecutedAt null `
 -Name null `
 -NextExecutionAt null `
 -StartDate null `
 -TemplateType null `
 -VoucherData null
```

- Convert the resource to JSON
```powershell
$RecurringTemplateCreate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

