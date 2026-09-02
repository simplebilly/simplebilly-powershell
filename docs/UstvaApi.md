# PSOpenAPITools.PSOpenAPITools\Api.UstvaApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-JahresustApi**](UstvaApi.md#Invoke-JahresustApi) | **GET** /api/v1/bookkeeping/jahresust | 
[**Invoke-UstvaApi**](UstvaApi.md#Invoke-UstvaApi) | **GET** /api/v1/bookkeeping/ustva | 


<a id="Invoke-JahresustApi"></a>
# **Invoke-JahresustApi**
> JahresUstErgebnis Invoke-JahresustApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-JahresustApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-JahresustApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**JahresUstErgebnis**](JahresUstErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-UstvaApi"></a>
# **Invoke-UstvaApi**
> UstvaErgebnis Invoke-UstvaApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Zeitraum] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Zeitraum = "MyZeitraum" # String | 

try {
    $Result = Invoke-UstvaApi -Zeitraum $Zeitraum
} catch {
    Write-Host ("Exception occurred when calling Invoke-UstvaApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Zeitraum** | **String**|  | 

### Return type

[**UstvaErgebnis**](UstvaErgebnis.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

