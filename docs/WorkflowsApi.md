# PSOpenAPITools.PSOpenAPITools\Api.WorkflowsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ListWorkflowsApi**](WorkflowsApi.md#Invoke-ListWorkflowsApi) | **GET** /api/v1/workflows | 
[**Set-WorkflowEnabledApi**](WorkflowsApi.md#Set-WorkflowEnabledApi) | **PUT** /api/v1/workflows/{workflow_id}/enabled | 


<a id="Invoke-ListWorkflowsApi"></a>
# **Invoke-ListWorkflowsApi**
> Workflow[] Invoke-ListWorkflowsApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListWorkflowsApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListWorkflowsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Workflow[]**](Workflow.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Set-WorkflowEnabledApi"></a>
# **Set-WorkflowEnabledApi**
> Workflow Set-WorkflowEnabledApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WorkflowId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WorkflowEnabledUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WorkflowId = "MyWorkflowId" # String | 
$WorkflowEnabledUpdate = Initialize-WorkflowEnabledUpdate -Enabled $false # WorkflowEnabledUpdate | 

try {
    $Result = Set-WorkflowEnabledApi -WorkflowId $WorkflowId -WorkflowEnabledUpdate $WorkflowEnabledUpdate
} catch {
    Write-Host ("Exception occurred when calling Set-WorkflowEnabledApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WorkflowId** | **String**|  | 
 **WorkflowEnabledUpdate** | [**WorkflowEnabledUpdate**](WorkflowEnabledUpdate.md)|  | 

### Return type

[**Workflow**](Workflow.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

