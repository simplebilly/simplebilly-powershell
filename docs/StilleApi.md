# PSOpenAPITools.PSOpenAPITools\Api.StilleApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-StilleExportApi**](StilleApi.md#Invoke-StilleExportApi) | **GET** /api/v1/bookkeeping/stille/export | 
[**Invoke-StilleReportApi**](StilleApi.md#Invoke-StilleReportApi) | **GET** /api/v1/bookkeeping/stille/report | 


<a id="Invoke-StilleExportApi"></a>
# **Invoke-StilleExportApi**
> StilleExportResponse Invoke-StilleExportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-StilleExportApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-StilleExportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**StilleExportResponse**](StilleExportResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-StilleReportApi"></a>
# **Invoke-StilleReportApi**
> StilleReport Invoke-StilleReportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-StilleReportApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-StilleReportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**StilleReport**](StilleReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

