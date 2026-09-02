# PSOpenAPITools.PSOpenAPITools\Api.EmissionsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-EmissionEntryApi**](EmissionsApi.md#New-EmissionEntryApi) | **POST** /api/v1/bookkeeping/emissions/entries | 
[**New-EmissionTargetApi**](EmissionsApi.md#New-EmissionTargetApi) | **POST** /api/v1/bookkeeping/emissions/targets | 
[**Invoke-DeleteEmissionEntryApi**](EmissionsApi.md#Invoke-DeleteEmissionEntryApi) | **DELETE** /api/v1/bookkeeping/emissions/entries/{id} | 
[**Invoke-DeleteEmissionTargetApi**](EmissionsApi.md#Invoke-DeleteEmissionTargetApi) | **DELETE** /api/v1/bookkeeping/emissions/targets/{id} | 
[**Invoke-EmissionsEntriesApi**](EmissionsApi.md#Invoke-EmissionsEntriesApi) | **GET** /api/v1/bookkeeping/emissions/entries | 
[**Invoke-EmissionsExportApi**](EmissionsApi.md#Invoke-EmissionsExportApi) | **GET** /api/v1/bookkeeping/emissions/export | 
[**Invoke-EmissionsFactorsApi**](EmissionsApi.md#Invoke-EmissionsFactorsApi) | **GET** /api/v1/bookkeeping/emissions/factors | 
[**Invoke-EmissionsReportApi**](EmissionsApi.md#Invoke-EmissionsReportApi) | **GET** /api/v1/bookkeeping/emissions/report | 
[**Invoke-EmissionsTargetsApi**](EmissionsApi.md#Invoke-EmissionsTargetsApi) | **GET** /api/v1/bookkeeping/emissions/targets | 


<a id="New-EmissionEntryApi"></a>
# **New-EmissionEntryApi**
> EmissionEntry New-EmissionEntryApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreateEmissionEntry] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CreateEmissionEntry = Initialize-CreateEmissionEntry -ActivityValue "MyActivityValue" -CategoryId "MyCategoryId" -Description "MyDescription" -Method "MyMethod" -Scope "MyScope" -Unit "MyUnit" -Year 0 # CreateEmissionEntry | 

try {
    $Result = New-EmissionEntryApi -CreateEmissionEntry $CreateEmissionEntry
} catch {
    Write-Host ("Exception occurred when calling New-EmissionEntryApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateEmissionEntry** | [**CreateEmissionEntry**](CreateEmissionEntry.md)|  | 

### Return type

[**EmissionEntry**](EmissionEntry.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-EmissionTargetApi"></a>
# **New-EmissionTargetApi**
> EmissionTarget New-EmissionTargetApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreateEmissionTarget] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CreateEmissionTarget = Initialize-CreateEmissionTarget -BaseValue "MyBaseValue" -BaseYear 0 -Description "MyDescription" -Scope "MyScope" -TargetValue "MyTargetValue" -TargetYear 0 # CreateEmissionTarget | 

try {
    $Result = New-EmissionTargetApi -CreateEmissionTarget $CreateEmissionTarget
} catch {
    Write-Host ("Exception occurred when calling New-EmissionTargetApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CreateEmissionTarget** | [**CreateEmissionTarget**](CreateEmissionTarget.md)|  | 

### Return type

[**EmissionTarget**](EmissionTarget.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteEmissionEntryApi"></a>
# **Invoke-DeleteEmissionEntryApi**
> void Invoke-DeleteEmissionEntryApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteEmissionEntryApi -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteEmissionEntryApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Invoke-DeleteEmissionTargetApi"></a>
# **Invoke-DeleteEmissionTargetApi**
> void Invoke-DeleteEmissionTargetApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteEmissionTargetApi -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteEmissionTargetApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Invoke-EmissionsEntriesApi"></a>
# **Invoke-EmissionsEntriesApi**
> EmissionEntry[] Invoke-EmissionsEntriesApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-EmissionsEntriesApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-EmissionsEntriesApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**EmissionEntry[]**](EmissionEntry.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-EmissionsExportApi"></a>
# **Invoke-EmissionsExportApi**
> EmissionsExportResponse Invoke-EmissionsExportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-EmissionsExportApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-EmissionsExportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**EmissionsExportResponse**](EmissionsExportResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-EmissionsFactorsApi"></a>
# **Invoke-EmissionsFactorsApi**
> EmissionFactorResponse[] Invoke-EmissionsFactorsApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-EmissionsFactorsApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-EmissionsFactorsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**EmissionFactorResponse[]**](EmissionFactorResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-EmissionsReportApi"></a>
# **Invoke-EmissionsReportApi**
> EmissionsReport Invoke-EmissionsReportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-EmissionsReportApi -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-EmissionsReportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**EmissionsReport**](EmissionsReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-EmissionsTargetsApi"></a>
# **Invoke-EmissionsTargetsApi**
> EmissionTarget[] Invoke-EmissionsTargetsApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-EmissionsTargetsApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-EmissionsTargetsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**EmissionTarget[]**](EmissionTarget.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

