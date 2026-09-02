# PSOpenAPITools.PSOpenAPITools\Api.SupportTicketApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-TicketApi**](SupportTicketApi.md#New-TicketApi) | **POST** /api/v1/support/tickets | 
[**Invoke-DeleteTicketApi**](SupportTicketApi.md#Invoke-DeleteTicketApi) | **DELETE** /api/v1/support/tickets/{ticket_id} | 
[**Get-TicketApi**](SupportTicketApi.md#Get-TicketApi) | **GET** /api/v1/support/tickets/{ticket_id} | 
[**Invoke-ListTicketsApi**](SupportTicketApi.md#Invoke-ListTicketsApi) | **GET** /api/v1/support/tickets | 
[**Update-TicketApi**](SupportTicketApi.md#Update-TicketApi) | **PUT** /api/v1/support/tickets/{ticket_id} | 


<a id="New-TicketApi"></a>
# **New-TicketApi**
> SupportTicket New-TicketApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreateTicketRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CreateTicketRequest = Initialize-CreateTicketRequest -ChannelId "MyChannelId" -ChannelType "MyChannelType" -CustomerEmail "MyCustomerEmail" -CustomerId "MyCustomerId" -CustomerName "MyCustomerName" -ExternalId "MyExternalId" -MessageBody "MyMessageBody" -OrderRef "MyOrderRef" -Subject "MySubject" # CreateTicketRequest | 

try {
    $Result = New-TicketApi -CreateTicketRequest $CreateTicketRequest
} catch {
    Write-Host ("Exception occurred when calling New-TicketApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateTicketRequest** | [**CreateTicketRequest**](CreateTicketRequest.md)|  | 

### Return type

[**SupportTicket**](SupportTicket.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteTicketApi"></a>
# **Invoke-DeleteTicketApi**
> void Invoke-DeleteTicketApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TicketId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TicketId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteTicketApi -TicketId $TicketId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteTicketApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TicketId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-TicketApi"></a>
# **Get-TicketApi**
> SupportTicket Get-TicketApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TicketId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TicketId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-TicketApi -TicketId $TicketId
} catch {
    Write-Host ("Exception occurred when calling Get-TicketApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TicketId** | **String**|  | 

### Return type

[**SupportTicket**](SupportTicket.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListTicketsApi"></a>
# **Invoke-ListTicketsApi**
> SupportTicket[] Invoke-ListTicketsApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Priority] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AssignedTo] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ChannelType] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Status = "MyStatus" # String |  (optional)
$Priority = "MyPriority" # String |  (optional)
$AssignedTo = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String |  (optional)
$ChannelType = "MyChannelType" # String |  (optional)
$CustomerId = "MyCustomerId" # String |  (optional)
$Search = "MySearch" # String |  (optional)
$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)

try {
    $Result = Invoke-ListTicketsApi -Status $Status -Priority $Priority -AssignedTo $AssignedTo -ChannelType $ChannelType -CustomerId $CustomerId -Search $Search -Page $Page -PageSize $PageSize
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListTicketsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Status** | **String**|  | [optional] 
 **Priority** | **String**|  | [optional] 
 **AssignedTo** | **String**|  | [optional] 
 **ChannelType** | **String**|  | [optional] 
 **CustomerId** | **String**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 

### Return type

[**SupportTicket[]**](SupportTicket.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-TicketApi"></a>
# **Update-TicketApi**
> SupportTicket Update-TicketApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TicketId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupportTicketUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TicketId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$SupportTicketUpdate = Initialize-SupportTicketUpdate -AssignedTo "MyAssignedTo" -ChannelId "MyChannelId" -ChannelType "email" -ClosedAt (Get-Date) -CreatedAt (Get-Date) -CustomerEmail "MyCustomerEmail" -CustomerId "MyCustomerId" -CustomerName "MyCustomerName" -ExternalId "MyExternalId" -FirstMessageAt (Get-Date) -LastMessageAt (Get-Date) -LeadId "MyLeadId" -MessageCount 0 -OrderRef "MyOrderRef" -Priority "normal" -Resolution "MyResolution" -Status "open" -Subject "MySubject" -Tags  -TenantId "MyTenantId" -UpdatedAt (Get-Date) # SupportTicketUpdate | 

try {
    $Result = Update-TicketApi -TicketId $TicketId -SupportTicketUpdate $SupportTicketUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-TicketApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TicketId** | **String**|  | 
 **SupportTicketUpdate** | [**SupportTicketUpdate**](SupportTicketUpdate.md)|  | 

### Return type

[**SupportTicket**](SupportTicket.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

