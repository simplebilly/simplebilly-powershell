# PSOpenAPITools.PSOpenAPITools\Api.JobApplicationApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ApplyPublic**](JobApplicationApi.md#Invoke-ApplyPublic) | **POST** /api/v1/public/jobs/{posting_id}/apply | 
[**Invoke-DeleteJobApplication**](JobApplicationApi.md#Invoke-DeleteJobApplication) | **DELETE** /api/v1/job-applications/{application_id} | 
[**Invoke-DownloadCv**](JobApplicationApi.md#Invoke-DownloadCv) | **GET** /api/v1/job-applications/{application_id}/cv | 
[**Get-JobApplication**](JobApplicationApi.md#Get-JobApplication) | **GET** /api/v1/job-applications/{application_id} | 
[**ConvertTo-boundEmail**](JobApplicationApi.md#ConvertTo-boundEmail) | **POST** /api/v1/public/jobs/inbound-email | Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with &#x60;from&#x60;, &#x60;subject&#x60;, &#x60;body-plain&#x60; and one or more &#x60;attachment-N&#x60; file fields. The subject may reference a posting as &#x60;[JOB-&lt;posting_id&gt;]&#x60;; without one the application lands in the general inbox.
[**Invoke-ListJobApplications**](JobApplicationApi.md#Invoke-ListJobApplications) | **GET** /api/v1/job-applications | 
[**Invoke-ListPublicPostings**](JobApplicationApi.md#Invoke-ListPublicPostings) | **GET** /api/v1/public/jobs | 
[**Invoke-ScoreJobApplication**](JobApplicationApi.md#Invoke-ScoreJobApplication) | **POST** /api/v1/job-applications/{application_id}/score | 
[**Update-JobApplicationStatus**](JobApplicationApi.md#Update-JobApplicationStatus) | **PATCH** /api/v1/job-applications/{application_id}/status | 


<a id="Invoke-ApplyPublic"></a>
# **Invoke-ApplyPublic**
> void Invoke-ApplyPublic<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PostingId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PostingId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-ApplyPublic -PostingId $PostingId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ApplyPublic: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PostingId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteJobApplication"></a>
# **Invoke-DeleteJobApplication**
> JobApplication Invoke-DeleteJobApplication<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ApplicationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ApplicationId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteJobApplication -ApplicationId $ApplicationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteJobApplication: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ApplicationId** | **String**|  | 

### Return type

[**JobApplication**](JobApplication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DownloadCv"></a>
# **Invoke-DownloadCv**
> void Invoke-DownloadCv<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ApplicationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ApplicationId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DownloadCv -ApplicationId $ApplicationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DownloadCv: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ApplicationId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-JobApplication"></a>
# **Get-JobApplication**
> JobApplication Get-JobApplication<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ApplicationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ApplicationId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-JobApplication -ApplicationId $ApplicationId
} catch {
    Write-Host ("Exception occurred when calling Get-JobApplication: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ApplicationId** | **String**|  | 

### Return type

[**JobApplication**](JobApplication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="ConvertTo-boundEmail"></a>
# **ConvertTo-boundEmail**
> void ConvertTo-boundEmail<br>

Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with `from`, `subject`, `body-plain` and one or more `attachment-N` file fields. The subject may reference a posting as `[JOB-<posting_id>]`; without one the application lands in the general inbox.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Inbound CV email, mailgun/sendgrid inbound-parse style: multipart form with `from`, `subject`, `body-plain` and one or more `attachment-N` file fields. The subject may reference a posting as `[JOB-<posting_id>]`; without one the application lands in the general inbox.
try {
    $Result = ConvertTo-boundEmail
} catch {
    Write-Host ("Exception occurred when calling ConvertTo-boundEmail: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Invoke-ListJobApplications"></a>
# **Invoke-ListJobApplications**
> JobApplication[] Invoke-ListJobApplications<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PostingId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PostingId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String |  (optional)
$Status = "MyStatus" # String |  (optional)
$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)

try {
    $Result = Invoke-ListJobApplications -PostingId $PostingId -Status $Status -Page $Page -PageSize $PageSize
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListJobApplications: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PostingId** | **String**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 

### Return type

[**JobApplication[]**](JobApplication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListPublicPostings"></a>
# **Invoke-ListPublicPostings**
> PublicPosting[] Invoke-ListPublicPostings<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListPublicPostings
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListPublicPostings: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PublicPosting[]**](PublicPosting.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ScoreJobApplication"></a>
# **Invoke-ScoreJobApplication**
> JobApplication Invoke-ScoreJobApplication<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ApplicationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ApplicationId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-ScoreJobApplication -ApplicationId $ApplicationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ScoreJobApplication: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ApplicationId** | **String**|  | 

### Return type

[**JobApplication**](JobApplication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-JobApplicationStatus"></a>
# **Update-JobApplicationStatus**
> JobApplication Update-JobApplicationStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ApplicationId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ApplicationStatusDto] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ApplicationId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$ApplicationStatusDto = Initialize-ApplicationStatusDto -PostingId "MyPostingId" -Status "MyStatus" # ApplicationStatusDto | 

try {
    $Result = Update-JobApplicationStatus -ApplicationId $ApplicationId -ApplicationStatusDto $ApplicationStatusDto
} catch {
    Write-Host ("Exception occurred when calling Update-JobApplicationStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ApplicationId** | **String**|  | 
 **ApplicationStatusDto** | [**ApplicationStatusDto**](ApplicationStatusDto.md)|  | 

### Return type

[**JobApplication**](JobApplication.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

