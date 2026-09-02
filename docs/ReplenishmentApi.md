# PSOpenAPITools.PSOpenAPITools\Api.ReplenishmentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-ApplyReplenishments**](ReplenishmentApi.md#Invoke-ApplyReplenishments) | **POST** /api/v1/replenishments/apply | Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
[**Get-Replenishments**](ReplenishmentApi.md#Get-Replenishments) | **GET** /api/v1/replenishments | 


<a id="Invoke-ApplyReplenishments"></a>
# **Invoke-ApplyReplenishments**
> AnyType Invoke-ApplyReplenishments<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TargetWarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SourceWarehouseId] <String><br>

Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TargetWarehouseId = "MyTargetWarehouseId" # String | Warehouse to be replenished. Defaults to the tenant's default warehouse. (optional)
$SourceWarehouseId = "MySourceWarehouseId" # String | Restrict source warehouses to this id. (optional)

# Create one draft stock transfer per (source → target) pair carrying all suggested product lines for that pair.
try {
    $Result = Invoke-ApplyReplenishments -TargetWarehouseId $TargetWarehouseId -SourceWarehouseId $SourceWarehouseId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ApplyReplenishments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TargetWarehouseId** | **String**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] 
 **SourceWarehouseId** | **String**| Restrict source warehouses to this id. | [optional] 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Replenishments"></a>
# **Get-Replenishments**
> ReplenishmentResponse Get-Replenishments<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TargetWarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SourceWarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TargetWarehouseId = "MyTargetWarehouseId" # String | Warehouse to be replenished. Defaults to the tenant's default warehouse. (optional)
$SourceWarehouseId = "MySourceWarehouseId" # String | Restrict source warehouses to this id. (optional)

try {
    $Result = Get-Replenishments -TargetWarehouseId $TargetWarehouseId -SourceWarehouseId $SourceWarehouseId
} catch {
    Write-Host ("Exception occurred when calling Get-Replenishments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TargetWarehouseId** | **String**| Warehouse to be replenished. Defaults to the tenant&#39;s default warehouse. | [optional] 
 **SourceWarehouseId** | **String**| Restrict source warehouses to this id. | [optional] 

### Return type

[**ReplenishmentResponse**](ReplenishmentResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

