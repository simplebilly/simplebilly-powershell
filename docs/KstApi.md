# PSOpenAPITools.PSOpenAPITools\Api.KstApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-KstApi**](KstApi.md#Invoke-KstApi) | **GET** /api/v1/bookkeeping/kst | 


<a id="Invoke-KstApi"></a>
# **Invoke-KstApi**
> KstErgebnis Invoke-KstApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Gewinn] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 
$Gewinn = "MyGewinn" # String |  (optional)

try {
    $Result = Invoke-KstApi -Year $Year -Gewinn $Gewinn
} catch {
    Write-Host ("Exception occurred when calling Invoke-KstApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 
 **Gewinn** | **String**|  | [optional] 

### Return type

[**KstErgebnis**](KstErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

