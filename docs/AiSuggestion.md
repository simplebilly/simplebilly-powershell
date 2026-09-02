# AiSuggestion
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Confidence** | **Double** |  | 
**Reasoning** | **String** |  | 
**SuggestedPriority** | **String** |  | [optional] 
**SuggestedReply** | **String** |  | 
**SuggestedStatus** | **String** |  | [optional] 
**ToolCalls** | **String[]** |  | 

## Examples

- Prepare the resource
```powershell
$AiSuggestion = Initialize-PSOpenAPIToolsAiSuggestion  -Confidence null `
 -Reasoning null `
 -SuggestedPriority null `
 -SuggestedReply null `
 -SuggestedStatus null `
 -ToolCalls null
```

- Convert the resource to JSON
```powershell
$AiSuggestion | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

