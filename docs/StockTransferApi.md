# PSOpenAPITools.PSOpenAPITools\Api.StockTransferApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-StockTransfer**](StockTransferApi.md#New-StockTransfer) | **POST** /api/v1/stock-transfers | 
[**Invoke-DeleteStockTransfer**](StockTransferApi.md#Invoke-DeleteStockTransfer) | **DELETE** /api/v1/stock-transfers/{stock_transfer_id} | 
[**Get-StockTransfer**](StockTransferApi.md#Get-StockTransfer) | **GET** /api/v1/stock-transfers/{stock_transfer_id} | 
[**Invoke-ListStockTransfers**](StockTransferApi.md#Invoke-ListStockTransfers) | **GET** /api/v1/stock-transfers/ | 
[**Update-StockTransferStatus**](StockTransferApi.md#Update-StockTransferStatus) | **PUT** /api/v1/stock-transfers/{stock_transfer_id}/status | 


<a id="New-StockTransfer"></a>
# **New-StockTransfer**
> StockTransfer New-StockTransfer<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-StockTransfer] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$StockTransfer = Initialize-StockTransfer -LineItems  -Notes "MyNotes" -SourceWarehouseId "MySourceWarehouseId" -Status "draft" -TargetWarehouseId "MyTargetWarehouseId" -TransferDate (Get-Date) -TransferNumber "MyTransferNumber" # StockTransfer | 

try {
    $Result = New-StockTransfer -StockTransfer $StockTransfer
} catch {
    Write-Host ("Exception occurred when calling New-StockTransfer: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **StockTransfer** | [**StockTransfer**](StockTransfer.md)|  | 

### Return type

[**StockTransfer**](StockTransfer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteStockTransfer"></a>
# **Invoke-DeleteStockTransfer**
> void Invoke-DeleteStockTransfer<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-StockTransferId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$StockTransferId = "MyStockTransferId" # String | 

try {
    $Result = Invoke-DeleteStockTransfer -StockTransferId $StockTransferId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteStockTransfer: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **StockTransferId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-StockTransfer"></a>
# **Get-StockTransfer**
> StockTransfer Get-StockTransfer<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-StockTransferId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$StockTransferId = "MyStockTransferId" # String | 

try {
    $Result = Get-StockTransfer -StockTransferId $StockTransferId
} catch {
    Write-Host ("Exception occurred when calling Get-StockTransfer: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **StockTransferId** | **String**|  | 

### Return type

[**StockTransfer**](StockTransfer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListStockTransfers"></a>
# **Invoke-ListStockTransfers**
> StockTransfer[] Invoke-ListStockTransfers<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$WarehouseId = "MyWarehouseId" # String |  (optional)

try {
    $Result = Invoke-ListStockTransfers -Page $Page -PageSize $PageSize -Status $Status -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListStockTransfers: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **WarehouseId** | **String**|  | [optional] 

### Return type

[**StockTransfer[]**](StockTransfer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-StockTransferStatus"></a>
# **Update-StockTransferStatus**
> StockTransfer Update-StockTransferStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-StockTransferId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-StockTransferStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$StockTransferId = "MyStockTransferId" # String | 
$StockTransferStatusUpdate = Initialize-StockTransferStatusUpdate -Status "MyStatus" # StockTransferStatusUpdate | 

try {
    $Result = Update-StockTransferStatus -StockTransferId $StockTransferId -StockTransferStatusUpdate $StockTransferStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-StockTransferStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **StockTransferId** | **String**|  | 
 **StockTransferStatusUpdate** | [**StockTransferStatusUpdate**](StockTransferStatusUpdate.md)|  | 

### Return type

[**StockTransfer**](StockTransfer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

