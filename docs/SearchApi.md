# PSOpenAPITools.PSOpenAPITools\Api.SearchApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-GlobalSearch**](SearchApi.md#Invoke-GlobalSearch) | **GET** /api/v1/search | GET /api/v1/search?q&#x3D;...
[**Invoke-MyPermissions**](SearchApi.md#Invoke-MyPermissions) | **GET** /api/v1/me/permissions | GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.


<a id="Invoke-GlobalSearch"></a>
# **Invoke-GlobalSearch**
> AnyType Invoke-GlobalSearch<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Q] <String><br>

GET /api/v1/search?q=...

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Q = "MyQ" # String | Search text (min 2 chars)

# GET /api/v1/search?q=...
try {
    $Result = Invoke-GlobalSearch -Q $Q
} catch {
    Write-Host ("Exception occurred when calling Invoke-GlobalSearch: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Q** | **String**| Search text (min 2 chars) | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-MyPermissions"></a>
# **Invoke-MyPermissions**
> AnyType Invoke-MyPermissions<br>

GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# GET /api/v1/me/permissions — resolved permissions from the auth token, used by the frontend to show/hide admin navigation.
try {
    $Result = Invoke-MyPermissions
} catch {
    Write-Host ("Exception occurred when calling Invoke-MyPermissions: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

