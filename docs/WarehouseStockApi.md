# PSOpenAPITools.PSOpenAPITools\Api.WarehouseStockApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-WarehouseStock**](WarehouseStockApi.md#New-WarehouseStock) | **POST** /api/v1/warehouses/{warehouse_id}/stock | 
[**Invoke-DeleteWarehouseStock**](WarehouseStockApi.md#Invoke-DeleteWarehouseStock) | **DELETE** /api/v1/warehouses/{warehouse_id}/stock/{product_id} | 
[**Invoke-ListWarehouseStock**](WarehouseStockApi.md#Invoke-ListWarehouseStock) | **GET** /api/v1/warehouses/{warehouse_id}/stock | 
[**Update-WarehouseStock**](WarehouseStockApi.md#Update-WarehouseStock) | **PUT** /api/v1/warehouses/{warehouse_id}/stock/{product_id} | 


<a id="New-WarehouseStock"></a>
# **New-WarehouseStock**
> WarehouseStock New-WarehouseStock<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-StockAdjustment] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WarehouseId = "MyWarehouseId" # String | 
$StockAdjustment = Initialize-StockAdjustment -BatchNumber "MyBatchNumber" -BinLocation "MyBinLocation" -ExpiryDate (Get-Date) -ProductId "MyProductId" -Quantity 0 -SerialNumbers "MySerialNumbers" # StockAdjustment | 

try {
    $Result = New-WarehouseStock -WarehouseId $WarehouseId -StockAdjustment $StockAdjustment
} catch {
    Write-Host ("Exception occurred when calling New-WarehouseStock: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WarehouseId** | **String**|  | 
 **StockAdjustment** | [**StockAdjustment**](StockAdjustment.md)|  | 

### Return type

[**WarehouseStock**](WarehouseStock.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteWarehouseStock"></a>
# **Invoke-DeleteWarehouseStock**
> void Invoke-DeleteWarehouseStock<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WarehouseId = "MyWarehouseId" # String | 
$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteWarehouseStock -WarehouseId $WarehouseId -ProductId $ProductId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteWarehouseStock: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WarehouseId** | **String**|  | 
 **ProductId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListWarehouseStock"></a>
# **Invoke-ListWarehouseStock**
> WarehouseStock[] Invoke-ListWarehouseStock<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WarehouseId = "MyWarehouseId" # String | 

try {
    $Result = Invoke-ListWarehouseStock -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListWarehouseStock: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WarehouseId** | **String**|  | 

### Return type

[**WarehouseStock[]**](WarehouseStock.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-WarehouseStock"></a>
# **Update-WarehouseStock**
> WarehouseStock Update-WarehouseStock<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-StockAdjustment] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WarehouseId = "MyWarehouseId" # String | 
$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$StockAdjustment = Initialize-StockAdjustment -BatchNumber "MyBatchNumber" -BinLocation "MyBinLocation" -ExpiryDate (Get-Date) -ProductId "MyProductId" -Quantity 0 -SerialNumbers "MySerialNumbers" # StockAdjustment | 

try {
    $Result = Update-WarehouseStock -WarehouseId $WarehouseId -ProductId $ProductId -StockAdjustment $StockAdjustment
} catch {
    Write-Host ("Exception occurred when calling Update-WarehouseStock: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WarehouseId** | **String**|  | 
 **ProductId** | **String**|  | 
 **StockAdjustment** | [**StockAdjustment**](StockAdjustment.md)|  | 

### Return type

[**WarehouseStock**](WarehouseStock.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

