# PSOpenAPITools.PSOpenAPITools\Api.SupportChannelApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ChannelApi**](SupportChannelApi.md#New-ChannelApi) | **POST** /api/v1/support/channels | 
[**Invoke-DeleteChannelApi**](SupportChannelApi.md#Invoke-DeleteChannelApi) | **DELETE** /api/v1/support/channels/{channel_id} | 
[**Invoke-ListChannelsApi**](SupportChannelApi.md#Invoke-ListChannelsApi) | **GET** /api/v1/support/channels | 
[**Update-ChannelApi**](SupportChannelApi.md#Update-ChannelApi) | **PUT** /api/v1/support/channels/{channel_id} | 


<a id="New-ChannelApi"></a>
# **New-ChannelApi**
> SupportChannel New-ChannelApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreateChannelDto] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CreateChannelDto = Initialize-CreateChannelDto -ChannelType "MyChannelType" -Config  -Name "MyName" # CreateChannelDto | 

try {
    $Result = New-ChannelApi -CreateChannelDto $CreateChannelDto
} catch {
    Write-Host ("Exception occurred when calling New-ChannelApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateChannelDto** | [**CreateChannelDto**](CreateChannelDto.md)|  | 

### Return type

[**SupportChannel**](SupportChannel.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteChannelApi"></a>
# **Invoke-DeleteChannelApi**
> void Invoke-DeleteChannelApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ChannelId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ChannelId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteChannelApi -ChannelId $ChannelId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteChannelApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ChannelId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListChannelsApi"></a>
# **Invoke-ListChannelsApi**
> SupportChannel[] Invoke-ListChannelsApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListChannelsApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListChannelsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**SupportChannel[]**](SupportChannel.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ChannelApi"></a>
# **Update-ChannelApi**
> SupportChannel Update-ChannelApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ChannelId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdateChannelDto] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ChannelId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$UpdateChannelDto = Initialize-UpdateChannelDto -Config  -IsActive $false -Name "MyName" # UpdateChannelDto | 

try {
    $Result = Update-ChannelApi -ChannelId $ChannelId -UpdateChannelDto $UpdateChannelDto
} catch {
    Write-Host ("Exception occurred when calling Update-ChannelApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ChannelId** | **String**|  | 
 **UpdateChannelDto** | [**UpdateChannelDto**](UpdateChannelDto.md)|  | 

### Return type

[**SupportChannel**](SupportChannel.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

