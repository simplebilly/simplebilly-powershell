# PSOpenAPITools.PSOpenAPITools\Api.ProposeAssignmentsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ProposeAssignmentsApi**](ProposeAssignmentsApi.md#Invoke-ProposeAssignmentsApi) | **GET** /api/v1/bookkeeping/propose-assignments | 


<a id="Invoke-ProposeAssignmentsApi"></a>
# **Invoke-ProposeAssignmentsApi**
> ProposedAssignment[] Invoke-ProposeAssignmentsApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-MinConfidence] <System.Nullable[Double]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$MinConfidence = 1.2 # Double |  (optional)
$CustomerId = "MyCustomerId" # String |  (optional)

try {
    $Result = Invoke-ProposeAssignmentsApi -MinConfidence $MinConfidence -CustomerId $CustomerId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ProposeAssignmentsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **MinConfidence** | **Double**|  | [optional] 
 **CustomerId** | **String**|  | [optional] 

### Return type

[**ProposedAssignment[]**](ProposedAssignment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

