# PSOpenAPITools.PSOpenAPITools\Api.TenantSettingsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-TenantSettings**](TenantSettingsApi.md#Get-TenantSettings) | **GET** /api/v1/settings/tenant | 
[**Update-TenantSettings**](TenantSettingsApi.md#Update-TenantSettings) | **PUT** /api/v1/settings/tenant | 


<a id="Get-TenantSettings"></a>
# **Get-TenantSettings**
> TenantSettings Get-TenantSettings<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Get-TenantSettings
} catch {
    Write-Host ("Exception occurred when calling Get-TenantSettings: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TenantSettings**](TenantSettings.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-TenantSettings"></a>
# **Update-TenantSettings**
> TenantSettings Update-TenantSettings<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdateTenantSettings] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PartialFeatureSettings = Initialize-PartialFeatureSettings -Onlineshop $false -ReportBilanz $false -ReportBwa $false -ReportEuer $false -ReportGewerbesteuer $false -ReportGuv $false -ReportKst $false -ReportUstva $false
$UpdateTenantSettings = Initialize-UpdateTenantSettings -CompanyType "gmbh" -Features $PartialFeatureSettings # UpdateTenantSettings | 

try {
    $Result = Update-TenantSettings -UpdateTenantSettings $UpdateTenantSettings
} catch {
    Write-Host ("Exception occurred when calling Update-TenantSettings: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **UpdateTenantSettings** | [**UpdateTenantSettings**](UpdateTenantSettings.md)|  | 

### Return type

[**TenantSettings**](TenantSettings.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

