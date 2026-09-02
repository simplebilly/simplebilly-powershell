# PSOpenAPITools.PSOpenAPITools\Api.TicketMessageApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ListMessagesApi**](TicketMessageApi.md#Invoke-ListMessagesApi) | **GET** /api/v1/support/tickets/{ticket_id}/messages | 
[**Send-MessageApi**](TicketMessageApi.md#Send-MessageApi) | **POST** /api/v1/support/tickets/{ticket_id}/messages | 


<a id="Invoke-ListMessagesApi"></a>
# **Invoke-ListMessagesApi**
> TicketMessage[] Invoke-ListMessagesApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TicketId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TicketId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-ListMessagesApi -TicketId $TicketId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListMessagesApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TicketId** | **String**|  | 

### Return type

[**TicketMessage[]**](TicketMessage.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Send-MessageApi"></a>
# **Send-MessageApi**
> TicketMessage Send-MessageApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TicketId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SendMessageDto] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TicketId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$SendMessageDto = Initialize-SendMessageDto -Body "MyBody" -IsInternal $false # SendMessageDto | 

try {
    $Result = Send-MessageApi -TicketId $TicketId -SendMessageDto $SendMessageDto
} catch {
    Write-Host ("Exception occurred when calling Send-MessageApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TicketId** | **String**|  | 
 **SendMessageDto** | [**SendMessageDto**](SendMessageDto.md)|  | 

### Return type

[**TicketMessage**](TicketMessage.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

