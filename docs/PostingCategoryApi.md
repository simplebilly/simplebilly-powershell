# PSOpenAPITools.PSOpenAPITools\Api.PostingCategoryApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-PostingCategory**](PostingCategoryApi.md#New-PostingCategory) | **POST** /api/v1/posting-categories | 
[**Invoke-DeletePostingCategory**](PostingCategoryApi.md#Invoke-DeletePostingCategory) | **DELETE** /api/v1/posting-categories/{category_id} | 
[**Invoke-ListPostingCategories**](PostingCategoryApi.md#Invoke-ListPostingCategories) | **GET** /api/v1/posting-categories | 
[**Invoke-SeedPostingCategories**](PostingCategoryApi.md#Invoke-SeedPostingCategories) | **POST** /api/v1/posting-categories/seed/{skr_version} | 
[**Update-PostingCategory**](PostingCategoryApi.md#Update-PostingCategory) | **PUT** /api/v1/posting-categories/{category_id} | 


<a id="New-PostingCategory"></a>
# **New-PostingCategory**
> PostingCategory New-PostingCategory<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Body =  # AnyType | 

try {
    $Result = New-PostingCategory -Body $Body
} catch {
    Write-Host ("Exception occurred when calling New-PostingCategory: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Body** | **AnyType**|  | 

### Return type

[**PostingCategory**](PostingCategory.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeletePostingCategory"></a>
# **Invoke-DeletePostingCategory**
> void Invoke-DeletePostingCategory<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CategoryId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CategoryId = "MyCategoryId" # String | 

try {
    $Result = Invoke-DeletePostingCategory -CategoryId $CategoryId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeletePostingCategory: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

<a id="Invoke-ListPostingCategories"></a>
# **Invoke-ListPostingCategories**
> PostingCategory[] Invoke-ListPostingCategories<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ListPostingCategories
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListPostingCategories: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**PostingCategory[]**](PostingCategory.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-SeedPostingCategories"></a>
# **Invoke-SeedPostingCategories**
> void Invoke-SeedPostingCategories<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SkrVersion] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$SkrVersion = "MySkrVersion" # String | 

try {
    $Result = Invoke-SeedPostingCategories -SkrVersion $SkrVersion
} catch {
    Write-Host ("Exception occurred when calling Invoke-SeedPostingCategories: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **SkrVersion** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-PostingCategory"></a>
# **Update-PostingCategory**
> PostingCategory Update-PostingCategory<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CategoryId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CategoryId = "MyCategoryId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-PostingCategory -CategoryId $CategoryId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-PostingCategory: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CategoryId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**PostingCategory**](PostingCategory.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

