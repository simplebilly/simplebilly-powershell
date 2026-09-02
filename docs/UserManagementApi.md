# PSOpenAPITools.PSOpenAPITools\Api.UserManagementApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-User**](UserManagementApi.md#Get-User) | **GET** /api/v1/users/{user_id} | 
[**Invoke-ListUsers**](UserManagementApi.md#Invoke-ListUsers) | **GET** /api/v1/users | 
[**Remove-User**](UserManagementApi.md#Remove-User) | **DELETE** /api/v1/users/{user_id} | 
[**Update-UserPermissions**](UserManagementApi.md#Update-UserPermissions) | **PUT** /api/v1/users/{user_id}/permissions | 
[**Update-UserRole**](UserManagementApi.md#Update-UserRole) | **PUT** /api/v1/users/{user_id}/role | 


<a id="Get-User"></a>
# **Get-User**
> TenantUser Get-User<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UserId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$UserId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-User -UserId $UserId
} catch {
    Write-Host ("Exception occurred when calling Get-User: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **UserId** | **String**|  | 

### Return type

[**TenantUser**](TenantUser.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListUsers"></a>
# **Invoke-ListUsers**
> TenantUser[] Invoke-ListUsers<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListUsers
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListUsers: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TenantUser[]**](TenantUser.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Remove-User"></a>
# **Remove-User**
> void Remove-User<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UserId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$UserId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Remove-User -UserId $UserId
} catch {
    Write-Host ("Exception occurred when calling Remove-User: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **UserId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-UserPermissions"></a>
# **Update-UserPermissions**
> void Update-UserPermissions<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UserId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdatePermissionsPayload] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$UserId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$UpdatePermissionsPayload = Initialize-UpdatePermissionsPayload -Permissions "MyPermissions" # UpdatePermissionsPayload | 

try {
    $Result = Update-UserPermissions -UserId $UserId -UpdatePermissionsPayload $UpdatePermissionsPayload
} catch {
    Write-Host ("Exception occurred when calling Update-UserPermissions: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **UserId** | **String**|  | 
 **UpdatePermissionsPayload** | [**UpdatePermissionsPayload**](UpdatePermissionsPayload.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-UserRole"></a>
# **Update-UserRole**
> void Update-UserRole<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UserId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdateRolePayload] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$UserId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$UpdateRolePayload = Initialize-UpdateRolePayload -Role "MyRole" -SyncPermissions $false # UpdateRolePayload | 

try {
    $Result = Update-UserRole -UserId $UserId -UpdateRolePayload $UpdateRolePayload
} catch {
    Write-Host ("Exception occurred when calling Update-UserRole: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **UserId** | **String**|  | 
 **UpdateRolePayload** | [**UpdateRolePayload**](UpdateRolePayload.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

