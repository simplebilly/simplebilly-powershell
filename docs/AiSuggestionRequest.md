# AiSuggestionRequest
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Instructions** | **String** |  | [optional] 
**MessageBody** | **String** |  | [optional] 
**TicketId** | **String** |  | 

## Examples

- Prepare the resource
```powershell
$AiSuggestionRequest = Initialize-PSOpenAPIToolsAiSuggestionRequest  -Instructions null `
 -MessageBody null `
 -TicketId null
```

- Convert the resource to JSON
```powershell
$AiSuggestionRequest | ConvertTo-JSON
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

