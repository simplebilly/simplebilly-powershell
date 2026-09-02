# PSOpenAPITools.PSOpenAPITools\Api.DatevApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-DatevExportApi**](DatevApi.md#Invoke-DatevExportApi) | **GET** /api/v1/bookkeeping/datev/export | Export bookkeeping data as DATEV CSV
[**Invoke-DatevPreviewApi**](DatevApi.md#Invoke-DatevPreviewApi) | **GET** /api/v1/bookkeeping/datev/preview | Exported_datev_bookings: returns formed bookings for review


<a id="Invoke-DatevExportApi"></a>
# **Invoke-DatevExportApi**
> DatevExportResponse Invoke-DatevExportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AccountSchema] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateFrom] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateTo] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>

Export bookkeeping data as DATEV CSV

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AccountSchema = "MyAccountSchema" # String |  (optional)
$DateFrom = "MyDateFrom" # String |  (optional)
$DateTo = "MyDateTo" # String |  (optional)
$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)

# Export bookkeeping data as DATEV CSV
try {
    $Result = Invoke-DatevExportApi -AccountSchema $AccountSchema -DateFrom $DateFrom -DateTo $DateTo -Page $Page -PageSize $PageSize
} catch {
    Write-Host ("Exception occurred when calling Invoke-DatevExportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AccountSchema** | **String**|  | [optional] 
 **DateFrom** | **String**|  | [optional] 
 **DateTo** | **String**|  | [optional] 
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 

### Return type

[**DatevExportResponse**](DatevExportResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DatevPreviewApi"></a>
# **Invoke-DatevPreviewApi**
> DatevBookingPreview[] Invoke-DatevPreviewApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AccountSchema] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateFrom] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateTo] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>

Exported_datev_bookings: returns formed bookings for review

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AccountSchema = "MyAccountSchema" # String |  (optional)
$DateFrom = "MyDateFrom" # String |  (optional)
$DateTo = "MyDateTo" # String |  (optional)
$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)

# Exported_datev_bookings: returns formed bookings for review
try {
    $Result = Invoke-DatevPreviewApi -AccountSchema $AccountSchema -DateFrom $DateFrom -DateTo $DateTo -Page $Page -PageSize $PageSize
} catch {
    Write-Host ("Exception occurred when calling Invoke-DatevPreviewApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AccountSchema** | **String**|  | [optional] 
 **DateFrom** | **String**|  | [optional] 
 **DateTo** | **String**|  | [optional] 
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 

### Return type

[**DatevBookingPreview[]**](DatevBookingPreview.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

