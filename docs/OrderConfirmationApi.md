# PSOpenAPITools.PSOpenAPITools\Api.OrderConfirmationApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Confirmation**](OrderConfirmationApi.md#New-Confirmation) | **POST** /api/v1/order-confirmations | 
[**Invoke-DeleteConfirmation**](OrderConfirmationApi.md#Invoke-DeleteConfirmation) | **DELETE** /api/v1/order-confirmations/{confirmation_id} | 
[**Invoke-DownloadConfirmationPdf**](OrderConfirmationApi.md#Invoke-DownloadConfirmationPdf) | **GET** /api/v1/order-confirmations/{confirmation_id}/pdf | 
[**Get-Confirmation**](OrderConfirmationApi.md#Get-Confirmation) | **GET** /api/v1/order-confirmations/{confirmation_id} | 
[**Invoke-ListConfirmations**](OrderConfirmationApi.md#Invoke-ListConfirmations) | **GET** /api/v1/order-confirmations/ | 
[**Invoke-OrderconfirmationRestore**](OrderConfirmationApi.md#Invoke-OrderconfirmationRestore) | **POST** /api/v1/order-confirmations/{confirmation_id}/restore | 
[**Invoke-PursueConfirmation**](OrderConfirmationApi.md#Invoke-PursueConfirmation) | **POST** /api/v1/order-confirmations/{confirmation_id}/pursue | 


<a id="New-Confirmation"></a>
# **New-Confirmation**
> OrderConfirmation New-Confirmation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderConfirmationCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderConfirmationCreate = Initialize-OrderConfirmationCreate -Address  -ConfirmationNumber "MyConfirmationNumber" -ContactId "MyContactId" -ContactName "MyContactName" -Currency "MyCurrency" -Files  -Introduction "MyIntroduction" -LineItems  -PrecedingSalesVoucherId "MyPrecedingSalesVoucherId" -PrecedingSalesVoucherType "order_confirmation" -Remark "MyRemark" -TaxCondition "MyTaxCondition" -Title "MyTitle" -VoucherDate (Get-Date) -VoucherStatus "open" # OrderConfirmationCreate | 

try {
    $Result = New-Confirmation -OrderConfirmationCreate $OrderConfirmationCreate
} catch {
    Write-Host ("Exception occurred when calling New-Confirmation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderConfirmationCreate** | [**OrderConfirmationCreate**](OrderConfirmationCreate.md)|  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteConfirmation"></a>
# **Invoke-DeleteConfirmation**
> void Invoke-DeleteConfirmation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConfirmationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConfirmationId = "MyConfirmationId" # String | 

try {
    $Result = Invoke-DeleteConfirmation -ConfirmationId $ConfirmationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteConfirmation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConfirmationId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DownloadConfirmationPdf"></a>
# **Invoke-DownloadConfirmationPdf**
> void Invoke-DownloadConfirmationPdf<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConfirmationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConfirmationId = "MyConfirmationId" # String | 

try {
    $Result = Invoke-DownloadConfirmationPdf -ConfirmationId $ConfirmationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DownloadConfirmationPdf: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConfirmationId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Confirmation"></a>
# **Get-Confirmation**
> OrderConfirmation Get-Confirmation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConfirmationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConfirmationId = "MyConfirmationId" # String | 

try {
    $Result = Get-Confirmation -ConfirmationId $ConfirmationId
} catch {
    Write-Host ("Exception occurred when calling Get-Confirmation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConfirmationId** | **String**|  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListConfirmations"></a>
# **Invoke-ListConfirmations**
> OrderConfirmation[] Invoke-ListConfirmations<br>
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
    $Result = Invoke-ListConfirmations -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListConfirmations: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**OrderConfirmation[]**](OrderConfirmation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-OrderconfirmationRestore"></a>
# **Invoke-OrderconfirmationRestore**
> OrderConfirmation Invoke-OrderconfirmationRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConfirmationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConfirmationId = "MyConfirmationId" # String | 

try {
    $Result = Invoke-OrderconfirmationRestore -ConfirmationId $ConfirmationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-OrderconfirmationRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConfirmationId** | **String**|  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PursueConfirmation"></a>
# **Invoke-PursueConfirmation**
> DeliveryNote Invoke-PursueConfirmation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ConfirmationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ConfirmationId = "MyConfirmationId" # String | 

try {
    $Result = Invoke-PursueConfirmation -ConfirmationId $ConfirmationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-PursueConfirmation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ConfirmationId** | **String**|  | 

### Return type

[**DeliveryNote**](DeliveryNote.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

