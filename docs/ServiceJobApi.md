# PSOpenAPITools.PSOpenAPITools\Api.ServiceJobApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ServiceJob**](ServiceJobApi.md#New-ServiceJob) | **POST** /api/v1/service-jobs | 
[**Invoke-DeleteServiceJob**](ServiceJobApi.md#Invoke-DeleteServiceJob) | **DELETE** /api/v1/service-jobs/{id} | 
[**Get-ServiceJob**](ServiceJobApi.md#Get-ServiceJob) | **GET** /api/v1/service-jobs/{id} | 
[**Get-ServiceJobs**](ServiceJobApi.md#Get-ServiceJobs) | **GET** /api/v1/service-jobs/ | 
[**Update-ServiceJob**](ServiceJobApi.md#Update-ServiceJob) | **PUT** /api/v1/service-jobs/{id} | 


<a id="New-ServiceJob"></a>
# **New-ServiceJob**
> ServiceJob New-ServiceJob<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ServiceJobCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ServiceJobCreate = Initialize-ServiceJobCreate -Address "MyAddress" -CustomerEmail "MyCustomerEmail" -CustomerId "MyCustomerId" -CustomerName "MyCustomerName" -CustomerPhone "MyCustomerPhone" -Description "MyDescription" -EstimatedDurationMinutes 0 -Lat 0 -Lng 0 -Notes "MyNotes" -Status "pending" # ServiceJobCreate | 

try {
    $Result = New-ServiceJob -ServiceJobCreate $ServiceJobCreate
} catch {
    Write-Host ("Exception occurred when calling New-ServiceJob: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ServiceJobCreate** | [**ServiceJobCreate**](ServiceJobCreate.md)|  | 

### Return type

[**ServiceJob**](ServiceJob.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteServiceJob"></a>
# **Invoke-DeleteServiceJob**
> void Invoke-DeleteServiceJob<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteServiceJob -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteServiceJob: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ServiceJob"></a>
# **Get-ServiceJob**
> ServiceJob Get-ServiceJob<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-ServiceJob -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-ServiceJob: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**ServiceJob**](ServiceJob.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ServiceJobs"></a>
# **Get-ServiceJobs**
> ServiceJob[] Get-ServiceJobs<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IncludeDeleted] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 1 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)
$IncludeDeleted = $true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

try {
    $Result = Get-ServiceJobs -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-ServiceJobs: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **IncludeDeleted** | **Boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**ServiceJob[]**](ServiceJob.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ServiceJob"></a>
# **Update-ServiceJob**
> ServiceJob Update-ServiceJob<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ServiceJobUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$ServiceJobUpdate = Initialize-ServiceJobUpdate -Address "MyAddress" -CustomerEmail "MyCustomerEmail" -CustomerId "MyCustomerId" -CustomerName "MyCustomerName" -CustomerPhone "MyCustomerPhone" -Description "MyDescription" -EstimatedDurationMinutes 0 -Lat 0 -Lng 0 -Notes "MyNotes" -Status "pending" # ServiceJobUpdate | 

try {
    $Result = Update-ServiceJob -Id $Id -ServiceJobUpdate $ServiceJobUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ServiceJob: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **ServiceJobUpdate** | [**ServiceJobUpdate**](ServiceJobUpdate.md)|  | 

### Return type

[**ServiceJob**](ServiceJob.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

