# PSOpenAPITools.PSOpenAPITools\Api.ProductCategoryApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ProductCategory**](ProductCategoryApi.md#New-ProductCategory) | **POST** /api/v1/product-categories | 
[**Invoke-DeleteProductCategory**](ProductCategoryApi.md#Invoke-DeleteProductCategory) | **DELETE** /api/v1/product-categories/{category_id} | 
[**Get-ProductCategory**](ProductCategoryApi.md#Get-ProductCategory) | **GET** /api/v1/product-categories/{category_id} | 
[**Invoke-ListProductCategories**](ProductCategoryApi.md#Invoke-ListProductCategories) | **GET** /api/v1/product-categories | 
[**Update-ProductCategory**](ProductCategoryApi.md#Update-ProductCategory) | **PUT** /api/v1/product-categories/{category_id} | 


<a id="New-ProductCategory"></a>
# **New-ProductCategory**
> ProductCategory New-ProductCategory<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductCategory] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductCategory = Initialize-ProductCategory -Description "MyDescription" -Name "MyName" -ParentCategoryId "MyParentCategoryId" -SortOrder 0 # ProductCategory | 

try {
    $Result = New-ProductCategory -ProductCategory $ProductCategory
} catch {
    Write-Host ("Exception occurred when calling New-ProductCategory: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductCategory** | [**ProductCategory**](ProductCategory.md)|  | 

### Return type

[**ProductCategory**](ProductCategory.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteProductCategory"></a>
# **Invoke-DeleteProductCategory**
> void Invoke-DeleteProductCategory<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CategoryId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CategoryId = "MyCategoryId" # String | 

try {
    $Result = Invoke-DeleteProductCategory -CategoryId $CategoryId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteProductCategory: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CategoryId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ProductCategory"></a>
# **Get-ProductCategory**
> ProductCategory Get-ProductCategory<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CategoryId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CategoryId = "MyCategoryId" # String | 

try {
    $Result = Get-ProductCategory -CategoryId $CategoryId
} catch {
    Write-Host ("Exception occurred when calling Get-ProductCategory: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CategoryId** | **String**|  | 

### Return type

[**ProductCategory**](ProductCategory.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListProductCategories"></a>
# **Invoke-ListProductCategories**
> ProductCategory[] Invoke-ListProductCategories<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListProductCategories
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListProductCategories: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ProductCategory[]**](ProductCategory.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ProductCategory"></a>
# **Update-ProductCategory**
> ProductCategory Update-ProductCategory<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CategoryId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CategoryId = "MyCategoryId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-ProductCategory -CategoryId $CategoryId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-ProductCategory: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CategoryId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**ProductCategory**](ProductCategory.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

