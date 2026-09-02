# PSOpenAPITools.PSOpenAPITools\Api.PeppolApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-PeppolApi**](PeppolApi.md#Invoke-PeppolApi) | **GET** /api/v1/invoices/{id}/peppol | 


<a id="Invoke-PeppolApi"></a>
# **Invoke-PeppolApi**
> PeppolResponse Invoke-PeppolApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 

try {
    $Result = Invoke-PeppolApi -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PeppolApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**PeppolResponse**](PeppolResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

