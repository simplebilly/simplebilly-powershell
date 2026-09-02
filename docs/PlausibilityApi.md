# PSOpenAPITools.PSOpenAPITools\Api.PlausibilityApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-PlausibilityCheckApi**](PlausibilityApi.md#Invoke-PlausibilityCheckApi) | **GET** /api/v1/bookkeeping/plausibility | 


<a id="Invoke-PlausibilityCheckApi"></a>
# **Invoke-PlausibilityCheckApi**
> PlausibilityReport Invoke-PlausibilityCheckApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateFrom] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateTo] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DateFrom = "MyDateFrom" # String |  (optional)
$DateTo = "MyDateTo" # String |  (optional)

try {
    $Result = Invoke-PlausibilityCheckApi -DateFrom $DateFrom -DateTo $DateTo
} catch {
    Write-Host ("Exception occurred when calling Invoke-PlausibilityCheckApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DateFrom** | **String**|  | [optional] 
 **DateTo** | **String**|  | [optional] 

### Return type

[**PlausibilityReport**](PlausibilityReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

