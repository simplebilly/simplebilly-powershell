# PSOpenAPITools.PSOpenAPITools\Api.EbilanzApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-EbilanzReportApi**](EbilanzApi.md#Invoke-EbilanzReportApi) | **GET** /api/v1/bookkeeping/ebilanz | 
[**Invoke-EbilanzXbrlExportApi**](EbilanzApi.md#Invoke-EbilanzXbrlExportApi) | **GET** /api/v1/bookkeeping/ebilanz/xbrl | 


<a id="Invoke-EbilanzReportApi"></a>
# **Invoke-EbilanzReportApi**
> EBilanzReport Invoke-EbilanzReportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateFrom] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateTo] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 |  (optional)
$DateFrom = "MyDateFrom" # String |  (optional)
$DateTo = "MyDateTo" # String |  (optional)

try {
    $Result = Invoke-EbilanzReportApi -Year $Year -DateFrom $DateFrom -DateTo $DateTo
} catch {
    Write-Host ("Exception occurred when calling Invoke-EbilanzReportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | [optional] 
 **DateFrom** | **String**|  | [optional] 
 **DateTo** | **String**|  | [optional] 

### Return type

[**EBilanzReport**](EBilanzReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-EbilanzXbrlExportApi"></a>
# **Invoke-EbilanzXbrlExportApi**
> void Invoke-EbilanzXbrlExportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateFrom] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateTo] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 |  (optional)
$DateFrom = "MyDateFrom" # String |  (optional)
$DateTo = "MyDateTo" # String |  (optional)

try {
    $Result = Invoke-EbilanzXbrlExportApi -Year $Year -DateFrom $DateFrom -DateTo $DateTo
} catch {
    Write-Host ("Exception occurred when calling Invoke-EbilanzXbrlExportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | [optional] 
 **DateFrom** | **String**|  | [optional] 
 **DateTo** | **String**|  | [optional] 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/xml

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

