# PSOpenAPITools.PSOpenAPITools\Api.GewinnverwendungApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-GewinnverwendungApi**](GewinnverwendungApi.md#Invoke-GewinnverwendungApi) | **GET** /api/v1/bookkeeping/gewinnverwendung | 
[**Invoke-GewinnverwendungExportApi**](GewinnverwendungApi.md#Invoke-GewinnverwendungExportApi) | **GET** /api/v1/bookkeeping/gewinnverwendung/export | 


<a id="Invoke-GewinnverwendungApi"></a>
# **Invoke-GewinnverwendungApi**
> GewinnverwendungsReport Invoke-GewinnverwendungApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-GewinnverwendungApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-GewinnverwendungApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**GewinnverwendungsReport**](GewinnverwendungsReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-GewinnverwendungExportApi"></a>
# **Invoke-GewinnverwendungExportApi**
> GewinnverwendungsExportResponse Invoke-GewinnverwendungExportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-GewinnverwendungExportApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-GewinnverwendungExportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**GewinnverwendungsExportResponse**](GewinnverwendungsExportResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

