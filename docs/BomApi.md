# PSOpenAPITools.PSOpenAPITools\Api.BomApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Bom**](BomApi.md#New-Bom) | **POST** /api/v1/boms | 
[**Invoke-DeleteBom**](BomApi.md#Invoke-DeleteBom) | **DELETE** /api/v1/boms/{bom_id} | 
[**Get-Bom**](BomApi.md#Get-Bom) | **GET** /api/v1/boms/{bom_id} | 
[**Invoke-ListBoms**](BomApi.md#Invoke-ListBoms) | **GET** /api/v1/boms/ | 
[**Update-Bom**](BomApi.md#Update-Bom) | **PUT** /api/v1/boms/{bom_id} | 


<a id="New-Bom"></a>
# **New-Bom**
> Bom New-Bom<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-BomCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$BomCreate = Initialize-BomCreate -Components  -Description "MyDescription" -Name "MyName" -OutputQuantity 0 -ProductId "MyProductId" -Status "draft" # BomCreate | 

try {
    $Result = New-Bom -BomCreate $BomCreate
} catch {
    Write-Host ("Exception occurred when calling New-Bom: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **BomCreate** | [**BomCreate**](BomCreate.md)|  | 

### Return type

[**Bom**](Bom.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteBom"></a>
# **Invoke-DeleteBom**
> void Invoke-DeleteBom<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-BomId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$BomId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-DeleteBom -BomId $BomId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteBom: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **BomId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Bom"></a>
# **Get-Bom**
> Bom Get-Bom<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-BomId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$BomId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Get-Bom -BomId $BomId
} catch {
    Write-Host ("Exception occurred when calling Get-Bom: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **BomId** | **String**|  | 

### Return type

[**Bom**](Bom.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListBoms"></a>
# **Invoke-ListBoms**
> Bom[] Invoke-ListBoms<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)
$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | Filter by finished product id. (optional)

try {
    $Result = Invoke-ListBoms -Page $Page -PageSize $PageSize -Search $Search -ProductId $ProductId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListBoms: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **ProductId** | **String**| Filter by finished product id. | [optional] 

### Return type

[**Bom[]**](Bom.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Bom"></a>
# **Update-Bom**
> Bom Update-Bom<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-BomId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-BomUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$BomId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$BomUpdate = Initialize-BomUpdate -Components  -Description "MyDescription" -Name "MyName" -OutputQuantity 0 -ProductId "MyProductId" -Status "draft" # BomUpdate | 

try {
    $Result = Update-Bom -BomId $BomId -BomUpdate $BomUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-Bom: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **BomId** | **String**|  | 
 **BomUpdate** | [**BomUpdate**](BomUpdate.md)|  | 

### Return type

[**Bom**](Bom.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

