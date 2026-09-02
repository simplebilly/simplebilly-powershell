# PSOpenAPITools.PSOpenAPITools\Api.KostenVorschauApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-KostenVorschauApi**](KostenVorschauApi.md#Invoke-KostenVorschauApi) | **GET** /api/v1/bookkeeping/kosten-vorschau | 


<a id="Invoke-KostenVorschauApi"></a>
# **Invoke-KostenVorschauApi**
> KostenVorschau Invoke-KostenVorschauApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Month] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 
$Month = 56 # Int32 | 

try {
    $Result = Invoke-KostenVorschauApi -Year $Year -Month $Month
} catch {
    Write-Host ("Exception occurred when calling Invoke-KostenVorschauApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 
 **Month** | **Int32**|  | 

### Return type

[**KostenVorschau**](KostenVorschau.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

