# PSOpenAPITools.PSOpenAPITools\Api.AiApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-AiSuggestApi**](AiApi.md#Invoke-AiSuggestApi) | **POST** /api/v1/support/ai/suggest | 
[**New-WorkerApi**](AiApi.md#New-WorkerApi) | **POST** /api/v1/support/ai/workers | 
[**Invoke-ListWorkersApi**](AiApi.md#Invoke-ListWorkersApi) | **GET** /api/v1/support/ai/workers | 
[**Invoke-RunWorkerApi**](AiApi.md#Invoke-RunWorkerApi) | **POST** /api/v1/support/ai/workers/{worker_id}/run | 


<a id="Invoke-AiSuggestApi"></a>
# **Invoke-AiSuggestApi**
> AiSuggestion Invoke-AiSuggestApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AiSuggestionRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AiSuggestionRequest = Initialize-AiSuggestionRequest -Instructions "MyInstructions" -MessageBody "MyMessageBody" -TicketId "MyTicketId" # AiSuggestionRequest | 

try {
    $Result = Invoke-AiSuggestApi -AiSuggestionRequest $AiSuggestionRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-AiSuggestApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AiSuggestionRequest** | [**AiSuggestionRequest**](AiSuggestionRequest.md)|  | 

### Return type

[**AiSuggestion**](AiSuggestion.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-WorkerApi"></a>
# **New-WorkerApi**
> AiWorkerConfig New-WorkerApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AiConfigDto] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AiConfigDto = Initialize-AiConfigDto -AutoReply $false -MaxToolCalls 0 -Model "MyModel" -Name "MyName" -Provider "MyProvider" -SystemPrompt "MySystemPrompt" -TriggerOn "MyTriggerOn" # AiConfigDto | 

try {
    $Result = New-WorkerApi -AiConfigDto $AiConfigDto
} catch {
    Write-Host ("Exception occurred when calling New-WorkerApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AiConfigDto** | [**AiConfigDto**](AiConfigDto.md)|  | 

### Return type

[**AiWorkerConfig**](AiWorkerConfig.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListWorkersApi"></a>
# **Invoke-ListWorkersApi**
> AiWorkerConfig[] Invoke-ListWorkersApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListWorkersApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListWorkersApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AiWorkerConfig[]**](AiWorkerConfig.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-RunWorkerApi"></a>
# **Invoke-RunWorkerApi**
> AiSuggestion Invoke-RunWorkerApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WorkerId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AiSuggestionRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WorkerId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$AiSuggestionRequest = Initialize-AiSuggestionRequest -Instructions "MyInstructions" -MessageBody "MyMessageBody" -TicketId "MyTicketId" # AiSuggestionRequest | 

try {
    $Result = Invoke-RunWorkerApi -WorkerId $WorkerId -AiSuggestionRequest $AiSuggestionRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-RunWorkerApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WorkerId** | **String**|  | 
 **AiSuggestionRequest** | [**AiSuggestionRequest**](AiSuggestionRequest.md)|  | 

### Return type

[**AiSuggestion**](AiSuggestion.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

