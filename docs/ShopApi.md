# PSOpenAPITools.PSOpenAPITools\Api.ShopApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ShopEditorSave**](ShopApi.md#Invoke-ShopEditorSave) | **POST** /api/v1/shop/editor | 


<a id="Invoke-ShopEditorSave"></a>
# **Invoke-ShopEditorSave**
> AnyType Invoke-ShopEditorSave<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = Invoke-ShopEditorSave -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-ShopEditorSave: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

