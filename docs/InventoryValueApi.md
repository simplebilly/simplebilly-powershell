# PSOpenAPITools.PSOpenAPITools\Api.InventoryValueApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-InventoryValueApi**](InventoryValueApi.md#Get-InventoryValueApi) | **GET** /api/v1/bookkeeping/inventory-value | 
[**Invoke-RecordInventoryValueApi**](InventoryValueApi.md#Invoke-RecordInventoryValueApi) | **POST** /api/v1/bookkeeping/inventory-value/record | 


<a id="Get-InventoryValueApi"></a>
# **Get-InventoryValueApi**
> CurrentInventoryValue Get-InventoryValueApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Get-InventoryValueApi
} catch {
    Write-Host ("Exception occurred when calling Get-InventoryValueApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**CurrentInventoryValue**](CurrentInventoryValue.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-RecordInventoryValueApi"></a>
# **Invoke-RecordInventoryValueApi**
> InventoryValuePoint Invoke-RecordInventoryValueApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-RecordInventoryValueApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-RecordInventoryValueApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**InventoryValuePoint**](InventoryValuePoint.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

