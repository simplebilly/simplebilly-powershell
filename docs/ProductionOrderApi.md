# PSOpenAPITools.PSOpenAPITools\Api.ProductionOrderApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ProductionOrder**](ProductionOrderApi.md#New-ProductionOrder) | **POST** /api/v1/production-orders | 
[**Invoke-DeleteProductionOrder**](ProductionOrderApi.md#Invoke-DeleteProductionOrder) | **DELETE** /api/v1/production-orders/{production_order_id} | 
[**Get-ProductionOrder**](ProductionOrderApi.md#Get-ProductionOrder) | **GET** /api/v1/production-orders/{production_order_id} | 
[**Invoke-ListProductionOrders**](ProductionOrderApi.md#Invoke-ListProductionOrders) | **GET** /api/v1/production-orders/ | 
[**Invoke-ProductionOrderCosting**](ProductionOrderApi.md#Invoke-ProductionOrderCosting) | **GET** /api/v1/production-orders/{production_order_id}/costing | Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product&#39;s sale price.
[**Update-ProductionOrder**](ProductionOrderApi.md#Update-ProductionOrder) | **PUT** /api/v1/production-orders/{production_order_id} | 
[**Update-ProductionOrderStatus**](ProductionOrderApi.md#Update-ProductionOrderStatus) | **PUT** /api/v1/production-orders/{production_order_id}/status | 


<a id="New-ProductionOrder"></a>
# **New-ProductionOrder**
> ProductionOrder New-ProductionOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductionOrder] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductionOrder = Initialize-ProductionOrder -BomId "MyBomId" -Components  -EndDate (Get-Date) -Notes "MyNotes" -OrderNumber "MyOrderNumber" -ProductId "MyProductId" -Quantity 0 -SourceWarehouseId "MySourceWarehouseId" -StartDate (Get-Date) -Status "planned" -TargetWarehouseId "MyTargetWarehouseId" # ProductionOrder | 

try {
    $Result = New-ProductionOrder -ProductionOrder $ProductionOrder
} catch {
    Write-Host ("Exception occurred when calling New-ProductionOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductionOrder** | [**ProductionOrder**](ProductionOrder.md)|  | 

### Return type

[**ProductionOrder**](ProductionOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteProductionOrder"></a>
# **Invoke-DeleteProductionOrder**
> void Invoke-DeleteProductionOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductionOrderId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductionOrderId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteProductionOrder -ProductionOrderId $ProductionOrderId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteProductionOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductionOrderId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ProductionOrder"></a>
# **Get-ProductionOrder**
> ProductionOrder Get-ProductionOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductionOrderId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductionOrderId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-ProductionOrder -ProductionOrderId $ProductionOrderId
} catch {
    Write-Host ("Exception occurred when calling Get-ProductionOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductionOrderId** | **String**|  | 

### Return type

[**ProductionOrder**](ProductionOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListProductionOrders"></a>
# **Invoke-ListProductionOrders**
> ProductionOrder[] Invoke-ListProductionOrders<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)
$Status = "MyStatus" # String | Filter by status. (optional)

try {
    $Result = Invoke-ListProductionOrders -Page $Page -PageSize $PageSize -Search $Search -Status $Status
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListProductionOrders: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **Status** | **String**| Filter by status. | [optional] 

### Return type

[**ProductionOrder[]**](ProductionOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ProductionOrderCosting"></a>
# **Invoke-ProductionOrderCosting**
> ProductionOrderCosting Invoke-ProductionOrderCosting<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductionOrderId] <String><br>

Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductionOrderId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

# Actual-costing report (Nachkalkulation) — material costs from BOM components at their purchase price plus the resulting per-unit cost and margin against the finished product's sale price.
try {
    $Result = Invoke-ProductionOrderCosting -ProductionOrderId $ProductionOrderId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ProductionOrderCosting: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductionOrderId** | **String**|  | 

### Return type

[**ProductionOrderCosting**](ProductionOrderCosting.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ProductionOrder"></a>
# **Update-ProductionOrder**
> ProductionOrder Update-ProductionOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductionOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductionOrder] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductionOrderId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$ProductionOrder = Initialize-ProductionOrder -BomId "MyBomId" -Components  -EndDate (Get-Date) -Notes "MyNotes" -OrderNumber "MyOrderNumber" -ProductId "MyProductId" -Quantity 0 -SourceWarehouseId "MySourceWarehouseId" -StartDate (Get-Date) -Status "planned" -TargetWarehouseId "MyTargetWarehouseId" # ProductionOrder | 

try {
    $Result = Update-ProductionOrder -ProductionOrderId $ProductionOrderId -ProductionOrder $ProductionOrder
} catch {
    Write-Host ("Exception occurred when calling Update-ProductionOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductionOrderId** | **String**|  | 
 **ProductionOrder** | [**ProductionOrder**](ProductionOrder.md)|  | 

### Return type

[**ProductionOrder**](ProductionOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ProductionOrderStatus"></a>
# **Update-ProductionOrderStatus**
> ProductionOrder Update-ProductionOrderStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductionOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductionOrderStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductionOrderId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$ProductionOrderStatusUpdate = Initialize-ProductionOrderStatusUpdate -Status "MyStatus" # ProductionOrderStatusUpdate | 

try {
    $Result = Update-ProductionOrderStatus -ProductionOrderId $ProductionOrderId -ProductionOrderStatusUpdate $ProductionOrderStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ProductionOrderStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductionOrderId** | **String**|  | 
 **ProductionOrderStatusUpdate** | [**ProductionOrderStatusUpdate**](ProductionOrderStatusUpdate.md)|  | 

### Return type

[**ProductionOrder**](ProductionOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

