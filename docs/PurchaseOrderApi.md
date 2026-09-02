# PSOpenAPITools.PSOpenAPITools\Api.PurchaseOrderApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-PurchaseOrder**](PurchaseOrderApi.md#New-PurchaseOrder) | **POST** /api/v1/purchase-orders | 
[**Invoke-DeletePurchaseOrder**](PurchaseOrderApi.md#Invoke-DeletePurchaseOrder) | **DELETE** /api/v1/purchase-orders/{purchase_order_id} | 
[**Get-PurchaseOrder**](PurchaseOrderApi.md#Get-PurchaseOrder) | **GET** /api/v1/purchase-orders/{purchase_order_id} | 
[**Invoke-ListPurchaseOrders**](PurchaseOrderApi.md#Invoke-ListPurchaseOrders) | **GET** /api/v1/purchase-orders/ | 
[**Sync-Invoice**](PurchaseOrderApi.md#Sync-Invoice) | **POST** /api/v1/purchase-orders/{purchase_order_id}/match-invoice | 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
[**Update-PurchaseOrder**](PurchaseOrderApi.md#Update-PurchaseOrder) | **PUT** /api/v1/purchase-orders/{purchase_order_id} | 
[**Update-PurchaseOrderStatus**](PurchaseOrderApi.md#Update-PurchaseOrderStatus) | **PUT** /api/v1/purchase-orders/{purchase_order_id}/status | 


<a id="New-PurchaseOrder"></a>
# **New-PurchaseOrder**
> PurchaseOrder New-PurchaseOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrder] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PurchaseOrder = Initialize-PurchaseOrder -Currency "MyCurrency" -DeliveryAddress  -ExpectedDeliveryDate (Get-Date) -LineItems  -Notes "MyNotes" -OrderDate (Get-Date) -PoNumber "MyPoNumber" -Status "draft" -SupplierContactId "MySupplierContactId" -SupplierName "MySupplierName" -TotalGrossAmount "MyTotalGrossAmount" -TotalNetAmount "MyTotalNetAmount" # PurchaseOrder | 

try {
    $Result = New-PurchaseOrder -PurchaseOrder $PurchaseOrder
} catch {
    Write-Host ("Exception occurred when calling New-PurchaseOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PurchaseOrder** | [**PurchaseOrder**](PurchaseOrder.md)|  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeletePurchaseOrder"></a>
# **Invoke-DeletePurchaseOrder**
> void Invoke-DeletePurchaseOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrderId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PurchaseOrderId = "MyPurchaseOrderId" # String | 

try {
    $Result = Invoke-DeletePurchaseOrder -PurchaseOrderId $PurchaseOrderId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeletePurchaseOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PurchaseOrderId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-PurchaseOrder"></a>
# **Get-PurchaseOrder**
> PurchaseOrder Get-PurchaseOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrderId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PurchaseOrderId = "MyPurchaseOrderId" # String | 

try {
    $Result = Get-PurchaseOrder -PurchaseOrderId $PurchaseOrderId
} catch {
    Write-Host ("Exception occurred when calling Get-PurchaseOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PurchaseOrderId** | **String**|  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListPurchaseOrders"></a>
# **Invoke-ListPurchaseOrders**
> PurchaseOrder[] Invoke-ListPurchaseOrders<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierName] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$SupplierName = "MySupplierName" # String |  (optional)
$Search = "MySearch" # String |  (optional)

try {
    $Result = Invoke-ListPurchaseOrders -Page $Page -PageSize $PageSize -Status $Status -SupplierName $SupplierName -Search $Search
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListPurchaseOrders: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **SupplierName** | **String**|  | [optional] 
 **Search** | **String**|  | [optional] 

### Return type

[**PurchaseOrder[]**](PurchaseOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Sync-Invoice"></a>
# **Sync-Invoice**
> AnyType Sync-Invoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InvoiceMatchRequest] <PSCustomObject><br>

3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PurchaseOrderId = "MyPurchaseOrderId" # String | 
$InvoiceMatchRequest = Initialize-InvoiceMatchRequest -SupplierInvoiceId "MySupplierInvoiceId" # InvoiceMatchRequest | 

# 3-way invoice check (Rechnungsprüfung): compares the purchase order line items, the quantities received via goods receipts, and the supplier invoice line items, reporting quantity and price variances per product.
try {
    $Result = Sync-Invoice -PurchaseOrderId $PurchaseOrderId -InvoiceMatchRequest $InvoiceMatchRequest
} catch {
    Write-Host ("Exception occurred when calling Sync-Invoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PurchaseOrderId** | **String**|  | 
 **InvoiceMatchRequest** | [**InvoiceMatchRequest**](InvoiceMatchRequest.md)|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-PurchaseOrder"></a>
# **Update-PurchaseOrder**
> PurchaseOrder Update-PurchaseOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PurchaseOrderId = "MyPurchaseOrderId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-PurchaseOrder -PurchaseOrderId $PurchaseOrderId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-PurchaseOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PurchaseOrderId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-PurchaseOrderStatus"></a>
# **Update-PurchaseOrderStatus**
> PurchaseOrder Update-PurchaseOrderStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrderStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PurchaseOrderId = "MyPurchaseOrderId" # String | 
$PurchaseOrderStatusUpdate = Initialize-PurchaseOrderStatusUpdate -Status "MyStatus" # PurchaseOrderStatusUpdate | 

try {
    $Result = Update-PurchaseOrderStatus -PurchaseOrderId $PurchaseOrderId -PurchaseOrderStatusUpdate $PurchaseOrderStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-PurchaseOrderStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PurchaseOrderId** | **String**|  | 
 **PurchaseOrderStatusUpdate** | [**PurchaseOrderStatusUpdate**](PurchaseOrderStatusUpdate.md)|  | 

### Return type

[**PurchaseOrder**](PurchaseOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

