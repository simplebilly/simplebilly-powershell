# AiWorkerConfig
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AutoReply** | **Boolean** |  | 
**CreatedAt** | **System.DateTime** |  | 
**Id** | **String** |  | 
**IsActive** | **Boolean** |  | 
**MaxToolCalls** | **Int32** |  | 
**Model** | **String** |  | 
**Name** | **String** |  | 
**Provider** | **String** |  | 
**SystemPrompt** | **String** |  | 
**TenantId** | **String** |  | 
**TriggerOn** | **String[]** |  | 
**UpdatedAt** | **System.DateTime** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$AiWorkerConfig = Initialize-PSOpenAPIToolsAiWorkerConfig  -AutoReply null `
 -CreatedAt null `
 -Id null `
 -IsActive null `
 -MaxToolCalls null `
 -Model null `
 -Name null `
 -Provider null `
 -SystemPrompt null `
 -TenantId null `
 -TriggerOn null `
 -UpdatedAt null
```

- Convert the resource to JSON
```powershell
$AiWorkerConfig | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

