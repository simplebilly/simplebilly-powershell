# PSOpenAPITools.PSOpenAPITools\Api.GoodsReceiptApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-GoodsReceipt**](GoodsReceiptApi.md#New-GoodsReceipt) | **POST** /api/v1/goods-receipts | 
[**Invoke-DeleteGoodsReceipt**](GoodsReceiptApi.md#Invoke-DeleteGoodsReceipt) | **DELETE** /api/v1/goods-receipts/{goods_receipt_id} | 
[**Get-GoodsReceipt**](GoodsReceiptApi.md#Get-GoodsReceipt) | **GET** /api/v1/goods-receipts/{goods_receipt_id} | 
[**Invoke-ListGoodsReceipts**](GoodsReceiptApi.md#Invoke-ListGoodsReceipts) | **GET** /api/v1/goods-receipts/ | 


<a id="New-GoodsReceipt"></a>
# **New-GoodsReceipt**
> GoodsReceipt New-GoodsReceipt<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GoodsReceipt] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GoodsReceipt = Initialize-GoodsReceipt -GrNumber "MyGrNumber" -LineItems  -Notes "MyNotes" -PurchaseOrderId "MyPurchaseOrderId" -ReceiptDate (Get-Date) -SupplierContactId "MySupplierContactId" -SupplierName "MySupplierName" -WarehouseId "MyWarehouseId" # GoodsReceipt | 

try {
    $Result = New-GoodsReceipt -GoodsReceipt $GoodsReceipt
} catch {
    Write-Host ("Exception occurred when calling New-GoodsReceipt: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GoodsReceipt** | [**GoodsReceipt**](GoodsReceipt.md)|  | 

### Return type

[**GoodsReceipt**](GoodsReceipt.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteGoodsReceipt"></a>
# **Invoke-DeleteGoodsReceipt**
> void Invoke-DeleteGoodsReceipt<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GoodsReceiptId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GoodsReceiptId = "MyGoodsReceiptId" # String | 

try {
    $Result = Invoke-DeleteGoodsReceipt -GoodsReceiptId $GoodsReceiptId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteGoodsReceipt: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GoodsReceiptId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-GoodsReceipt"></a>
# **Get-GoodsReceipt**
> GoodsReceipt Get-GoodsReceipt<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GoodsReceiptId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GoodsReceiptId = "MyGoodsReceiptId" # String | 

try {
    $Result = Get-GoodsReceipt -GoodsReceiptId $GoodsReceiptId
} catch {
    Write-Host ("Exception occurred when calling Get-GoodsReceipt: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GoodsReceiptId** | **String**|  | 

### Return type

[**GoodsReceipt**](GoodsReceipt.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListGoodsReceipts"></a>
# **Invoke-ListGoodsReceipts**
> GoodsReceipt[] Invoke-ListGoodsReceipts<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierName] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$PurchaseOrderId = "MyPurchaseOrderId" # String |  (optional)
$SupplierName = "MySupplierName" # String |  (optional)
$WarehouseId = "MyWarehouseId" # String |  (optional)

try {
    $Result = Invoke-ListGoodsReceipts -Page $Page -PageSize $PageSize -PurchaseOrderId $PurchaseOrderId -SupplierName $SupplierName -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListGoodsReceipts: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **PurchaseOrderId** | **String**|  | [optional] 
 **SupplierName** | **String**|  | [optional] 
 **WarehouseId** | **String**|  | [optional] 

### Return type

[**GoodsReceipt[]**](GoodsReceipt.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

