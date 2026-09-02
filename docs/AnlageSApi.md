# PSOpenAPITools.PSOpenAPITools\Api.AnlageSApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-AnlageSApi**](AnlageSApi.md#Invoke-AnlageSApi) | **GET** /api/v1/bookkeeping/anlage-s | 


<a id="Invoke-AnlageSApi"></a>
# **Invoke-AnlageSApi**
> AnlageSErgebnis Invoke-AnlageSApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-AnlageSApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-AnlageSApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**AnlageSErgebnis**](AnlageSErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

