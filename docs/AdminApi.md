# PSOpenAPITools.PSOpenAPITools\Api.AdminApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-TriggerMirror**](AdminApi.md#Invoke-TriggerMirror) | **POST** /api/v1/admin/storage/mirror | 


<a id="Invoke-TriggerMirror"></a>
# **Invoke-TriggerMirror**
> MirrorTriggerResponse Invoke-TriggerMirror<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-TriggerMirror
} catch {
    Write-Host ("Exception occurred when calling Invoke-TriggerMirror: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**MirrorTriggerResponse**](MirrorTriggerResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

