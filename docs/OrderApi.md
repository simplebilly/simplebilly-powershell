# PSOpenAPITools.PSOpenAPITools\Api.OrderApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Add-OrderTags**](OrderApi.md#Add-OrderTags) | **POST** /api/v1/orders/{order_id}/tags | 
[**Find-OrderByExternalRef**](OrderApi.md#Find-OrderByExternalRef) | **GET** /api/v1/orders/by-ext-ref/{ext_ref} | 
[**Get-Order**](OrderApi.md#Get-Order) | **GET** /api/v1/order/{order_number} | 
[**Get-Orders**](OrderApi.md#Get-Orders) | **GET** /api/v1/orders | 
[**Invoke-PatchOrder**](OrderApi.md#Invoke-PatchOrder) | **PATCH** /api/v1/orders/{order_id} | 
[**Invoke-ReplaceOrderTags**](OrderApi.md#Invoke-ReplaceOrderTags) | **PUT** /api/v1/orders/{order_id}/tags | 
[**Update-OrderState**](OrderApi.md#Update-OrderState) | **PUT** /api/v1/orders/{order_id}/state | 


<a id="Add-OrderTags"></a>
# **Add-OrderTags**
> Order Add-OrderTags<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderTagsRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderId = "MyOrderId" # String | 
$OrderTagsRequest = Initialize-OrderTagsRequest -Tags "MyTags" # OrderTagsRequest | 

try {
    $Result = Add-OrderTags -OrderId $OrderId -OrderTagsRequest $OrderTagsRequest
} catch {
    Write-Host ("Exception occurred when calling Add-OrderTags: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderId** | **String**|  | 
 **OrderTagsRequest** | [**OrderTagsRequest**](OrderTagsRequest.md)|  | 

### Return type

[**Order**](Order.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Find-OrderByExternalRef"></a>
# **Find-OrderByExternalRef**
> Order Find-OrderByExternalRef<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ExtRef] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ExtRef = "MyExtRef" # String | 

try {
    $Result = Find-OrderByExternalRef -ExtRef $ExtRef
} catch {
    Write-Host ("Exception occurred when calling Find-OrderByExternalRef: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ExtRef** | **String**|  | 

### Return type

[**Order**](Order.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Order"></a>
# **Get-Order**
> Order Get-Order<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 

try {
    $Result = Get-Order -OrderNumber $OrderNumber
} catch {
    Write-Host ("Exception occurred when calling Get-Order: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 

### Return type

[**Order**](Order.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Orders"></a>
# **Get-Orders**
> Order[] Get-Orders<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IncludeDeleted] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 1 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)
$IncludeDeleted = $true # Boolean | Soft-delete entities: set true to include rows with `deleted_at` set. (optional)

try {
    $Result = Get-Orders -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-Orders: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **IncludeDeleted** | **Boolean**| Soft-delete entities: set true to include rows with &#x60;deleted_at&#x60; set. | [optional] 

### Return type

[**Order[]**](Order.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PatchOrder"></a>
# **Invoke-PatchOrder**
> Order Invoke-PatchOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderId = "MyOrderId" # String | 
$Body =  # AnyType | 

try {
    $Result = Invoke-PatchOrder -OrderId $OrderId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-PatchOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**Order**](Order.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ReplaceOrderTags"></a>
# **Invoke-ReplaceOrderTags**
> Order Invoke-ReplaceOrderTags<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderTagsRequest] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderId = "MyOrderId" # String | 
$OrderTagsRequest = Initialize-OrderTagsRequest -Tags "MyTags" # OrderTagsRequest | 

try {
    $Result = Invoke-ReplaceOrderTags -OrderId $OrderId -OrderTagsRequest $OrderTagsRequest
} catch {
    Write-Host ("Exception occurred when calling Invoke-ReplaceOrderTags: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderId** | **String**|  | 
 **OrderTagsRequest** | [**OrderTagsRequest**](OrderTagsRequest.md)|  | 

### Return type

[**Order**](Order.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-OrderState"></a>
# **Update-OrderState**
> Order Update-OrderState<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderStateUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderId = "MyOrderId" # String | 
$OrderStateUpdate = Initialize-OrderStateUpdate -SendStateToShop $false -State "MyState" # OrderStateUpdate | 

try {
    $Result = Update-OrderState -OrderId $OrderId -OrderStateUpdate $OrderStateUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-OrderState: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderId** | **String**|  | 
 **OrderStateUpdate** | [**OrderStateUpdate**](OrderStateUpdate.md)|  | 

### Return type

[**Order**](Order.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

