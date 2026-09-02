# PSOpenAPITools.PSOpenAPITools\Api.WebhooksApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Subscription**](WebhooksApi.md#New-Subscription) | **POST** /api/v1/webhook-subscriptions | Create a webhook subscription (outbound hook).
[**Invoke-DeleteSubscription**](WebhooksApi.md#Invoke-DeleteSubscription) | **DELETE** /api/v1/webhook-subscriptions/{subscription_id} | Delete a webhook subscription.
[**Invoke-EmitApi**](WebhooksApi.md#Invoke-EmitApi) | **POST** /api/v1/webhooks/emit | Manually fire an event against matching hooks (for testing/flows).
[**Invoke-ListEvent**](WebhooksApi.md#Invoke-ListEvent) | **GET** /api/v1/webhook-events | List webhook events (inbound + outbound log).
[**Invoke-ListSubscriptions**](WebhooksApi.md#Invoke-ListSubscriptions) | **GET** /api/v1/webhook-subscriptions | List webhook subscriptions for the tenant.
[**Update-Subscription**](WebhooksApi.md#Update-Subscription) | **PUT** /api/v1/webhook-subscriptions/{subscription_id} | Update a webhook subscription.


<a id="New-Subscription"></a>
# **New-Subscription**
> WebhookSubscription New-Subscription<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreateSubscriptionRequest] <PSCustomObject><br>

Create a webhook subscription (outbound hook).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CreateSubscriptionRequest = Initialize-CreateSubscriptionRequest -EventType "MyEventType" -IsActive $false -Name "MyName" -Secret "MySecret" -Url "MyUrl" # CreateSubscriptionRequest | 

# Create a webhook subscription (outbound hook).
try {
    $Result = New-Subscription -CreateSubscriptionRequest $CreateSubscriptionRequest
} catch {
    Write-Host ("Exception occurred when calling New-Subscription: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateSubscriptionRequest** | [**CreateSubscriptionRequest**](CreateSubscriptionRequest.md)|  | 

### Return type

[**WebhookSubscription**](WebhookSubscription.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteSubscription"></a>
# **Invoke-DeleteSubscription**
> void Invoke-DeleteSubscription<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SubscriptionId] <String><br>

Delete a webhook subscription.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SubscriptionId = "MySubscriptionId" # String | 

# Delete a webhook subscription.
try {
    $Result = Invoke-DeleteSubscription -SubscriptionId $SubscriptionId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteSubscription: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-EmitApi"></a>
# **Invoke-EmitApi**
> void Invoke-EmitApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmitEventRequest] <PSCustomObject><br>

Manually fire an event against matching hooks (for testing/flows).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$EmitEventRequest = Initialize-EmitEventRequest -EventType "MyEventType" -Payload # EmitEventRequest | 

# Manually fire an event against matching hooks (for testing/flows).
try {
    $Result = Invoke-EmitApi -EmitEventRequest $EmitEventRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-EmitApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **EmitEventRequest** | [**EmitEventRequest**](EmitEventRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListEvent"></a>
# **Invoke-ListEvent**
> WebhookEvent[] Invoke-ListEvent<br>

List webhook events (inbound + outbound log).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# List webhook events (inbound + outbound log).
try {
    $Result = Invoke-ListEvent
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListEvent: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookEvent[]**](WebhookEvent.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListSubscriptions"></a>
# **Invoke-ListSubscriptions**
> WebhookSubscription[] Invoke-ListSubscriptions<br>

List webhook subscriptions for the tenant.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# List webhook subscriptions for the tenant.
try {
    $Result = Invoke-ListSubscriptions
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListSubscriptions: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**WebhookSubscription[]**](WebhookSubscription.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Subscription"></a>
# **Update-Subscription**
> WebhookSubscription Update-Subscription<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SubscriptionId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdateSubscriptionRequest] <PSCustomObject><br>

Update a webhook subscription.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SubscriptionId = "MySubscriptionId" # String | 
$UpdateSubscriptionRequest = Initialize-UpdateSubscriptionRequest -EventType "MyEventType" -IsActive $false -Name "MyName" -Secret "MySecret" -Url "MyUrl" # UpdateSubscriptionRequest | 

# Update a webhook subscription.
try {
    $Result = Update-Subscription -SubscriptionId $SubscriptionId -UpdateSubscriptionRequest $UpdateSubscriptionRequest
} catch {
    Write-Host ("Exception occurred when calling Update-Subscription: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SubscriptionId** | **String**|  | 
 **UpdateSubscriptionRequest** | [**UpdateSubscriptionRequest**](UpdateSubscriptionRequest.md)|  | 

### Return type

[**WebhookSubscription**](WebhookSubscription.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

