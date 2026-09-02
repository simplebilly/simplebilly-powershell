# PSOpenAPITools.PSOpenAPITools\Api.TrainingsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-MyTrainings**](TrainingsApi.md#Get-MyTrainings) | **GET** /api/v1/trainings/me | 
[**Get-TrainingContent**](TrainingsApi.md#Get-TrainingContent) | **GET** /api/v1/trainings/content/{code} | 
[**Get-TrainingOverview**](TrainingsApi.md#Get-TrainingOverview) | **GET** /api/v1/trainings/overview | 
[**Submit-TrainingResult**](TrainingsApi.md#Submit-TrainingResult) | **POST** /api/v1/trainings/submit-result | 


<a id="Get-MyTrainings"></a>
# **Get-MyTrainings**
> MyTrainingItem[] Get-MyTrainings<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Get-MyTrainings
} catch {
    Write-Host ("Exception occurred when calling Get-MyTrainings: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**MyTrainingItem[]**](MyTrainingItem.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-TrainingContent"></a>
# **Get-TrainingContent**
> TrainingContent Get-TrainingContent<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Code] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Code = "MyCode" # String | Training code, e.g. data_privacy

try {
    $Result = Get-TrainingContent -Code $Code
} catch {
    Write-Host ("Exception occurred when calling Get-TrainingContent: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Code** | **String**| Training code, e.g. data_privacy | 

### Return type

[**TrainingContent**](TrainingContent.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-TrainingOverview"></a>
# **Get-TrainingOverview**
> HrTrainingOverview[] Get-TrainingOverview<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Get-TrainingOverview
} catch {
    Write-Host ("Exception occurred when calling Get-TrainingOverview: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**HrTrainingOverview[]**](HrTrainingOverview.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Submit-TrainingResult"></a>
# **Submit-TrainingResult**
> SubmitResultResponse Submit-TrainingResult<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SubmitResultDto] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SubmitResultDto = Initialize-SubmitResultDto -Answers 0 -AssignmentId "MyAssignmentId" -Score 0 -TrainingCode "MyTrainingCode" # SubmitResultDto | 

try {
    $Result = Submit-TrainingResult -SubmitResultDto $SubmitResultDto
} catch {
    Write-Host ("Exception occurred when calling Submit-TrainingResult: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SubmitResultDto** | [**SubmitResultDto**](SubmitResultDto.md)|  | 

### Return type

[**SubmitResultResponse**](SubmitResultResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

