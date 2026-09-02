# PSOpenAPITools.PSOpenAPITools\Api.UserApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Rename-Password**](UserApi.md#Rename-Password) | **POST** /user/change-password | Change the current user&#39;s password (requires the current password).
[**New-Team**](UserApi.md#New-Team) | **POST** /user/teams | Create a new team within the current tenant
[**New-ApiKey**](UserApi.md#New-ApiKey) | **POST** /user/api-key | Generate a new API key for the current user
[**ConvertTo-viteUser**](UserApi.md#ConvertTo-viteUser) | **POST** /user/invite | Invite a user to the current tenant/organization
[**Invoke-ListTeams**](UserApi.md#Invoke-ListTeams) | **GET** /user/teams | List all teams in the current tenant
[**Remove-UserFromOrg**](UserApi.md#Remove-UserFromOrg) | **DELETE** /user/remove | Remove a user from the current organization
[**Update-Profile**](UserApi.md#Update-Profile) | **PUT** /user/profile | Update the current user&#39;s profile
[**Use-rProfile**](UserApi.md#Use-rProfile) | **GET** /user/profile | Get the current user&#39;s profile
[**Use-rTenants**](UserApi.md#Use-rTenants) | **GET** /user/tenants | List all tenants (organizations) the current user belongs to


<a id="Rename-Password"></a>
# **Rename-Password**
> void Rename-Password<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ChangePasswordRequest] <PSCustomObject><br>

Change the current user's password (requires the current password).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ChangePasswordRequest = Initialize-ChangePasswordRequest -CurrentPassword "MyCurrentPassword" -NewPassword "MyNewPassword" # ChangePasswordRequest | 

# Change the current user's password (requires the current password).
try {
    $Result = Rename-Password -ChangePasswordRequest $ChangePasswordRequest
} catch {
    Write-Host ("Exception occurred when calling Rename-Password: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ChangePasswordRequest** | [**ChangePasswordRequest**](ChangePasswordRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-Team"></a>
# **New-Team**
> ApiResponseTeam New-Team<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TeamCreate] <PSCustomObject><br>

Create a new team within the current tenant

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TeamCreate = Initialize-TeamCreate -Description "MyDescription" -Name "MyName" -ParentTeamId "MyParentTeamId" # TeamCreate | 

# Create a new team within the current tenant
try {
    $Result = New-Team -TeamCreate $TeamCreate
} catch {
    Write-Host ("Exception occurred when calling New-Team: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TeamCreate** | [**TeamCreate**](TeamCreate.md)|  | 

### Return type

[**ApiResponseTeam**](ApiResponseTeam.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-ApiKey"></a>
# **New-ApiKey**
> ApiResponseString New-ApiKey<br>

Generate a new API key for the current user

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Generate a new API key for the current user
try {
    $Result = New-ApiKey
} catch {
    Write-Host ("Exception occurred when calling New-ApiKey: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseString**](ApiResponseString.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="ConvertTo-viteUser"></a>
# **ConvertTo-viteUser**
> void ConvertTo-viteUser<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InviteRequest] <PSCustomObject><br>

Invite a user to the current tenant/organization

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$InviteRequest = Initialize-InviteRequest -Email "MyEmail" # InviteRequest | 

# Invite a user to the current tenant/organization
try {
    $Result = ConvertTo-viteUser -InviteRequest $InviteRequest
} catch {
    Write-Host ("Exception occurred when calling ConvertTo-viteUser: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **InviteRequest** | [**InviteRequest**](InviteRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListTeams"></a>
# **Invoke-ListTeams**
> ApiResponseVecTeam Invoke-ListTeams<br>

List all teams in the current tenant

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# List all teams in the current tenant
try {
    $Result = Invoke-ListTeams
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListTeams: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseVecTeam**](ApiResponseVecTeam.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Remove-UserFromOrg"></a>
# **Remove-UserFromOrg**
> void Remove-UserFromOrg<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RemoveUserRequest] <PSCustomObject><br>

Remove a user from the current organization

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RemoveUserRequest = Initialize-RemoveUserRequest -Email "MyEmail" # RemoveUserRequest | 

# Remove a user from the current organization
try {
    $Result = Remove-UserFromOrg -RemoveUserRequest $RemoveUserRequest
} catch {
    Write-Host ("Exception occurred when calling Remove-UserFromOrg: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RemoveUserRequest** | [**RemoveUserRequest**](RemoveUserRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Profile"></a>
# **Update-Profile**
> void Update-Profile<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-UpdateProfileRequest] <PSCustomObject><br>

Update the current user's profile

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$UpdateProfileRequest = Initialize-UpdateProfileRequest -AvatarUrl "MyAvatarUrl" -FirstName "MyFirstName" -LastName "MyLastName" -Name "MyName" # UpdateProfileRequest | 

# Update the current user's profile
try {
    $Result = Update-Profile -UpdateProfileRequest $UpdateProfileRequest
} catch {
    Write-Host ("Exception occurred when calling Update-Profile: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **UpdateProfileRequest** | [**UpdateProfileRequest**](UpdateProfileRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Use-rProfile"></a>
# **Use-rProfile**
> ApiResponseUserProfile Use-rProfile<br>

Get the current user's profile

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Get the current user's profile
try {
    $Result = Use-rProfile
} catch {
    Write-Host ("Exception occurred when calling Use-rProfile: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseUserProfile**](ApiResponseUserProfile.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Use-rTenants"></a>
# **Use-rTenants**
> ApiResponseVecUserTenantInfo Use-rTenants<br>

List all tenants (organizations) the current user belongs to

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# List all tenants (organizations) the current user belongs to
try {
    $Result = Use-rTenants
} catch {
    Write-Host ("Exception occurred when calling Use-rTenants: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ApiResponseVecUserTenantInfo**](ApiResponseVecUserTenantInfo.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

