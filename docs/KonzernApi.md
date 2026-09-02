# PSOpenAPITools.PSOpenAPITools\Api.KonzernApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-KonzernExportApi**](KonzernApi.md#Invoke-KonzernExportApi) | **GET** /api/v1/bookkeeping/konzern/status/export | 
[**Invoke-KonzernStatusApi**](KonzernApi.md#Invoke-KonzernStatusApi) | **GET** /api/v1/bookkeeping/konzern/status | 


<a id="Invoke-KonzernExportApi"></a>
# **Invoke-KonzernExportApi**
> KonzernExportResponse Invoke-KonzernExportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-KonzernExportApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-KonzernExportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**KonzernExportResponse**](KonzernExportResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-KonzernStatusApi"></a>
# **Invoke-KonzernStatusApi**
> KonzernStatus Invoke-KonzernStatusApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-KonzernStatusApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-KonzernStatusApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**KonzernStatus**](KonzernStatus.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

