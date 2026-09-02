# PSOpenAPITools.PSOpenAPITools\Api.ImportRunnerApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-ImportStatus**](ImportRunnerApi.md#Get-ImportStatus) | **GET** /api/v1/import/{job_id} | 
[**Start-Import**](ImportRunnerApi.md#Start-Import) | **POST** /api/v1/import/start | 
[**Test-ImportConnection**](ImportRunnerApi.md#Test-ImportConnection) | **POST** /api/v1/import/test | 


<a id="Get-ImportStatus"></a>
# **Get-ImportStatus**
> ImportJobStatus Get-ImportStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-JobId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$JobId = "MyJobId" # String | 

try {
    $Result = Get-ImportStatus -JobId $JobId
} catch {
    Write-Host ("Exception occurred when calling Get-ImportStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **JobId** | **String**|  | 

### Return type

[**ImportJobStatus**](ImportJobStatus.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Start-Import"></a>
# **Start-Import**
> ImportStartResponse Start-Import<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ImportStartRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ImportStartRequest = Initialize-ImportStartRequest -ApiKey "MyApiKey" -Provider "MyProvider" -Years 0 # ImportStartRequest | 

try {
    $Result = Start-Import -ImportStartRequest $ImportStartRequest
} catch {
    Write-Host ("Exception occurred when calling Start-Import: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ImportStartRequest** | [**ImportStartRequest**](ImportStartRequest.md)|  | 

### Return type

[**ImportStartResponse**](ImportStartResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Test-ImportConnection"></a>
# **Test-ImportConnection**
> ImportTestResponse Test-ImportConnection<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ImportTestRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ImportTestRequest = Initialize-ImportTestRequest -ApiKey "MyApiKey" -Provider "MyProvider" # ImportTestRequest | 

try {
    $Result = Test-ImportConnection -ImportTestRequest $ImportTestRequest
} catch {
    Write-Host ("Exception occurred when calling Test-ImportConnection: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ImportTestRequest** | [**ImportTestRequest**](ImportTestRequest.md)|  | 

### Return type

[**ImportTestResponse**](ImportTestResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

