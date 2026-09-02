# PSOpenAPITools.PSOpenAPITools\Api.CouponApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-CouponRestore**](CouponApi.md#Invoke-CouponRestore) | **POST** /api/v1/coupons/{coupon_id}/restore | 
[**New-Coupon**](CouponApi.md#New-Coupon) | **POST** /api/v1/coupons | 
[**Invoke-DeleteCoupon**](CouponApi.md#Invoke-DeleteCoupon) | **DELETE** /api/v1/coupons/{coupon_id} | 
[**Get-Coupon**](CouponApi.md#Get-Coupon) | **GET** /api/v1/coupons/{coupon_id} | 
[**Invoke-ListCoupons**](CouponApi.md#Invoke-ListCoupons) | **GET** /api/v1/coupons/ | 
[**Update-Coupon**](CouponApi.md#Update-Coupon) | **PUT** /api/v1/coupons/{coupon_id} | 


<a id="Invoke-CouponRestore"></a>
# **Invoke-CouponRestore**
> Coupon Invoke-CouponRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CouponId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CouponId = "MyCouponId" # String | 

try {
    $Result = Invoke-CouponRestore -CouponId $CouponId
} catch {
    Write-Host ("Exception occurred when calling Invoke-CouponRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CouponId** | **String**|  | 

### Return type

[**Coupon**](Coupon.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-Coupon"></a>
# **New-Coupon**
> Coupon New-Coupon<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CouponCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CouponCreate = Initialize-CouponCreate -Code "MyCode" -Description "MyDescription" -DiscountType "percentage" -DiscountValue "MyDiscountValue" -ExpiresAt (Get-Date) -IsActive $false -IsCombineable $false -MaxDiscountAmount "MyMaxDiscountAmount" -MaxUses 0 -MaxUsesPerCustomer 0 -MinOrderAmount "MyMinOrderAmount" -ProductIds  -StartsAt (Get-Date) # CouponCreate | 

try {
    $Result = New-Coupon -CouponCreate $CouponCreate
} catch {
    Write-Host ("Exception occurred when calling New-Coupon: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CouponCreate** | [**CouponCreate**](CouponCreate.md)|  | 

### Return type

[**Coupon**](Coupon.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteCoupon"></a>
# **Invoke-DeleteCoupon**
> void Invoke-DeleteCoupon<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CouponId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CouponId = "MyCouponId" # String | 

try {
    $Result = Invoke-DeleteCoupon -CouponId $CouponId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteCoupon: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CouponId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Coupon"></a>
# **Get-Coupon**
> Coupon Get-Coupon<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CouponId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CouponId = "MyCouponId" # String | 

try {
    $Result = Get-Coupon -CouponId $CouponId
} catch {
    Write-Host ("Exception occurred when calling Get-Coupon: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CouponId** | **String**|  | 

### Return type

[**Coupon**](Coupon.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListCoupons"></a>
# **Invoke-ListCoupons**
> Coupon[] Invoke-ListCoupons<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IsActive] <System.Nullable[Boolean]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Code] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DiscountType] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$IsActive = $true # Boolean |  (optional)
$Code = "MyCode" # String |  (optional)
$DiscountType = "MyDiscountType" # String |  (optional)

try {
    $Result = Invoke-ListCoupons -Page $Page -PageSize $PageSize -IsActive $IsActive -Code $Code -DiscountType $DiscountType
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListCoupons: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **IsActive** | **Boolean**|  | [optional] 
 **Code** | **String**|  | [optional] 
 **DiscountType** | **String**|  | [optional] 

### Return type

[**Coupon[]**](Coupon.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Coupon"></a>
# **Update-Coupon**
> Coupon Update-Coupon<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CouponId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CouponUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CouponId = "MyCouponId" # String | 
$CouponUpdate = Initialize-CouponUpdate -Code "MyCode" -Description "MyDescription" -DiscountType "percentage" -DiscountValue "MyDiscountValue" -ExpiresAt (Get-Date) -IsActive $false -IsCombineable $false -MaxDiscountAmount "MyMaxDiscountAmount" -MaxUses 0 -MaxUsesPerCustomer 0 -MinOrderAmount "MyMinOrderAmount" -ProductIds  -StartsAt (Get-Date) # CouponUpdate | 

try {
    $Result = Update-Coupon -CouponId $CouponId -CouponUpdate $CouponUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-Coupon: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CouponId** | **String**|  | 
 **CouponUpdate** | [**CouponUpdate**](CouponUpdate.md)|  | 

### Return type

[**Coupon**](Coupon.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

