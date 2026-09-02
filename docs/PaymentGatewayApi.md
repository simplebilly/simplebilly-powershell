# PSOpenAPITools.PSOpenAPITools\Api.PaymentGatewayApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-PaymentGatewayApi**](PaymentGatewayApi.md#New-PaymentGatewayApi) | **POST** /api/v1/payment-gateways | 
[**Invoke-DeletePaymentGatewayApi**](PaymentGatewayApi.md#Invoke-DeletePaymentGatewayApi) | **DELETE** /api/v1/payment-gateways/{gateway_id} | 
[**Invoke-ListPaymentGatewaysApi**](PaymentGatewayApi.md#Invoke-ListPaymentGatewaysApi) | **GET** /api/v1/payment-gateways/ | 
[**Invoke-OauthAuthorizeApi**](PaymentGatewayApi.md#Invoke-OauthAuthorizeApi) | **POST** /api/v1/payment-gateways/oauth/authorize | 
[**Invoke-OauthCallbackApi**](PaymentGatewayApi.md#Invoke-OauthCallbackApi) | **POST** /api/v1/payment-gateways/oauth/callback | 
[**Update-PaymentGatewayApi**](PaymentGatewayApi.md#Update-PaymentGatewayApi) | **PUT** /api/v1/payment-gateways/{gateway_id} | 


<a id="New-PaymentGatewayApi"></a>
# **New-PaymentGatewayApi**
> PaymentGateway New-PaymentGatewayApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = New-PaymentGatewayApi -Body $Body
} catch {
    Write-Host ("Exception occurred when calling New-PaymentGatewayApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**PaymentGateway**](PaymentGateway.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeletePaymentGatewayApi"></a>
# **Invoke-DeletePaymentGatewayApi**
> void Invoke-DeletePaymentGatewayApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GatewayId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GatewayId = "MyGatewayId" # String | 

try {
    $Result = Invoke-DeletePaymentGatewayApi -GatewayId $GatewayId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeletePaymentGatewayApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GatewayId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListPaymentGatewaysApi"></a>
# **Invoke-ListPaymentGatewaysApi**
> PaymentGateway[] Invoke-ListPaymentGatewaysApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListPaymentGatewaysApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListPaymentGatewaysApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PaymentGateway[]**](PaymentGateway.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-OauthAuthorizeApi"></a>
# **Invoke-OauthAuthorizeApi**
> GatewayOAuthAuthorizeResponse Invoke-OauthAuthorizeApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GatewayOAuthAuthorizeRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GatewayOAuthAuthorizeRequest = Initialize-GatewayOAuthAuthorizeRequest -GatewayType "MyGatewayType" -RedirectUri "MyRedirectUri" # GatewayOAuthAuthorizeRequest | 

try {
    $Result = Invoke-OauthAuthorizeApi -GatewayOAuthAuthorizeRequest $GatewayOAuthAuthorizeRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-OauthAuthorizeApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GatewayOAuthAuthorizeRequest** | [**GatewayOAuthAuthorizeRequest**](GatewayOAuthAuthorizeRequest.md)|  | 

### Return type

[**GatewayOAuthAuthorizeResponse**](GatewayOAuthAuthorizeResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-OauthCallbackApi"></a>
# **Invoke-OauthCallbackApi**
> PaymentGateway Invoke-OauthCallbackApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GatewayOAuthCallbackRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GatewayOAuthCallbackRequest = Initialize-GatewayOAuthCallbackRequest -Code "MyCode" -GatewayType "MyGatewayType" -RedirectUri "MyRedirectUri" -State "MyState" # GatewayOAuthCallbackRequest | 

try {
    $Result = Invoke-OauthCallbackApi -GatewayOAuthCallbackRequest $GatewayOAuthCallbackRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-OauthCallbackApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GatewayOAuthCallbackRequest** | [**GatewayOAuthCallbackRequest**](GatewayOAuthCallbackRequest.md)|  | 

### Return type

[**PaymentGateway**](PaymentGateway.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-PaymentGatewayApi"></a>
# **Update-PaymentGatewayApi**
> PaymentGateway Update-PaymentGatewayApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GatewayId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GatewayId = "MyGatewayId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-PaymentGatewayApi -GatewayId $GatewayId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-PaymentGatewayApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GatewayId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**PaymentGateway**](PaymentGateway.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

