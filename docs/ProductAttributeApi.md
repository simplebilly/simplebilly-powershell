# PSOpenAPITools.PSOpenAPITools\Api.ProductAttributeApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ProductAttribute**](ProductAttributeApi.md#New-ProductAttribute) | **POST** /api/v1/product-attributes | 
[**Invoke-DeleteProductAttribute**](ProductAttributeApi.md#Invoke-DeleteProductAttribute) | **DELETE** /api/v1/product-attributes/{attribute_id} | 
[**Get-ProductAttribute**](ProductAttributeApi.md#Get-ProductAttribute) | **GET** /api/v1/product-attributes/{attribute_id} | 
[**Invoke-ListProductAttributes**](ProductAttributeApi.md#Invoke-ListProductAttributes) | **GET** /api/v1/product-attributes/ | 
[**Update-ProductAttribute**](ProductAttributeApi.md#Update-ProductAttribute) | **PUT** /api/v1/product-attributes/{attribute_id} | 


<a id="New-ProductAttribute"></a>
# **New-ProductAttribute**
> ProductAttribute New-ProductAttribute<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductAttributeCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductAttributeCreate = Initialize-ProductAttributeCreate -IsFilterable $false -Name "MyName" -Position 0 -ProductId "MyProductId" -Unit "MyUnit" -Value "MyValue" # ProductAttributeCreate | 

try {
    $Result = New-ProductAttribute -ProductAttributeCreate $ProductAttributeCreate
} catch {
    Write-Host ("Exception occurred when calling New-ProductAttribute: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductAttributeCreate** | [**ProductAttributeCreate**](ProductAttributeCreate.md)|  | 

### Return type

[**ProductAttribute**](ProductAttribute.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteProductAttribute"></a>
# **Invoke-DeleteProductAttribute**
> void Invoke-DeleteProductAttribute<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AttributeId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AttributeId = "MyAttributeId" # String | 

try {
    $Result = Invoke-DeleteProductAttribute -AttributeId $AttributeId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteProductAttribute: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AttributeId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ProductAttribute"></a>
# **Get-ProductAttribute**
> ProductAttribute Get-ProductAttribute<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AttributeId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AttributeId = "MyAttributeId" # String | 

try {
    $Result = Get-ProductAttribute -AttributeId $AttributeId
} catch {
    Write-Host ("Exception occurred when calling Get-ProductAttribute: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AttributeId** | **String**|  | 

### Return type

[**ProductAttribute**](ProductAttribute.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListProductAttributes"></a>
# **Invoke-ListProductAttributes**
> ProductAttribute[] Invoke-ListProductAttributes<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IsFilterable] <System.Nullable[Boolean]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String |  (optional)
$IsFilterable = $true # Boolean |  (optional)
$Search = "MySearch" # String |  (optional)

try {
    $Result = Invoke-ListProductAttributes -Page $Page -PageSize $PageSize -ProductId $ProductId -IsFilterable $IsFilterable -Search $Search
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListProductAttributes: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **ProductId** | **String**|  | [optional] 
 **IsFilterable** | **Boolean**|  | [optional] 
 **Search** | **String**|  | [optional] 

### Return type

[**ProductAttribute[]**](ProductAttribute.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ProductAttribute"></a>
# **Update-ProductAttribute**
> ProductAttribute Update-ProductAttribute<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AttributeId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductAttributeUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AttributeId = "MyAttributeId" # String | 
$ProductAttributeUpdate = Initialize-ProductAttributeUpdate -IsFilterable $false -Name "MyName" -Position 0 -ProductId "MyProductId" -Unit "MyUnit" -Value "MyValue" # ProductAttributeUpdate | 

try {
    $Result = Update-ProductAttribute -AttributeId $AttributeId -ProductAttributeUpdate $ProductAttributeUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ProductAttribute: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AttributeId** | **String**|  | 
 **ProductAttributeUpdate** | [**ProductAttributeUpdate**](ProductAttributeUpdate.md)|  | 

### Return type

[**ProductAttribute**](ProductAttribute.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

