# AiConfigDto
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AutoReply** | **Boolean** |  | [optional] 
**MaxToolCalls** | **Int32** |  | [optional] 
**Model** | **String** |  | 
**Name** | **String** |  | 
**Provider** | **String** |  | 
**SystemPrompt** | **String** |  | [optional] 
**TriggerOn** | **String[]** |  | [optional] 

## Examples

- Prepare the resource
```powershell
$AiConfigDto = Initialize-PSOpenAPIToolsAiConfigDto  -AutoReply null `
 -MaxToolCalls null `
 -Model null `
 -Name null `
 -Provider null `
 -SystemPrompt null `
 -TriggerOn null
```

- Convert the resource to JSON
```powershell
$AiConfigDto | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

