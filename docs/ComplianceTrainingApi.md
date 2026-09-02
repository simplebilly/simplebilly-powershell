# PSOpenAPITools.PSOpenAPITools\Api.ComplianceTrainingApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ComplianceTraining**](ComplianceTrainingApi.md#New-ComplianceTraining) | **POST** /api/v1/compliance-trainings | 
[**Invoke-DeleteComplianceTraining**](ComplianceTrainingApi.md#Invoke-DeleteComplianceTraining) | **DELETE** /api/v1/compliance-trainings/{id} | 
[**Get-ComplianceTraining**](ComplianceTrainingApi.md#Get-ComplianceTraining) | **GET** /api/v1/compliance-trainings/{id} | 
[**Get-ComplianceTrainings**](ComplianceTrainingApi.md#Get-ComplianceTrainings) | **GET** /api/v1/compliance-trainings/ | 
[**Update-ComplianceTraining**](ComplianceTrainingApi.md#Update-ComplianceTraining) | **PUT** /api/v1/compliance-trainings/{id} | 


<a id="New-ComplianceTraining"></a>
# **New-ComplianceTraining**
> ComplianceTraining New-ComplianceTraining<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ComplianceTrainingCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ComplianceTrainingCreate = Initialize-ComplianceTrainingCreate -Assignable $false -Code "MyCode" -Description "MyDescription" -PassScore 0 -PluginPlatform "MyPluginPlatform" -Source "builtin" -Title "MyTitle" -ValidityMonths 0 # ComplianceTrainingCreate | 

try {
    $Result = New-ComplianceTraining -ComplianceTrainingCreate $ComplianceTrainingCreate
} catch {
    Write-Host ("Exception occurred when calling New-ComplianceTraining: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ComplianceTrainingCreate** | [**ComplianceTrainingCreate**](ComplianceTrainingCreate.md)|  | 

### Return type

[**ComplianceTraining**](ComplianceTraining.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteComplianceTraining"></a>
# **Invoke-DeleteComplianceTraining**
> void Invoke-DeleteComplianceTraining<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteComplianceTraining -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteComplianceTraining: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Get-ComplianceTraining"></a>
# **Get-ComplianceTraining**
> ComplianceTraining Get-ComplianceTraining<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-ComplianceTraining -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-ComplianceTraining: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**ComplianceTraining**](ComplianceTraining.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ComplianceTrainings"></a>
# **Get-ComplianceTrainings**
> ComplianceTraining[] Get-ComplianceTrainings<br>
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
    $Result = Get-ComplianceTrainings -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-ComplianceTrainings: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**ComplianceTraining[]**](ComplianceTraining.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ComplianceTraining"></a>
# **Update-ComplianceTraining**
> ComplianceTraining Update-ComplianceTraining<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ComplianceTrainingUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$ComplianceTrainingUpdate = Initialize-ComplianceTrainingUpdate -Assignable $false -Code "MyCode" -Description "MyDescription" -PassScore 0 -PluginPlatform "MyPluginPlatform" -Source "builtin" -Title "MyTitle" -ValidityMonths 0 # ComplianceTrainingUpdate | 

try {
    $Result = Update-ComplianceTraining -Id $Id -ComplianceTrainingUpdate $ComplianceTrainingUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ComplianceTraining: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **ComplianceTrainingUpdate** | [**ComplianceTrainingUpdate**](ComplianceTrainingUpdate.md)|  | 

### Return type

[**ComplianceTraining**](ComplianceTraining.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

