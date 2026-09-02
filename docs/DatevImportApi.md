# PSOpenAPITools.PSOpenAPITools\Api.DatevImportApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-DatevImportApi**](DatevImportApi.md#Invoke-DatevImportApi) | **POST** /api/v1/bookkeeping/datev/import | 


<a id="Invoke-DatevImportApi"></a>
# **Invoke-DatevImportApi**
> DatevImportResponse Invoke-DatevImportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = Invoke-DatevImportApi -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-DatevImportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**DatevImportResponse**](DatevImportResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

