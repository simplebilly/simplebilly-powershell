# PSOpenAPITools.PSOpenAPITools\Api.PaygapApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-PaygapAuskunftApi**](PaygapApi.md#Invoke-PaygapAuskunftApi) | **GET** /api/v1/bookkeeping/paygap/auskunft/{employee_id} | 
[**Invoke-PaygapExportApi**](PaygapApi.md#Invoke-PaygapExportApi) | **GET** /api/v1/bookkeeping/paygap/export | 
[**Invoke-PaygapReportApi**](PaygapApi.md#Invoke-PaygapReportApi) | **GET** /api/v1/bookkeeping/paygap/report | 


<a id="Invoke-PaygapAuskunftApi"></a>
# **Invoke-PaygapAuskunftApi**
> PayGapInfoResponse Invoke-PaygapAuskunftApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EmployeeId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$EmployeeId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PaygapAuskunftApi -EmployeeId $EmployeeId
} catch {
    Write-Host ("Exception occurred when calling Invoke-PaygapAuskunftApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **EmployeeId** | **String**|  | 

### Return type

[**PayGapInfoResponse**](PayGapInfoResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PaygapExportApi"></a>
# **Invoke-PaygapExportApi**
> PayGapExportResponse Invoke-PaygapExportApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-PaygapExportApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-PaygapExportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PayGapExportResponse**](PayGapExportResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PaygapReportApi"></a>
# **Invoke-PaygapReportApi**
> PayGapReport Invoke-PaygapReportApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-PaygapReportApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-PaygapReportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PayGapReport**](PayGapReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

