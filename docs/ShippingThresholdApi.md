# PSOpenAPITools.PSOpenAPITools\Api.ShippingThresholdApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ShippingThreshold**](ShippingThresholdApi.md#New-ShippingThreshold) | **POST** /api/v1/shipping-thresholds | 
[**Invoke-DeleteShippingThreshold**](ShippingThresholdApi.md#Invoke-DeleteShippingThreshold) | **DELETE** /api/v1/shipping-thresholds/{threshold_id} | 
[**Get-Deliverable**](ShippingThresholdApi.md#Get-Deliverable) | **GET** /api/v1/shipping-thresholds/deliverable | 
[**Get-ShippingThreshold**](ShippingThresholdApi.md#Get-ShippingThreshold) | **GET** /api/v1/shipping-thresholds/{threshold_id} | 
[**Invoke-ListShippingThresholds**](ShippingThresholdApi.md#Invoke-ListShippingThresholds) | **GET** /api/v1/shipping-thresholds/ | 
[**Update-ShippingThreshold**](ShippingThresholdApi.md#Update-ShippingThreshold) | **PUT** /api/v1/shipping-thresholds/{threshold_id} | 


<a id="New-ShippingThreshold"></a>
# **New-ShippingThreshold**
> ShippingThreshold New-ShippingThreshold<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShippingThresholdCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ShippingThresholdCreate = Initialize-ShippingThresholdCreate -IsActive $false -MaxSellable 0 -Name "MyName" -Notes "MyNotes" -ProductId "MyProductId" -ReserveStock 0 -WarehouseId "MyWarehouseId" # ShippingThresholdCreate | 

try {
    $Result = New-ShippingThreshold -ShippingThresholdCreate $ShippingThresholdCreate
} catch {
    Write-Host ("Exception occurred when calling New-ShippingThreshold: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ShippingThresholdCreate** | [**ShippingThresholdCreate**](ShippingThresholdCreate.md)|  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteShippingThreshold"></a>
# **Invoke-DeleteShippingThreshold**
> void Invoke-DeleteShippingThreshold<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ThresholdId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ThresholdId = "MyThresholdId" # String | 

try {
    $Result = Invoke-DeleteShippingThreshold -ThresholdId $ThresholdId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteShippingThreshold: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ThresholdId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Deliverable"></a>
# **Get-Deliverable**
> DeliverableResponse Get-Deliverable<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$WarehouseId = "MyWarehouseId" # String |  (optional)

try {
    $Result = Get-Deliverable -ProductId $ProductId -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Get-Deliverable: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProductId** | **String**|  | 
 **WarehouseId** | **String**|  | [optional] 

### Return type

[**DeliverableResponse**](DeliverableResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ShippingThreshold"></a>
# **Get-ShippingThreshold**
> ShippingThreshold Get-ShippingThreshold<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ThresholdId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ThresholdId = "MyThresholdId" # String | 

try {
    $Result = Get-ShippingThreshold -ThresholdId $ThresholdId
} catch {
    Write-Host ("Exception occurred when calling Get-ShippingThreshold: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ThresholdId** | **String**|  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListShippingThresholds"></a>
# **Invoke-ListShippingThresholds**
> ShippingThreshold[] Invoke-ListShippingThresholds<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IsActive] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String |  (optional)
$WarehouseId = "MyWarehouseId" # String |  (optional)
$IsActive = $true # Boolean |  (optional)

try {
    $Result = Invoke-ListShippingThresholds -Page $Page -PageSize $PageSize -ProductId $ProductId -WarehouseId $WarehouseId -IsActive $IsActive
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListShippingThresholds: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **ProductId** | **String**|  | [optional] 
 **WarehouseId** | **String**|  | [optional] 
 **IsActive** | **Boolean**|  | [optional] 

### Return type

[**ShippingThreshold[]**](ShippingThreshold.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ShippingThreshold"></a>
# **Update-ShippingThreshold**
> ShippingThreshold Update-ShippingThreshold<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ThresholdId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShippingThresholdUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ThresholdId = "MyThresholdId" # String | 
$ShippingThresholdUpdate = Initialize-ShippingThresholdUpdate -IsActive $false -MaxSellable 0 -Name "MyName" -Notes "MyNotes" -ProductId "MyProductId" -ReserveStock 0 -WarehouseId "MyWarehouseId" # ShippingThresholdUpdate | 

try {
    $Result = Update-ShippingThreshold -ThresholdId $ThresholdId -ShippingThresholdUpdate $ShippingThresholdUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ShippingThreshold: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ThresholdId** | **String**|  | 
 **ShippingThresholdUpdate** | [**ShippingThresholdUpdate**](ShippingThresholdUpdate.md)|  | 

### Return type

[**ShippingThreshold**](ShippingThreshold.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

