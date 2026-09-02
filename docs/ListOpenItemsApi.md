# PSOpenAPITools.PSOpenAPITools\Api.ListOpenItemsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ListOpenItemsApi**](ListOpenItemsApi.md#Invoke-ListOpenItemsApi) | **GET** /api/v1/bookkeeping/open-items | 


<a id="Invoke-ListOpenItemsApi"></a>
# **Invoke-ListOpenItemsApi**
> OpenItem[] Invoke-ListOpenItemsApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReminderLevel1Days] <System.Nullable[Int64]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReminderLevel2Days] <System.Nullable[Int64]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReminderLevel3Days] <System.Nullable[Int64]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ReminderLevel1Days = 789 # Int64 |  (optional)
$ReminderLevel2Days = 789 # Int64 |  (optional)
$ReminderLevel3Days = 789 # Int64 |  (optional)
$CustomerId = "MyCustomerId" # String |  (optional)

try {
    $Result = Invoke-ListOpenItemsApi -ReminderLevel1Days $ReminderLevel1Days -ReminderLevel2Days $ReminderLevel2Days -ReminderLevel3Days $ReminderLevel3Days -CustomerId $CustomerId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListOpenItemsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ReminderLevel1Days** | **Int64**|  | [optional] 
 **ReminderLevel2Days** | **Int64**|  | [optional] 
 **ReminderLevel3Days** | **Int64**|  | [optional] 
 **CustomerId** | **String**|  | [optional] 

### Return type

[**OpenItem[]**](OpenItem.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

