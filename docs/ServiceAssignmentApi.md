# PSOpenAPITools.PSOpenAPITools\Api.ServiceAssignmentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ServiceAssignment**](ServiceAssignmentApi.md#New-ServiceAssignment) | **POST** /api/v1/service-assignments | 
[**Invoke-DeleteServiceAssignment**](ServiceAssignmentApi.md#Invoke-DeleteServiceAssignment) | **DELETE** /api/v1/service-assignments/{id} | 
[**Get-ServiceAssignment**](ServiceAssignmentApi.md#Get-ServiceAssignment) | **GET** /api/v1/service-assignments/{id} | 
[**Get-ServiceAssignments**](ServiceAssignmentApi.md#Get-ServiceAssignments) | **GET** /api/v1/service-assignments/ | 
[**Update-ServiceAssignment**](ServiceAssignmentApi.md#Update-ServiceAssignment) | **PUT** /api/v1/service-assignments/{id} | 


<a id="New-ServiceAssignment"></a>
# **New-ServiceAssignment**
> ServiceAssignment New-ServiceAssignment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ServiceAssignmentCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ServiceAssignmentCreate = Initialize-ServiceAssignmentCreate -EmployeeId "MyEmployeeId" -JobId "MyJobId" -Notes "MyNotes" -ScheduledDate (Get-Date) -ScheduledEnd "MyScheduledEnd" -ScheduledStart "MyScheduledStart" -Status "planned" # ServiceAssignmentCreate | 

try {
    $Result = New-ServiceAssignment -ServiceAssignmentCreate $ServiceAssignmentCreate
} catch {
    Write-Host ("Exception occurred when calling New-ServiceAssignment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ServiceAssignmentCreate** | [**ServiceAssignmentCreate**](ServiceAssignmentCreate.md)|  | 

### Return type

[**ServiceAssignment**](ServiceAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteServiceAssignment"></a>
# **Invoke-DeleteServiceAssignment**
> void Invoke-DeleteServiceAssignment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteServiceAssignment -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteServiceAssignment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Get-ServiceAssignment"></a>
# **Get-ServiceAssignment**
> ServiceAssignment Get-ServiceAssignment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-ServiceAssignment -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-ServiceAssignment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**ServiceAssignment**](ServiceAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ServiceAssignments"></a>
# **Get-ServiceAssignments**
> ServiceAssignment[] Get-ServiceAssignments<br>
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
    $Result = Get-ServiceAssignments -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-ServiceAssignments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**ServiceAssignment[]**](ServiceAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ServiceAssignment"></a>
# **Update-ServiceAssignment**
> ServiceAssignment Update-ServiceAssignment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ServiceAssignmentUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$ServiceAssignmentUpdate = Initialize-ServiceAssignmentUpdate -EmployeeId "MyEmployeeId" -JobId "MyJobId" -Notes "MyNotes" -ScheduledDate (Get-Date) -ScheduledEnd "MyScheduledEnd" -ScheduledStart "MyScheduledStart" -Status "planned" # ServiceAssignmentUpdate | 

try {
    $Result = Update-ServiceAssignment -Id $Id -ServiceAssignmentUpdate $ServiceAssignmentUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ServiceAssignment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **ServiceAssignmentUpdate** | [**ServiceAssignmentUpdate**](ServiceAssignmentUpdate.md)|  | 

### Return type

[**ServiceAssignment**](ServiceAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

