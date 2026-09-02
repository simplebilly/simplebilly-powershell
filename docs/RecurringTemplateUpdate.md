# RecurringTemplateUpdate
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EndDate** | **System.DateTime** |  | [optional] 
**ExecutionInterval** | **String** |  | [optional] 
**ExecutionStatus** | [**ExecutionStatus**](ExecutionStatus.md) |  | [optional] 
**Finalize** | **Boolean** |  | [optional] 
**LastExecutedAt** | **System.DateTime** |  | [optional] 
**Name** | **String** |  | [optional] 
**NextExecutionAt** | **System.DateTime** |  | [optional] 
**StartDate** | **System.DateTime** |  | [optional] 
**TemplateType** | [**RecurringTemplateType**](RecurringTemplateType.md) |  | [optional] 
**VoucherData** | [**AnyType**](.md) |  | [optional] 

## Examples

- Prepare the resource
```powershell
$RecurringTemplateUpdate = Initialize-PSOpenAPIToolsRecurringTemplateUpdate  -EndDate null `
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
$RecurringTemplateUpdate | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

