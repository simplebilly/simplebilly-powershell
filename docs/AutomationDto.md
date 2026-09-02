# AutomationDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AutomationKey** | **String** |  | 
**Config** | [**AnyType**](.md) |  | 
**DefaultDay** | **Int32** |  | [optional] 
**Description** | **String** |  | 
**Enabled** | **Boolean** |  | 
**Kind** | **String** |  | 
**LastRunAt** | **System.DateTime** |  | [optional] 
**NextRunAt** | **System.DateTime** |  | [optional] 
**ScheduleKind** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$AutomationDto = Initialize-PSOpenAPIToolsAutomationDto  -AutomationKey null `
 -Config null `
 -DefaultDay null `
 -Description null `
 -Enabled null `
 -Kind null `
 -LastRunAt null `
 -NextRunAt null `
 -ScheduleKind null
```

- Convert the resource to JSON
```powershell
$AutomationDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

