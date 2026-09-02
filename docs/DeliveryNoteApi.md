# PSOpenAPITools.PSOpenAPITools\Api.DeliveryNoteApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-DeliveryNote**](DeliveryNoteApi.md#New-DeliveryNote) | **POST** /api/v1/delivery-notes | 
[**Invoke-DeleteDeliveryNote**](DeliveryNoteApi.md#Invoke-DeleteDeliveryNote) | **DELETE** /api/v1/delivery-notes/{delivery_note_id} | 
[**Invoke-DeliverynoteRestore**](DeliveryNoteApi.md#Invoke-DeliverynoteRestore) | **POST** /api/v1/delivery-notes/{delivery_note_id}/restore | 
[**Invoke-DownloadDeliveryNotePdf**](DeliveryNoteApi.md#Invoke-DownloadDeliveryNotePdf) | **GET** /api/v1/delivery-notes/{delivery_note_id}/pdf | 
[**Get-DeliveryNote**](DeliveryNoteApi.md#Get-DeliveryNote) | **GET** /api/v1/delivery-notes/{delivery_note_id} | 
[**Invoke-ListDeliveryNotes**](DeliveryNoteApi.md#Invoke-ListDeliveryNotes) | **GET** /api/v1/delivery-notes/ | 
[**Invoke-PursueDeliveryNote**](DeliveryNoteApi.md#Invoke-PursueDeliveryNote) | **POST** /api/v1/delivery-notes/{delivery_note_id}/pursue | 


<a id="New-DeliveryNote"></a>
# **New-DeliveryNote**
> DeliveryNote New-DeliveryNote<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryNoteCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryNoteCreate = Initialize-DeliveryNoteCreate -Address  -ContactId "MyContactId" -ContactName "MyContactName" -Currency "MyCurrency" -DeliveryDate (Get-Date) -DeliveryNoteNumber "MyDeliveryNoteNumber" -Files  -Introduction "MyIntroduction" -LineItems  -PrecedingSalesVoucherId "MyPrecedingSalesVoucherId" -PrecedingSalesVoucherType "order_confirmation" -Remark "MyRemark" -ShippingDate (Get-Date) -ShippingMethod "MyShippingMethod" -Title "MyTitle" -VoucherDate (Get-Date) -VoucherStatus "open" # DeliveryNoteCreate | 

try {
    $Result = New-DeliveryNote -DeliveryNoteCreate $DeliveryNoteCreate
} catch {
    Write-Host ("Exception occurred when calling New-DeliveryNote: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryNoteCreate** | [**DeliveryNoteCreate**](DeliveryNoteCreate.md)|  | 

### Return type

[**DeliveryNote**](DeliveryNote.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteDeliveryNote"></a>
# **Invoke-DeleteDeliveryNote**
> void Invoke-DeleteDeliveryNote<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryNoteId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryNoteId = "MyDeliveryNoteId" # String | 

try {
    $Result = Invoke-DeleteDeliveryNote -DeliveryNoteId $DeliveryNoteId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteDeliveryNote: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryNoteId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeliverynoteRestore"></a>
# **Invoke-DeliverynoteRestore**
> DeliveryNote Invoke-DeliverynoteRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryNoteId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryNoteId = "MyDeliveryNoteId" # String | 

try {
    $Result = Invoke-DeliverynoteRestore -DeliveryNoteId $DeliveryNoteId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeliverynoteRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryNoteId** | **String**|  | 

### Return type

[**DeliveryNote**](DeliveryNote.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DownloadDeliveryNotePdf"></a>
# **Invoke-DownloadDeliveryNotePdf**
> void Invoke-DownloadDeliveryNotePdf<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryNoteId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryNoteId = "MyDeliveryNoteId" # String | 

try {
    $Result = Invoke-DownloadDeliveryNotePdf -DeliveryNoteId $DeliveryNoteId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DownloadDeliveryNotePdf: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryNoteId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-DeliveryNote"></a>
# **Get-DeliveryNote**
> DeliveryNote Get-DeliveryNote<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryNoteId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryNoteId = "MyDeliveryNoteId" # String | 

try {
    $Result = Get-DeliveryNote -DeliveryNoteId $DeliveryNoteId
} catch {
    Write-Host ("Exception occurred when calling Get-DeliveryNote: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryNoteId** | **String**|  | 

### Return type

[**DeliveryNote**](DeliveryNote.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListDeliveryNotes"></a>
# **Invoke-ListDeliveryNotes**
> DeliveryNote[] Invoke-ListDeliveryNotes<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IncludeDeleted] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 1 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)
$IncludeDeleted = $true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

try {
    $Result = Invoke-ListDeliveryNotes -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListDeliveryNotes: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **IncludeDeleted** | **Boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**DeliveryNote[]**](DeliveryNote.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PursueDeliveryNote"></a>
# **Invoke-PursueDeliveryNote**
> Invoice Invoke-PursueDeliveryNote<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryNoteId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryNoteId = "MyDeliveryNoteId" # String | 

try {
    $Result = Invoke-PursueDeliveryNote -DeliveryNoteId $DeliveryNoteId
} catch {
    Write-Host ("Exception occurred when calling Invoke-PursueDeliveryNote: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryNoteId** | **String**|  | 

### Return type

[**Invoice**](Invoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

