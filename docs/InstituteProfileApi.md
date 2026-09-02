# PSOpenAPITools.PSOpenAPITools\Api.InstituteProfileApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-InstituteProfile**](InstituteProfileApi.md#Get-InstituteProfile) | **GET** /api/v1/institute-profile | Current institute profile (created with defaults when missing).
[**Update-InstituteProfile**](InstituteProfileApi.md#Update-InstituteProfile) | **PUT** /api/v1/institute-profile | Update the institute profile (institute_type and/or kapitalmarktorientiert).


<a id="Get-InstituteProfile"></a>
# **Get-InstituteProfile**
> InstituteProfile Get-InstituteProfile<br>

Current institute profile (created with defaults when missing).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Current institute profile (created with defaults when missing).
try {
    $Result = Get-InstituteProfile
} catch {
    Write-Host ("Exception occurred when calling Get-InstituteProfile: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InstituteProfile**](InstituteProfile.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-InstituteProfile"></a>
# **Update-InstituteProfile**
> InstituteProfile Update-InstituteProfile<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InstituteProfileUpdate] <PSCustomObject><br>

Update the institute profile (institute_type and/or kapitalmarktorientiert).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$InstituteProfileUpdate = Initialize-InstituteProfileUpdate -InstituteType "MyInstituteType" -Kapitalmarktorientiert $false # InstituteProfileUpdate | 

# Update the institute profile (institute_type and/or kapitalmarktorientiert).
try {
    $Result = Update-InstituteProfile -InstituteProfileUpdate $InstituteProfileUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-InstituteProfile: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **InstituteProfileUpdate** | [**InstituteProfileUpdate**](InstituteProfileUpdate.md)|  | 

### Return type

[**InstituteProfile**](InstituteProfile.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

