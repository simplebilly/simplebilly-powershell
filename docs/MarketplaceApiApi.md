# PSOpenAPITools.PSOpenAPITools\Api.MarketplaceApiApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ConnectionApi**](MarketplaceApiApi.md#New-ConnectionApi) | **POST** /api/v1/marketplace/connections | Create a new connection (for API-key based platforms)
[**Invoke-DeleteConnectionApi**](MarketplaceApiApi.md#Invoke-DeleteConnectionApi) | **DELETE** /api/v1/marketplace/connections/{connection_id} | Soft-delete a connection
[**Get-ConnectionApi**](MarketplaceApiApi.md#Get-ConnectionApi) | **GET** /api/v1/marketplace/connections/{connection_id} | Get a single connection
[**Get-SyncDirectionApi**](MarketplaceApiApi.md#Get-SyncDirectionApi) | **GET** /api/v1/marketplace/connections/{connection_id}/directions | Get current sync direction configuration for a connection
[**Get-SyncLogsApi**](MarketplaceApiApi.md#Get-SyncLogsApi) | **GET** /api/v1/marketplace/connections/{connection_id}/logs | Get sync logs for a connection
[**Invoke-ListConnectionsApi**](MarketplaceApiApi.md#Invoke-ListConnectionsApi) | **GET** /api/v1/marketplace/connections | List connections for the current tenant
[**Invoke-ListPlatformsApi**](MarketplaceApiApi.md#Invoke-ListPlatformsApi) | **GET** /api/v1/marketplace/platforms | List all supported platforms
[**Invoke-OauthAuthorizeApi**](MarketplaceApiApi.md#Invoke-OauthAuthorizeApi) | **POST** /api/v1/marketplace/oauth/authorize | OAuth: initiate authorization flow
[**Invoke-OauthCallbackApi**](MarketplaceApiApi.md#Invoke-OauthCallbackApi) | **POST** /api/v1/marketplace/oauth/callback | OAuth: handle callback after authorization
[**Invoke-TriggerSyncApi**](MarketplaceApiApi.md#Invoke-TriggerSyncApi) | **POST** /api/v1/marketplace/connections/{connection_id}/sync | Trigger sync for a connection
[**Update-ConnectionApi**](MarketplaceApiApi.md#Update-ConnectionApi) | **PUT** /api/v1/marketplace/connections/{connection_id} | Update a connection
[**Update-SyncDirectionApi**](MarketplaceApiApi.md#Update-SyncDirectionApi) | **PUT** /api/v1/marketplace/connections/{connection_id}/directions | Update per-entity sync direction configuration for a connection
[**Invoke-WebhookReceiverApi**](MarketplaceApiApi.md#Invoke-WebhookReceiverApi) | **POST** /api/v1/marketplace/webhook/{platform}/{connection_id} | Webhook receiver


<a id="New-ConnectionApi"></a>
# **New-ConnectionApi**
> MarketplaceConnection New-ConnectionApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreateConnectionRequest] <PSCustomObject><br>

Create a new connection (for API-key based platforms)

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CreateConnectionRequest = Initialize-CreateConnectionRequest -ApiKey "MyApiKey" -ApiSecret "MyApiSecret" -Config  -Label "MyLabel" -Platform "MyPlatform" -ShopDomain "MyShopDomain" # CreateConnectionRequest | 

# Create a new connection (for API-key based platforms)
try {
    $Result = New-ConnectionApi -CreateConnectionRequest $CreateConnectionRequest
} catch {
    Write-Host ("Exception occurred when calling New-ConnectionApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateConnectionRequest** | [**CreateConnectionRequest**](CreateConnectionRequest.md)|  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteConnectionApi"></a>
# **Invoke-DeleteConnectionApi**
> void Invoke-DeleteConnectionApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConnectionId] <String><br>

Soft-delete a connection

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConnectionId = "MyConnectionId" # String | 

# Soft-delete a connection
try {
    $Result = Invoke-DeleteConnectionApi -ConnectionId $ConnectionId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteConnectionApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConnectionId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ConnectionApi"></a>
# **Get-ConnectionApi**
> MarketplaceConnection Get-ConnectionApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConnectionId] <String><br>

Get a single connection

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConnectionId = "MyConnectionId" # String | 

# Get a single connection
try {
    $Result = Get-ConnectionApi -ConnectionId $ConnectionId
} catch {
    Write-Host ("Exception occurred when calling Get-ConnectionApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConnectionId** | **String**|  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-SyncDirectionApi"></a>
# **Get-SyncDirectionApi**
> void Get-SyncDirectionApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConnectionId] <String><br>

Get current sync direction configuration for a connection

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConnectionId = "MyConnectionId" # String | 

# Get current sync direction configuration for a connection
try {
    $Result = Get-SyncDirectionApi -ConnectionId $ConnectionId
} catch {
    Write-Host ("Exception occurred when calling Get-SyncDirectionApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConnectionId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-SyncLogsApi"></a>
# **Get-SyncLogsApi**
> SyncLog[] Get-SyncLogsApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConnectionId] <String><br>

Get sync logs for a connection

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConnectionId = "MyConnectionId" # String | 

# Get sync logs for a connection
try {
    $Result = Get-SyncLogsApi -ConnectionId $ConnectionId
} catch {
    Write-Host ("Exception occurred when calling Get-SyncLogsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConnectionId** | **String**|  | 

### Return type

[**SyncLog[]**](SyncLog.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListConnectionsApi"></a>
# **Invoke-ListConnectionsApi**
> MarketplaceConnection[] Invoke-ListConnectionsApi<br>

List connections for the current tenant

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# List connections for the current tenant
try {
    $Result = Invoke-ListConnectionsApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListConnectionsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**MarketplaceConnection[]**](MarketplaceConnection.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListPlatformsApi"></a>
# **Invoke-ListPlatformsApi**
> PlatformInfo[] Invoke-ListPlatformsApi<br>

List all supported platforms

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# List all supported platforms
try {
    $Result = Invoke-ListPlatformsApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListPlatformsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PlatformInfo[]**](PlatformInfo.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-OauthAuthorizeApi"></a>
# **Invoke-OauthAuthorizeApi**
> OAuthAuthorizeResponse Invoke-OauthAuthorizeApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OAuthAuthorizeRequest] <PSCustomObject><br>

OAuth: initiate authorization flow

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OAuthAuthorizeRequest = Initialize-OAuthAuthorizeRequest -Config  -Platform "MyPlatform" -RedirectUri "MyRedirectUri" # OAuthAuthorizeRequest | 

# OAuth: initiate authorization flow
try {
    $Result = Invoke-OauthAuthorizeApi -OAuthAuthorizeRequest $OAuthAuthorizeRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-OauthAuthorizeApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OAuthAuthorizeRequest** | [**OAuthAuthorizeRequest**](OAuthAuthorizeRequest.md)|  | 

### Return type

[**OAuthAuthorizeResponse**](OAuthAuthorizeResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-OauthCallbackApi"></a>
# **Invoke-OauthCallbackApi**
> MarketplaceConnection Invoke-OauthCallbackApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OAuthCallbackRequest] <PSCustomObject><br>

OAuth: handle callback after authorization

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OAuthCallbackRequest = Initialize-OAuthCallbackRequest -Code "MyCode" -Config  -ConnectionId "MyConnectionId" -Platform "MyPlatform" -ShopDomain "MyShopDomain" -State "MyState" # OAuthCallbackRequest | 

# OAuth: handle callback after authorization
try {
    $Result = Invoke-OauthCallbackApi -OAuthCallbackRequest $OAuthCallbackRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-OauthCallbackApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OAuthCallbackRequest** | [**OAuthCallbackRequest**](OAuthCallbackRequest.md)|  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-TriggerSyncApi"></a>
# **Invoke-TriggerSyncApi**
> SyncSummary Invoke-TriggerSyncApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConnectionId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SyncType] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Direction] <String><br>

Trigger sync for a connection

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConnectionId = "MyConnectionId" # String | 
$SyncType = "MySyncType" # String |  (optional)
$Direction = "MyDirection" # String |  (optional)

# Trigger sync for a connection
try {
    $Result = Invoke-TriggerSyncApi -ConnectionId $ConnectionId -SyncType $SyncType -Direction $Direction
} catch {
    Write-Host ("Exception occurred when calling Invoke-TriggerSyncApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConnectionId** | **String**|  | 
 **SyncType** | **String**|  | [optional] 
 **Direction** | **String**|  | [optional] 

### Return type

[**SyncSummary**](SyncSummary.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ConnectionApi"></a>
# **Update-ConnectionApi**
> MarketplaceConnection Update-ConnectionApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConnectionId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdateConnectionRequest] <PSCustomObject><br>

Update a connection

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConnectionId = "MyConnectionId" # String | 
$UpdateConnectionRequest = Initialize-UpdateConnectionRequest -ApiKey "MyApiKey" -ApiSecret "MyApiSecret" -Config  -IsActive $false -Label "MyLabel" -ShopDomain "MyShopDomain" # UpdateConnectionRequest | 

# Update a connection
try {
    $Result = Update-ConnectionApi -ConnectionId $ConnectionId -UpdateConnectionRequest $UpdateConnectionRequest
} catch {
    Write-Host ("Exception occurred when calling Update-ConnectionApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConnectionId** | **String**|  | 
 **UpdateConnectionRequest** | [**UpdateConnectionRequest**](UpdateConnectionRequest.md)|  | 

### Return type

[**MarketplaceConnection**](MarketplaceConnection.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-SyncDirectionApi"></a>
# **Update-SyncDirectionApi**
> void Update-SyncDirectionApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConnectionId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdateSyncDirectionRequest] <PSCustomObject><br>

Update per-entity sync direction configuration for a connection

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConnectionId = "MyConnectionId" # String | 
$UpdateSyncDirectionRequest = Initialize-UpdateSyncDirectionRequest -Directions @{ key_example = "MyInner" } # UpdateSyncDirectionRequest | 

# Update per-entity sync direction configuration for a connection
try {
    $Result = Update-SyncDirectionApi -ConnectionId $ConnectionId -UpdateSyncDirectionRequest $UpdateSyncDirectionRequest
} catch {
    Write-Host ("Exception occurred when calling Update-SyncDirectionApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConnectionId** | **String**|  | 
 **UpdateSyncDirectionRequest** | [**UpdateSyncDirectionRequest**](UpdateSyncDirectionRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-WebhookReceiverApi"></a>
# **Invoke-WebhookReceiverApi**
> void Invoke-WebhookReceiverApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Platform] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConnectionId] <String><br>

Webhook receiver

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Platform = "MyPlatform" # String | 
$ConnectionId = "MyConnectionId" # String | 

# Webhook receiver
try {
    $Result = Invoke-WebhookReceiverApi -Platform $Platform -ConnectionId $ConnectionId
} catch {
    Write-Host ("Exception occurred when calling Invoke-WebhookReceiverApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Platform** | **String**|  | 
 **ConnectionId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

