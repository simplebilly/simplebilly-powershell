# PSOpenAPITools.PSOpenAPITools\Api.AutomationsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ListAutomations**](AutomationsApi.md#Invoke-ListAutomations) | **GET** /api/v1/automations | 
[**Invoke-TriggerAutomation**](AutomationsApi.md#Invoke-TriggerAutomation) | **POST** /api/v1/automations/{key}/trigger | 
[**Update-Automation**](AutomationsApi.md#Update-Automation) | **PUT** /api/v1/automations/{key} | 


<a id="Invoke-ListAutomations"></a>
# **Invoke-ListAutomations**
> AutomationDto[] Invoke-ListAutomations<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListAutomations
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListAutomations: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AutomationDto[]**](AutomationDto.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-TriggerAutomation"></a>
# **Invoke-TriggerAutomation**
> SystemCollectionsHashtable Invoke-TriggerAutomation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Key] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Key = "MyKey" # String | 

try {
    $Result = Invoke-TriggerAutomation -Key $Key
} catch {
    Write-Host ("Exception occurred when calling Invoke-TriggerAutomation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Key** | **String**|  | 

### Return type

[**SystemCollectionsHashtable**](SystemCollectionsHashtable.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Automation"></a>
# **Update-Automation**
> AutomationDto Update-Automation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Key] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdateAutomation] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Key = "MyKey" # String | 
$UpdateAutomation = Initialize-UpdateAutomation -Config  -Enabled $false # UpdateAutomation | 

try {
    $Result = Update-Automation -Key $Key -UpdateAutomation $UpdateAutomation
} catch {
    Write-Host ("Exception occurred when calling Update-Automation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Key** | **String**|  | 
 **UpdateAutomation** | [**UpdateAutomation**](UpdateAutomation.md)|  | 

### Return type

[**AutomationDto**](AutomationDto.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

