# PSOpenAPITools.PSOpenAPITools\Api.OssReportApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-OssReportApi**](OssReportApi.md#Invoke-OssReportApi) | **GET** /api/v1/bookkeeping/oss | 


<a id="Invoke-OssReportApi"></a>
# **Invoke-OssReportApi**
> OssReport Invoke-OssReportApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-OssReportApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-OssReportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**OssReport**](OssReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

