# PSOpenAPITools.PSOpenAPITools\Api.OffenlegungApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-OffenlegungApi**](OffenlegungApi.md#Invoke-OffenlegungApi) | **GET** /api/v1/bookkeeping/offenlegung | 


<a id="Invoke-OffenlegungApi"></a>
# **Invoke-OffenlegungApi**
> OffenlegungReport Invoke-OffenlegungApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-OffenlegungApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-OffenlegungApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**OffenlegungReport**](OffenlegungReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

