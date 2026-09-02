# PSOpenAPITools.PSOpenAPITools\Api.InventoryCountApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-InventoryCount**](InventoryCountApi.md#New-InventoryCount) | **POST** /api/v1/inventory-counts | 
[**Invoke-DeleteInventoryCount**](InventoryCountApi.md#Invoke-DeleteInventoryCount) | **DELETE** /api/v1/inventory-counts/{inventory_count_id} | 
[**New-InventoryCount**](InventoryCountApi.md#New-InventoryCount) | **POST** /api/v1/inventory-counts/generate | 
[**Get-InventoryCount**](InventoryCountApi.md#Get-InventoryCount) | **GET** /api/v1/inventory-counts/{inventory_count_id} | 
[**Invoke-ListInventoryCounts**](InventoryCountApi.md#Invoke-ListInventoryCounts) | **GET** /api/v1/inventory-counts/ | 
[**Update-InventoryCount**](InventoryCountApi.md#Update-InventoryCount) | **PUT** /api/v1/inventory-counts/{inventory_count_id} | 
[**Update-InventoryCountStatus**](InventoryCountApi.md#Update-InventoryCountStatus) | **PUT** /api/v1/inventory-counts/{inventory_count_id}/status | 


<a id="New-InventoryCount"></a>
# **New-InventoryCount**
> InventoryCount New-InventoryCount<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InventoryCount] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$InventoryCount = Initialize-InventoryCount -CountDate (Get-Date) -CountNumber "MyCountNumber" -LineItems  -Notes "MyNotes" -Status "draft" -WarehouseId "MyWarehouseId" # InventoryCount | 

try {
    $Result = New-InventoryCount -InventoryCount $InventoryCount
} catch {
    Write-Host ("Exception occurred when calling New-InventoryCount: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **InventoryCount** | [**InventoryCount**](InventoryCount.md)|  | 

### Return type

[**InventoryCount**](InventoryCount.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteInventoryCount"></a>
# **Invoke-DeleteInventoryCount**
> void Invoke-DeleteInventoryCount<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InventoryCountId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$InventoryCountId = "MyInventoryCountId" # String | 

try {
    $Result = Invoke-DeleteInventoryCount -InventoryCountId $InventoryCountId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteInventoryCount: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **InventoryCountId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-InventoryCount"></a>
# **New-InventoryCount**
> InventoryCount New-InventoryCount<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-GenerateCountRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$GenerateCountRequest = Initialize-GenerateCountRequest -Notes "MyNotes" -ProductIds "MyProductIds" -WarehouseId "MyWarehouseId" # GenerateCountRequest | 

try {
    $Result = New-InventoryCount -GenerateCountRequest $GenerateCountRequest
} catch {
    Write-Host ("Exception occurred when calling New-InventoryCount: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **GenerateCountRequest** | [**GenerateCountRequest**](GenerateCountRequest.md)|  | 

### Return type

[**InventoryCount**](InventoryCount.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-InventoryCount"></a>
# **Get-InventoryCount**
> InventoryCount Get-InventoryCount<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InventoryCountId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$InventoryCountId = "MyInventoryCountId" # String | 

try {
    $Result = Get-InventoryCount -InventoryCountId $InventoryCountId
} catch {
    Write-Host ("Exception occurred when calling Get-InventoryCount: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **InventoryCountId** | **String**|  | 

### Return type

[**InventoryCount**](InventoryCount.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListInventoryCounts"></a>
# **Invoke-ListInventoryCounts**
> InventoryCount[] Invoke-ListInventoryCounts<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$WarehouseId = "MyWarehouseId" # String |  (optional)

try {
    $Result = Invoke-ListInventoryCounts -Page $Page -PageSize $PageSize -Status $Status -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListInventoryCounts: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **WarehouseId** | **String**|  | [optional] 

### Return type

[**InventoryCount[]**](InventoryCount.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-InventoryCount"></a>
# **Update-InventoryCount**
> InventoryCount Update-InventoryCount<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InventoryCountId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$InventoryCountId = "MyInventoryCountId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-InventoryCount -InventoryCountId $InventoryCountId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-InventoryCount: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **InventoryCountId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**InventoryCount**](InventoryCount.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-InventoryCountStatus"></a>
# **Update-InventoryCountStatus**
> InventoryCount Update-InventoryCountStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InventoryCountId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InventoryCountStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$InventoryCountId = "MyInventoryCountId" # String | 
$InventoryCountStatusUpdate = Initialize-InventoryCountStatusUpdate -Status "MyStatus" # InventoryCountStatusUpdate | 

try {
    $Result = Update-InventoryCountStatus -InventoryCountId $InventoryCountId -InventoryCountStatusUpdate $InventoryCountStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-InventoryCountStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **InventoryCountId** | **String**|  | 
 **InventoryCountStatusUpdate** | [**InventoryCountStatusUpdate**](InventoryCountStatusUpdate.md)|  | 

### Return type

[**InventoryCount**](InventoryCount.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

