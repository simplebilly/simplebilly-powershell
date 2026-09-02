# PSOpenAPITools.PSOpenAPITools\Api.TrainingAssignmentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-TrainingAssignment**](TrainingAssignmentApi.md#New-TrainingAssignment) | **POST** /api/v1/training-assignments | 
[**Invoke-DeleteTrainingAssignment**](TrainingAssignmentApi.md#Invoke-DeleteTrainingAssignment) | **DELETE** /api/v1/training-assignments/{id} | 
[**Get-TrainingAssignment**](TrainingAssignmentApi.md#Get-TrainingAssignment) | **GET** /api/v1/training-assignments/{id} | 
[**Get-TrainingAssignments**](TrainingAssignmentApi.md#Get-TrainingAssignments) | **GET** /api/v1/training-assignments/ | 
[**Update-TrainingAssignment**](TrainingAssignmentApi.md#Update-TrainingAssignment) | **PUT** /api/v1/training-assignments/{id} | 


<a id="New-TrainingAssignment"></a>
# **New-TrainingAssignment**
> TrainingAssignment New-TrainingAssignment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TrainingAssignmentCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TrainingAssignmentCreate = Initialize-TrainingAssignmentCreate -AssignedBy "MyAssignedBy" -DueDate (Get-Date) -EmployeeId "MyEmployeeId" -Notes "MyNotes" -Status "required" -TrainingId "MyTrainingId" # TrainingAssignmentCreate | 

try {
    $Result = New-TrainingAssignment -TrainingAssignmentCreate $TrainingAssignmentCreate
} catch {
    Write-Host ("Exception occurred when calling New-TrainingAssignment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TrainingAssignmentCreate** | [**TrainingAssignmentCreate**](TrainingAssignmentCreate.md)|  | 

### Return type

[**TrainingAssignment**](TrainingAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteTrainingAssignment"></a>
# **Invoke-DeleteTrainingAssignment**
> void Invoke-DeleteTrainingAssignment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteTrainingAssignment -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteTrainingAssignment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Get-TrainingAssignment"></a>
# **Get-TrainingAssignment**
> TrainingAssignment Get-TrainingAssignment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-TrainingAssignment -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-TrainingAssignment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**TrainingAssignment**](TrainingAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-TrainingAssignments"></a>
# **Get-TrainingAssignments**
> TrainingAssignment[] Get-TrainingAssignments<br>
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
    $Result = Get-TrainingAssignments -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-TrainingAssignments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**TrainingAssignment[]**](TrainingAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-TrainingAssignment"></a>
# **Update-TrainingAssignment**
> TrainingAssignment Update-TrainingAssignment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TrainingAssignmentUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$TrainingAssignmentUpdate = Initialize-TrainingAssignmentUpdate -AssignedBy "MyAssignedBy" -DueDate (Get-Date) -EmployeeId "MyEmployeeId" -Notes "MyNotes" -Status "required" -TrainingId "MyTrainingId" # TrainingAssignmentUpdate | 

try {
    $Result = Update-TrainingAssignment -Id $Id -TrainingAssignmentUpdate $TrainingAssignmentUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-TrainingAssignment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **TrainingAssignmentUpdate** | [**TrainingAssignmentUpdate**](TrainingAssignmentUpdate.md)|  | 

### Return type

[**TrainingAssignment**](TrainingAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

