# PSOpenAPITools.PSOpenAPITools\Api.AuthApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Receive-Invite**](AuthApi.md#Receive-Invite) | **POST** /auth/accept-invite | Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
[**Invoke-ForgotPassword**](AuthApi.md#Invoke-ForgotPassword) | **POST** /auth/forgot-password | Send a password reset email to the user
[**Invoke-Login**](AuthApi.md#Invoke-Login) | **POST** /auth/login | Authenticate a user with email + password (optional TOTP)
[**Invoke-Logout**](AuthApi.md#Invoke-Logout) | **POST** /auth/logout | Log out the current user (kills the assay session)
[**Invoke-MagicLinkLogin**](AuthApi.md#Invoke-MagicLinkLogin) | **POST** /auth/magic-link | Request a magic link login (sends an email with a one-time link)
[**Invoke-MagicLinkVerify**](AuthApi.md#Invoke-MagicLinkVerify) | **POST** /auth/magic-link/verify | Verify a magic link token and log the user in
[**Register-**](AuthApi.md#Register-) | **POST** /auth/register | Register a new user account
[**Reset-Password**](AuthApi.md#Reset-Password) | **POST** /auth/reset-password | Reset the user&#39;s password using a reset token
[**Invoke-TotpEnable**](AuthApi.md#Invoke-TotpEnable) | **POST** /auth/totp/enable | Enable TOTP two-factor authentication by verifying a code
[**Invoke-TotpSetup**](AuthApi.md#Invoke-TotpSetup) | **GET** /auth/totp/setup | Set up TOTP two-factor authentication (generates secret + backup codes)
[**Test-Email**](AuthApi.md#Test-Email) | **POST** /auth/verify-email | Verify a user&#39;s email address using a verification token


<a id="Receive-Invite"></a>
# **Receive-Invite**
> void Receive-Invite<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AcceptInviteRequest] <PSCustomObject><br>

Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AcceptInviteRequest = Initialize-AcceptInviteRequest -FirstName "MyFirstName" -LastName "MyLastName" -Password "MyPassword" -PrivacyAccepted $false -Token "MyToken" # AcceptInviteRequest | 

# Accept an invite: create the account (or reuse an existing one) and join the inviting tenant. The invite token proves control of the mailbox.
try {
    $Result = Receive-Invite -AcceptInviteRequest $AcceptInviteRequest
} catch {
    Write-Host ("Exception occurred when calling Receive-Invite: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AcceptInviteRequest** | [**AcceptInviteRequest**](AcceptInviteRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ForgotPassword"></a>
# **Invoke-ForgotPassword**
> void Invoke-ForgotPassword<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ForgotPasswordRequest] <PSCustomObject><br>

Send a password reset email to the user

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ForgotPasswordRequest = Initialize-ForgotPasswordRequest -Email "MyEmail" # ForgotPasswordRequest | 

# Send a password reset email to the user
try {
    $Result = Invoke-ForgotPassword -ForgotPasswordRequest $ForgotPasswordRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-ForgotPassword: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ForgotPasswordRequest** | [**ForgotPasswordRequest**](ForgotPasswordRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-Login"></a>
# **Invoke-Login**
> AuthResponse Invoke-Login<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-LoginRequest] <PSCustomObject><br>

Authenticate a user with email + password (optional TOTP)

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$LoginRequest = Initialize-LoginRequest -Email "MyEmail" -Password "MyPassword" -TotpCode "MyTotpCode" # LoginRequest | 

# Authenticate a user with email + password (optional TOTP)
try {
    $Result = Invoke-Login -LoginRequest $LoginRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-Login: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **LoginRequest** | [**LoginRequest**](LoginRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-Logout"></a>
# **Invoke-Logout**
> void Invoke-Logout<br>

Log out the current user (kills the assay session)

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Log out the current user (kills the assay session)
try {
    $Result = Invoke-Logout
} catch {
    Write-Host ("Exception occurred when calling Invoke-Logout: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-MagicLinkLogin"></a>
# **Invoke-MagicLinkLogin**
> void Invoke-MagicLinkLogin<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-MagicLinkRequest] <PSCustomObject><br>

Request a magic link login (sends an email with a one-time link)

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$MagicLinkRequest = Initialize-MagicLinkRequest -Email "MyEmail" # MagicLinkRequest | 

# Request a magic link login (sends an email with a one-time link)
try {
    $Result = Invoke-MagicLinkLogin -MagicLinkRequest $MagicLinkRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-MagicLinkLogin: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **MagicLinkRequest** | [**MagicLinkRequest**](MagicLinkRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-MagicLinkVerify"></a>
# **Invoke-MagicLinkVerify**
> AuthResponse Invoke-MagicLinkVerify<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-MagicLinkVerifyRequest] <PSCustomObject><br>

Verify a magic link token and log the user in

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$MagicLinkVerifyRequest = Initialize-MagicLinkVerifyRequest -Token "MyToken" # MagicLinkVerifyRequest | 

# Verify a magic link token and log the user in
try {
    $Result = Invoke-MagicLinkVerify -MagicLinkVerifyRequest $MagicLinkVerifyRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-MagicLinkVerify: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **MagicLinkVerifyRequest** | [**MagicLinkVerifyRequest**](MagicLinkVerifyRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Register-"></a>
# **Register-**
> AuthResponse Register-<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RegisterRequest] <PSCustomObject><br>

Register a new user account

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RegisterRequest = Initialize-RegisterRequest -CompanyName "MyCompanyName" -Email "MyEmail" -FirstName "MyFirstName" -LastName "MyLastName" -Password "MyPassword" -PrivacyAccepted $false # RegisterRequest | 

# Register a new user account
try {
    $Result = Register- -RegisterRequest $RegisterRequest
} catch {
    Write-Host ("Exception occurred when calling Register-: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RegisterRequest** | [**RegisterRequest**](RegisterRequest.md)|  | 

### Return type

[**AuthResponse**](AuthResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Reset-Password"></a>
# **Reset-Password**
> void Reset-Password<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ResetPasswordRequest] <PSCustomObject><br>

Reset the user's password using a reset token

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ResetPasswordRequest = Initialize-ResetPasswordRequest -NewPassword "MyNewPassword" -Token "MyToken" # ResetPasswordRequest | 

# Reset the user's password using a reset token
try {
    $Result = Reset-Password -ResetPasswordRequest $ResetPasswordRequest
} catch {
    Write-Host ("Exception occurred when calling Reset-Password: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ResetPasswordRequest** | [**ResetPasswordRequest**](ResetPasswordRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-TotpEnable"></a>
# **Invoke-TotpEnable**
> void Invoke-TotpEnable<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TotpEnableRequest] <PSCustomObject><br>

Enable TOTP two-factor authentication by verifying a code

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TotpEnableRequest = Initialize-TotpEnableRequest -Code "MyCode" # TotpEnableRequest | 

# Enable TOTP two-factor authentication by verifying a code
try {
    $Result = Invoke-TotpEnable -TotpEnableRequest $TotpEnableRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-TotpEnable: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TotpEnableRequest** | [**TotpEnableRequest**](TotpEnableRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-TotpSetup"></a>
# **Invoke-TotpSetup**
> TotpSetupResponse Invoke-TotpSetup<br>

Set up TOTP two-factor authentication (generates secret + backup codes)

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Set up TOTP two-factor authentication (generates secret + backup codes)
try {
    $Result = Invoke-TotpSetup
} catch {
    Write-Host ("Exception occurred when calling Invoke-TotpSetup: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**TotpSetupResponse**](TotpSetupResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Test-Email"></a>
# **Test-Email**
> void Test-Email<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VerifyEmailRequest] <PSCustomObject><br>

Verify a user's email address using a verification token

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VerifyEmailRequest = Initialize-VerifyEmailRequest -Token "MyToken" # VerifyEmailRequest | 

# Verify a user's email address using a verification token
try {
    $Result = Test-Email -VerifyEmailRequest $VerifyEmailRequest
} catch {
    Write-Host ("Exception occurred when calling Test-Email: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VerifyEmailRequest** | [**VerifyEmailRequest**](VerifyEmailRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

