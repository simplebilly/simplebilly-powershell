# PSOpenAPITools.PSOpenAPITools\Api.EuerApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-EuerApi**](EuerApi.md#Invoke-EuerApi) | **GET** /api/v1/bookkeeping/euer | 
[**Invoke-EuerKategorienApi**](EuerApi.md#Invoke-EuerKategorienApi) | **GET** /api/v1/bookkeeping/euer/kategorien | 


<a id="Invoke-EuerApi"></a>
# **Invoke-EuerApi**
> EuerErgebnis Invoke-EuerApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-EuerApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-EuerApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**EuerErgebnis**](EuerErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-EuerKategorienApi"></a>
# **Invoke-EuerKategorienApi**
> EuerDetailErgebnis Invoke-EuerKategorienApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-EuerKategorienApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-EuerKategorienApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**EuerDetailErgebnis**](EuerDetailErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

