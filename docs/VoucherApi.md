# PSOpenAPITools.PSOpenAPITools\Api.VoucherApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Voucher**](VoucherApi.md#New-Voucher) | **POST** /api/v1/vouchers | 
[**Invoke-DeleteVoucher**](VoucherApi.md#Invoke-DeleteVoucher) | **DELETE** /api/v1/vouchers/{voucher_id} | 
[**Get-Voucher**](VoucherApi.md#Get-Voucher) | **GET** /api/v1/vouchers/{voucher_id} | 
[**Invoke-ListVouchers**](VoucherApi.md#Invoke-ListVouchers) | **GET** /api/v1/vouchers/ | 
[**Update-Voucher**](VoucherApi.md#Update-Voucher) | **PUT** /api/v1/vouchers/{voucher_id} | 
[**Invoke-VoucherRestore**](VoucherApi.md#Invoke-VoucherRestore) | **POST** /api/v1/vouchers/{voucher_id}/restore | 


<a id="New-Voucher"></a>
# **New-Voucher**
> Voucher New-Voucher<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VoucherCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VoucherCreate = Initialize-VoucherCreate -CategoryId "MyCategoryId" -ContactId "MyContactId" -ContactName "MyContactName" -Currency "MyCurrency" -Description "MyDescription" -FileAttachments  -LineItems  -Metadata  -Notes "MyNotes" -OpenAmount "MyOpenAmount" -PaidDate (Get-Date) -PaymentStatus "unpaid" -TaxAmounts  -TaxCondition "MyTaxCondition" -TotalGrossAmount "MyTotalGrossAmount" -TotalNetAmount "MyTotalNetAmount" -VoucherDate (Get-Date) -VoucherNumber "MyVoucherNumber" -VoucherStatus "open" -VoucherType "invoice" # VoucherCreate | 

try {
    $Result = New-Voucher -VoucherCreate $VoucherCreate
} catch {
    Write-Host ("Exception occurred when calling New-Voucher: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VoucherCreate** | [**VoucherCreate**](VoucherCreate.md)|  | 

### Return type

[**Voucher**](Voucher.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteVoucher"></a>
# **Invoke-DeleteVoucher**
> void Invoke-DeleteVoucher<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VoucherId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VoucherId = "MyVoucherId" # String | 

try {
    $Result = Invoke-DeleteVoucher -VoucherId $VoucherId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteVoucher: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VoucherId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Voucher"></a>
# **Get-Voucher**
> Voucher Get-Voucher<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VoucherId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VoucherId = "MyVoucherId" # String | 

try {
    $Result = Get-Voucher -VoucherId $VoucherId
} catch {
    Write-Host ("Exception occurred when calling Get-Voucher: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VoucherId** | **String**|  | 

### Return type

[**Voucher**](Voucher.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListVouchers"></a>
# **Invoke-ListVouchers**
> Voucher[] Invoke-ListVouchers<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VoucherType] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VoucherStatus] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ContactName] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateFrom] <System.Nullable[System.DateTime]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DateTo] <System.Nullable[System.DateTime]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$VoucherType = "MyVoucherType" # String |  (optional)
$VoucherStatus = "MyVoucherStatus" # String |  (optional)
$ContactName = "MyContactName" # String |  (optional)
$DateFrom = (Get-Date) # System.DateTime |  (optional)
$DateTo = (Get-Date) # System.DateTime |  (optional)

try {
    $Result = Invoke-ListVouchers -Page $Page -PageSize $PageSize -VoucherType $VoucherType -VoucherStatus $VoucherStatus -ContactName $ContactName -DateFrom $DateFrom -DateTo $DateTo
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListVouchers: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **VoucherType** | **String**|  | [optional] 
 **VoucherStatus** | **String**|  | [optional] 
 **ContactName** | **String**|  | [optional] 
 **DateFrom** | **System.DateTime**|  | [optional] 
 **DateTo** | **System.DateTime**|  | [optional] 

### Return type

[**Voucher[]**](Voucher.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Voucher"></a>
# **Update-Voucher**
> Voucher Update-Voucher<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VoucherId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VoucherId = "MyVoucherId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-Voucher -VoucherId $VoucherId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-Voucher: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VoucherId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**Voucher**](Voucher.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-VoucherRestore"></a>
# **Invoke-VoucherRestore**
> Voucher Invoke-VoucherRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VoucherId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VoucherId = "MyVoucherId" # String | 

try {
    $Result = Invoke-VoucherRestore -VoucherId $VoucherId
} catch {
    Write-Host ("Exception occurred when calling Invoke-VoucherRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VoucherId** | **String**|  | 

### Return type

[**Voucher**](Voucher.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

