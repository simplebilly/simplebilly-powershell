# PSOpenAPITools.PSOpenAPITools\Api.EventSubscriptionApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-EventSubscription**](EventSubscriptionApi.md#New-EventSubscription) | **POST** /api/v1/event-subscriptions | 
[**Invoke-DeleteEventSubscription**](EventSubscriptionApi.md#Invoke-DeleteEventSubscription) | **DELETE** /api/v1/event-subscriptions/{subscription_id} | 
[**Invoke-ListEventSubscriptions**](EventSubscriptionApi.md#Invoke-ListEventSubscriptions) | **GET** /api/v1/event-subscriptions/ | 


<a id="New-EventSubscription"></a>
# **New-EventSubscription**
> EventSubscription New-EventSubscription<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = New-EventSubscription -Body $Body
} catch {
    Write-Host ("Exception occurred when calling New-EventSubscription: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**EventSubscription**](EventSubscription.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteEventSubscription"></a>
# **Invoke-DeleteEventSubscription**
> void Invoke-DeleteEventSubscription<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SubscriptionId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SubscriptionId = "MySubscriptionId" # String | 

try {
    $Result = Invoke-DeleteEventSubscription -SubscriptionId $SubscriptionId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteEventSubscription: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SubscriptionId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListEventSubscriptions"></a>
# **Invoke-ListEventSubscriptions**
> EventSubscription[] Invoke-ListEventSubscriptions<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListEventSubscriptions
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListEventSubscriptions: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**EventSubscription[]**](EventSubscription.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

