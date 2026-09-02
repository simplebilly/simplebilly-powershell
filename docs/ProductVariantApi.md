# PSOpenAPITools.PSOpenAPITools\Api.ProductVariantApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ProductVariant**](ProductVariantApi.md#New-ProductVariant) | **POST** /api/v1/product-variants | 
[**Invoke-DeleteProductVariant**](ProductVariantApi.md#Invoke-DeleteProductVariant) | **DELETE** /api/v1/product-variants/{variant_id} | 
[**New-ProductVariants**](ProductVariantApi.md#New-ProductVariants) | **POST** /api/v1/product-variants/generate | 
[**Get-ProductVariant**](ProductVariantApi.md#Get-ProductVariant) | **GET** /api/v1/product-variants/{variant_id} | 
[**Invoke-ListProductVariants**](ProductVariantApi.md#Invoke-ListProductVariants) | **GET** /api/v1/product-variants/ | 
[**Update-ProductVariant**](ProductVariantApi.md#Update-ProductVariant) | **PUT** /api/v1/product-variants/{variant_id} | 


<a id="New-ProductVariant"></a>
# **New-ProductVariant**
> ProductVariant New-ProductVariant<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductVariant] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductVariant = Initialize-ProductVariant -Barcode "MyBarcode" -ImageLink "MyImageLink" -IsActive $false -Name "MyName" -OptionValues  -Price "MyPrice" -PriceDelta "MyPriceDelta" -ProductId "MyProductId" -Sku "MySku" -StockQuantity 0 # ProductVariant | 

try {
    $Result = New-ProductVariant -ProductVariant $ProductVariant
} catch {
    Write-Host ("Exception occurred when calling New-ProductVariant: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductVariant** | [**ProductVariant**](ProductVariant.md)|  | 

### Return type

[**ProductVariant**](ProductVariant.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteProductVariant"></a>
# **Invoke-DeleteProductVariant**
> void Invoke-DeleteProductVariant<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VariantId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VariantId = "MyVariantId" # String | 

try {
    $Result = Invoke-DeleteProductVariant -VariantId $VariantId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteProductVariant: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VariantId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-ProductVariants"></a>
# **New-ProductVariants**
> ProductVariant[] New-ProductVariants<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GenerateVariantsRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GenerateVariantsRequest = Initialize-GenerateVariantsRequest -Options @{ key_example = "MyInner" } -PriceDelta "MyPriceDelta" -ProductId "MyProductId" -SkuPrefix "MySkuPrefix" # GenerateVariantsRequest | 

try {
    $Result = New-ProductVariants -GenerateVariantsRequest $GenerateVariantsRequest
} catch {
    Write-Host ("Exception occurred when calling New-ProductVariants: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GenerateVariantsRequest** | [**GenerateVariantsRequest**](GenerateVariantsRequest.md)|  | 

### Return type

[**ProductVariant[]**](ProductVariant.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ProductVariant"></a>
# **Get-ProductVariant**
> ProductVariant Get-ProductVariant<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VariantId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VariantId = "MyVariantId" # String | 

try {
    $Result = Get-ProductVariant -VariantId $VariantId
} catch {
    Write-Host ("Exception occurred when calling Get-ProductVariant: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VariantId** | **String**|  | 

### Return type

[**ProductVariant**](ProductVariant.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListProductVariants"></a>
# **Invoke-ListProductVariants**
> ProductVariant[] Invoke-ListProductVariants<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IsActive] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String |  (optional)
$IsActive = $true # Boolean |  (optional)

try {
    $Result = Invoke-ListProductVariants -Page $Page -PageSize $PageSize -ProductId $ProductId -IsActive $IsActive
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListProductVariants: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **ProductId** | **String**|  | [optional] 
 **IsActive** | **Boolean**|  | [optional] 

### Return type

[**ProductVariant[]**](ProductVariant.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ProductVariant"></a>
# **Update-ProductVariant**
> ProductVariant Update-ProductVariant<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-VariantId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$VariantId = "MyVariantId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-ProductVariant -VariantId $VariantId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-ProductVariant: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **VariantId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**ProductVariant**](ProductVariant.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

