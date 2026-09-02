# PSOpenAPITools.PSOpenAPITools\Api.SupplierInvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-SupplierInvoice**](SupplierInvoiceApi.md#New-SupplierInvoice) | **POST** /api/v1/supplier-invoices | 
[**Invoke-DeleteSupplierInvoice**](SupplierInvoiceApi.md#Invoke-DeleteSupplierInvoice) | **DELETE** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**Get-SupplierInvoice**](SupplierInvoiceApi.md#Get-SupplierInvoice) | **GET** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**Invoke-ListSupplierInvoices**](SupplierInvoiceApi.md#Invoke-ListSupplierInvoices) | **GET** /api/v1/supplier-invoices/ | 
[**Update-SupplierInvoice**](SupplierInvoiceApi.md#Update-SupplierInvoice) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id} | 
[**Update-SupplierInvoiceStatus**](SupplierInvoiceApi.md#Update-SupplierInvoiceStatus) | **PUT** /api/v1/supplier-invoices/{supplier_invoice_id}/status | 


<a id="New-SupplierInvoice"></a>
# **New-SupplierInvoice**
> SupplierInvoice New-SupplierInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierInvoice] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierInvoice = Initialize-SupplierInvoice -Currency "MyCurrency" -GoodsReceiptId "MyGoodsReceiptId" -InvoiceDate (Get-Date) -InvoiceNumber "MyInvoiceNumber" -LineItems  -Notes "MyNotes" -PurchaseOrderId "MyPurchaseOrderId" -Status "draft" -SupplierContactId "MySupplierContactId" -SupplierName "MySupplierName" -TotalGrossAmount "MyTotalGrossAmount" -TotalNetAmount "MyTotalNetAmount" # SupplierInvoice | 

try {
    $Result = New-SupplierInvoice -SupplierInvoice $SupplierInvoice
} catch {
    Write-Host ("Exception occurred when calling New-SupplierInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierInvoice** | [**SupplierInvoice**](SupplierInvoice.md)|  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteSupplierInvoice"></a>
# **Invoke-DeleteSupplierInvoice**
> void Invoke-DeleteSupplierInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierInvoiceId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierInvoiceId = "MySupplierInvoiceId" # String | 

try {
    $Result = Invoke-DeleteSupplierInvoice -SupplierInvoiceId $SupplierInvoiceId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteSupplierInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierInvoiceId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-SupplierInvoice"></a>
# **Get-SupplierInvoice**
> SupplierInvoice Get-SupplierInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierInvoiceId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierInvoiceId = "MySupplierInvoiceId" # String | 

try {
    $Result = Get-SupplierInvoice -SupplierInvoiceId $SupplierInvoiceId
} catch {
    Write-Host ("Exception occurred when calling Get-SupplierInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierInvoiceId** | **String**|  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListSupplierInvoices"></a>
# **Invoke-ListSupplierInvoices**
> SupplierInvoice[] Invoke-ListSupplierInvoices<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PurchaseOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierName] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$PurchaseOrderId = "MyPurchaseOrderId" # String |  (optional)
$SupplierName = "MySupplierName" # String |  (optional)

try {
    $Result = Invoke-ListSupplierInvoices -Page $Page -PageSize $PageSize -Status $Status -PurchaseOrderId $PurchaseOrderId -SupplierName $SupplierName
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListSupplierInvoices: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **PurchaseOrderId** | **String**|  | [optional] 
 **SupplierName** | **String**|  | [optional] 

### Return type

[**SupplierInvoice[]**](SupplierInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-SupplierInvoice"></a>
# **Update-SupplierInvoice**
> SupplierInvoice Update-SupplierInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierInvoiceId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierInvoiceId = "MySupplierInvoiceId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-SupplierInvoice -SupplierInvoiceId $SupplierInvoiceId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-SupplierInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierInvoiceId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-SupplierInvoiceStatus"></a>
# **Update-SupplierInvoiceStatus**
> SupplierInvoice Update-SupplierInvoiceStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierInvoiceId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierInvoiceStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SupplierInvoiceId = "MySupplierInvoiceId" # String | 
$SupplierInvoiceStatusUpdate = Initialize-SupplierInvoiceStatusUpdate -Status "MyStatus" # SupplierInvoiceStatusUpdate | 

try {
    $Result = Update-SupplierInvoiceStatus -SupplierInvoiceId $SupplierInvoiceId -SupplierInvoiceStatusUpdate $SupplierInvoiceStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-SupplierInvoiceStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SupplierInvoiceId** | **String**|  | 
 **SupplierInvoiceStatusUpdate** | [**SupplierInvoiceStatusUpdate**](SupplierInvoiceStatusUpdate.md)|  | 

### Return type

[**SupplierInvoice**](SupplierInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

