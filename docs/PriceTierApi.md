# PSOpenAPITools.PSOpenAPITools\Api.PriceTierApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-PriceTier**](PriceTierApi.md#New-PriceTier) | **POST** /api/v1/price-tiers | 
[**Invoke-DeletePriceTier**](PriceTierApi.md#Invoke-DeletePriceTier) | **DELETE** /api/v1/price-tiers/{price_tier_id} | 
[**Get-PriceTier**](PriceTierApi.md#Get-PriceTier) | **GET** /api/v1/price-tiers/{price_tier_id} | 
[**Get-ResolvedPrice**](PriceTierApi.md#Get-ResolvedPrice) | **GET** /api/v1/price-tiers/resolved | 
[**Invoke-ListPriceTiers**](PriceTierApi.md#Invoke-ListPriceTiers) | **GET** /api/v1/price-tiers/ | 
[**Update-PriceTier**](PriceTierApi.md#Update-PriceTier) | **PUT** /api/v1/price-tiers/{price_tier_id} | 


<a id="New-PriceTier"></a>
# **New-PriceTier**
> PriceTier New-PriceTier<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PriceTierCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PriceTierCreate = Initialize-PriceTierCreate -CustomerGroupId "MyCustomerGroupId" -MinQuantity 0 -ProductId "MyProductId" -UnitPrice "MyUnitPrice" # PriceTierCreate | 

try {
    $Result = New-PriceTier -PriceTierCreate $PriceTierCreate
} catch {
    Write-Host ("Exception occurred when calling New-PriceTier: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PriceTierCreate** | [**PriceTierCreate**](PriceTierCreate.md)|  | 

### Return type

[**PriceTier**](PriceTier.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeletePriceTier"></a>
# **Invoke-DeletePriceTier**
> void Invoke-DeletePriceTier<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PriceTierId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PriceTierId = "MyPriceTierId" # String | 

try {
    $Result = Invoke-DeletePriceTier -PriceTierId $PriceTierId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeletePriceTier: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PriceTierId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-PriceTier"></a>
# **Get-PriceTier**
> PriceTier Get-PriceTier<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PriceTierId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PriceTierId = "MyPriceTierId" # String | 

try {
    $Result = Get-PriceTier -PriceTierId $PriceTierId
} catch {
    Write-Host ("Exception occurred when calling Get-PriceTier: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PriceTierId** | **String**|  | 

### Return type

[**PriceTier**](PriceTier.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ResolvedPrice"></a>
# **Get-ResolvedPrice**
> ResolvedPriceResponse Get-ResolvedPrice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Quantity] <System.Nullable[Int64]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ContactId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$Quantity = 789 # Int64 |  (optional)
$ContactId = "MyContactId" # String | Contact used to match customer-group-scoped tiers. (optional)

try {
    $Result = Get-ResolvedPrice -ProductId $ProductId -Quantity $Quantity -ContactId $ContactId
} catch {
    Write-Host ("Exception occurred when calling Get-ResolvedPrice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductId** | **String**|  | 
 **Quantity** | **Int64**|  | [optional] 
 **ContactId** | **String**| Contact used to match customer-group-scoped tiers. | [optional] 

### Return type

[**ResolvedPriceResponse**](ResolvedPriceResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListPriceTiers"></a>
# **Invoke-ListPriceTiers**
> PriceTier[] Invoke-ListPriceTiers<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerGroupId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String |  (optional)
$CustomerGroupId = "MyCustomerGroupId" # String |  (optional)

try {
    $Result = Invoke-ListPriceTiers -Page $Page -PageSize $PageSize -ProductId $ProductId -CustomerGroupId $CustomerGroupId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListPriceTiers: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **ProductId** | **String**|  | [optional] 
 **CustomerGroupId** | **String**|  | [optional] 

### Return type

[**PriceTier[]**](PriceTier.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-PriceTier"></a>
# **Update-PriceTier**
> PriceTier Update-PriceTier<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PriceTierId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PriceTierUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PriceTierId = "MyPriceTierId" # String | 
$PriceTierUpdate = Initialize-PriceTierUpdate -CustomerGroupId "MyCustomerGroupId" -MinQuantity 0 -ProductId "MyProductId" -UnitPrice "MyUnitPrice" # PriceTierUpdate | 

try {
    $Result = Update-PriceTier -PriceTierId $PriceTierId -PriceTierUpdate $PriceTierUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-PriceTier: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PriceTierId** | **String**|  | 
 **PriceTierUpdate** | [**PriceTierUpdate**](PriceTierUpdate.md)|  | 

### Return type

[**PriceTier**](PriceTier.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

