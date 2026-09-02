# Automation
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AutomationKey** | **String** |  | 
**Config** | [**AnyType**](.md) |  | 
**CreatedAt** | **System.DateTime** |  | 
**Enabled** | **Boolean** |  | 
**LastRunAt** | **System.DateTime** |  | [optional] 
**NextRunAt** | **System.DateTime** |  | [optional] 
**TenantId** | **String** |  | 
**UpdatedAt** | **System.DateTime** |  | 

## Examples

- Prepare the resource
```powershell
$Automation = Initialize-PSOpenAPIToolsAutomation  -AutomationKey null `
 -Config null `
 -CreatedAt null `
 -Enabled null `
 -LastRunAt null `
 -NextRunAt null `
 -TenantId null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$Automation | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

