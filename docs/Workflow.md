# Workflow
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Actions** | [**AnyType**](.md) |  | [optional] 
**Enabled** | **Boolean** |  | [optional] 
**Name** | **String** |  | 
**TriggerEvent** | **String** | Event that triggers the workflow, e.g. &#x60;order.paid&#x60;, &#x60;order.shipped&#x60;. | 

## Examples

- Prepare the resource
```powershell
$Workflow = Initialize-PSOpenAPIToolsWorkflow  -Actions null `
 -Enabled null `
 -Name null `
 -TriggerEvent null
```

- Convert the resource to JSON
```powershell
$Workflow | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

