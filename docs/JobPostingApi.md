# PSOpenAPITools.PSOpenAPITools\Api.JobPostingApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-JobPosting**](JobPostingApi.md#New-JobPosting) | **POST** /api/v1/job-postings | 
[**Invoke-DeleteJobPosting**](JobPostingApi.md#Invoke-DeleteJobPosting) | **DELETE** /api/v1/job-postings/{id} | 
[**Get-JobPosting**](JobPostingApi.md#Get-JobPosting) | **GET** /api/v1/job-postings/{id} | 
[**Invoke-ListJobPostings**](JobPostingApi.md#Invoke-ListJobPostings) | **GET** /api/v1/job-postings | 
[**Update-JobPosting**](JobPostingApi.md#Update-JobPosting) | **PUT** /api/v1/job-postings/{id} | 


<a id="New-JobPosting"></a>
# **New-JobPosting**
> JobPosting New-JobPosting<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-JobPostingCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$JobPostingCreate = Initialize-JobPostingCreate -Currency "MyCurrency" -Department "MyDepartment" -Description "MyDescription" -EmploymentType "fulltime" -Location "MyLocation" -Remote $false -RequiredSkills  -Requirements "MyRequirements" -SalaryMax 0 -SalaryMin 0 -Status "draft" -Title "MyTitle" # JobPostingCreate | 

try {
    $Result = New-JobPosting -JobPostingCreate $JobPostingCreate
} catch {
    Write-Host ("Exception occurred when calling New-JobPosting: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobPostingCreate** | [**JobPostingCreate**](JobPostingCreate.md)|  | 

### Return type

[**JobPosting**](JobPosting.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteJobPosting"></a>
# **Invoke-DeleteJobPosting**
> void Invoke-DeleteJobPosting<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteJobPosting -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteJobPosting: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Get-JobPosting"></a>
# **Get-JobPosting**
> JobPosting Get-JobPosting<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-JobPosting -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-JobPosting: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**JobPosting**](JobPosting.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListJobPostings"></a>
# **Invoke-ListJobPostings**
> JobPosting[] Invoke-ListJobPostings<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Status = "MyStatus" # String |  (optional)
$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)

try {
    $Result = Invoke-ListJobPostings -Status $Status -Page $Page -PageSize $PageSize
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListJobPostings: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Status** | **String**|  | [optional] 
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 

### Return type

[**JobPosting[]**](JobPosting.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-JobPosting"></a>
# **Update-JobPosting**
> JobPosting Update-JobPosting<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-JobPostingUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$JobPostingUpdate = Initialize-JobPostingUpdate -Currency "MyCurrency" -Department "MyDepartment" -Description "MyDescription" -EmploymentType "fulltime" -Location "MyLocation" -Remote $false -RequiredSkills  -Requirements "MyRequirements" -SalaryMax 0 -SalaryMin 0 -Status "draft" -Title "MyTitle" # JobPostingUpdate | 

try {
    $Result = Update-JobPosting -Id $Id -JobPostingUpdate $JobPostingUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-JobPosting: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **JobPostingUpdate** | [**JobPostingUpdate**](JobPostingUpdate.md)|  | 

### Return type

[**JobPosting**](JobPosting.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

