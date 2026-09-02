# PSOpenAPITools.PSOpenAPITools\Api.InstituteApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ConvertTo-stituteStatusApi**](InstituteApi.md#ConvertTo-stituteStatusApi) | **GET** /api/v1/bookkeeping/institute/status | 


<a id="ConvertTo-stituteStatusApi"></a>
# **ConvertTo-stituteStatusApi**
> InstituteStatus ConvertTo-stituteStatusApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = ConvertTo-stituteStatusApi
} catch {
    Write-Host ("Exception occurred when calling ConvertTo-stituteStatusApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InstituteStatus**](InstituteStatus.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

