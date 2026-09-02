# PSOpenAPITools.PSOpenAPITools\Api.OnlineshopApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-SmtpConfigApi**](OnlineshopApi.md#Get-SmtpConfigApi) | **GET** /api/v1/settings/smtp | 
[**Save-SmtpConfigApi**](OnlineshopApi.md#Save-SmtpConfigApi) | **PUT** /api/v1/settings/smtp | 


<a id="Get-SmtpConfigApi"></a>
# **Get-SmtpConfigApi**
> SmtpConfig Get-SmtpConfigApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Get-SmtpConfigApi
} catch {
    Write-Host ("Exception occurred when calling Get-SmtpConfigApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**SmtpConfig**](SmtpConfig.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Save-SmtpConfigApi"></a>
# **Save-SmtpConfigApi**
> SmtpConfig Save-SmtpConfigApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SmtpConfig] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SmtpConfig = Initialize-SmtpConfig -Encryption "StartTls" -FromAddress "MyFromAddress" -FromName "MyFromName" -VarHost "MyVarHost" -Password "MyPassword" -Port 0 -TimeoutSeconds 0 -Username "MyUsername" # SmtpConfig |  (optional)

try {
    $Result = Save-SmtpConfigApi -SmtpConfig $SmtpConfig
} catch {
    Write-Host ("Exception occurred when calling Save-SmtpConfigApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SmtpConfig** | [**SmtpConfig**](SmtpConfig.md)|  | [optional] 

### Return type

[**SmtpConfig**](SmtpConfig.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

