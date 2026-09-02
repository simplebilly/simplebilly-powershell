# PSOpenAPITools.PSOpenAPITools\Api.ReturnOrderApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-ReturnOrder**](ReturnOrderApi.md#New-ReturnOrder) | **POST** /api/v1/returns | 
[**Invoke-DeleteReturnOrder**](ReturnOrderApi.md#Invoke-DeleteReturnOrder) | **DELETE** /api/v1/returns/{return_order_id} | 
[**Get-ReturnOrder**](ReturnOrderApi.md#Get-ReturnOrder) | **GET** /api/v1/returns/{return_order_id} | 
[**Invoke-ListReturnOrders**](ReturnOrderApi.md#Invoke-ListReturnOrders) | **GET** /api/v1/returns/ | 
[**Invoke-ReturnLogisticsQueue**](ReturnOrderApi.md#Invoke-ReturnLogisticsQueue) | **GET** /api/v1/returns/logistics-queue | 
[**Invoke-ReturnLogisticsSummary**](ReturnOrderApi.md#Invoke-ReturnLogisticsSummary) | **GET** /api/v1/returns/logistics-summary | Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.
[**Update-ReturnOrder**](ReturnOrderApi.md#Update-ReturnOrder) | **PUT** /api/v1/returns/{return_order_id} | 
[**Update-ReturnOrderStatus**](ReturnOrderApi.md#Update-ReturnOrderStatus) | **PUT** /api/v1/returns/{return_order_id}/status | 


<a id="New-ReturnOrder"></a>
# **New-ReturnOrder**
> ReturnOrder New-ReturnOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReturnOrder] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ReturnOrder = Initialize-ReturnOrder -CustomerContactId "MyCustomerContactId" -CustomerName "MyCustomerName" -LineItems  -Notes "MyNotes" -OrderId "MyOrderId" -OrderNumber "MyOrderNumber" -ReturnNumber "MyReturnNumber" -ReturnReason "MyReturnReason" -Status "requested" -WarehouseId "MyWarehouseId" # ReturnOrder | 

try {
    $Result = New-ReturnOrder -ReturnOrder $ReturnOrder
} catch {
    Write-Host ("Exception occurred when calling New-ReturnOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ReturnOrder** | [**ReturnOrder**](ReturnOrder.md)|  | 

### Return type

[**ReturnOrder**](ReturnOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteReturnOrder"></a>
# **Invoke-DeleteReturnOrder**
> void Invoke-DeleteReturnOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReturnOrderId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ReturnOrderId = "MyReturnOrderId" # String | 

try {
    $Result = Invoke-DeleteReturnOrder -ReturnOrderId $ReturnOrderId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteReturnOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ReturnOrderId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ReturnOrder"></a>
# **Get-ReturnOrder**
> ReturnOrder Get-ReturnOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReturnOrderId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ReturnOrderId = "MyReturnOrderId" # String | 

try {
    $Result = Get-ReturnOrder -ReturnOrderId $ReturnOrderId
} catch {
    Write-Host ("Exception occurred when calling Get-ReturnOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ReturnOrderId** | **String**|  | 

### Return type

[**ReturnOrder**](ReturnOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListReturnOrders"></a>
# **Invoke-ListReturnOrders**
> ReturnOrder[] Invoke-ListReturnOrders<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerName] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$CustomerName = "MyCustomerName" # String |  (optional)
$OrderNumber = "MyOrderNumber" # String |  (optional)

try {
    $Result = Invoke-ListReturnOrders -Page $Page -PageSize $PageSize -Status $Status -CustomerName $CustomerName -OrderNumber $OrderNumber
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListReturnOrders: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **CustomerName** | **String**|  | [optional] 
 **OrderNumber** | **String**|  | [optional] 

### Return type

[**ReturnOrder[]**](ReturnOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ReturnLogisticsQueue"></a>
# **Invoke-ReturnLogisticsQueue**
> ReturnLogisticsQueueItem[] Invoke-ReturnLogisticsQueue<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ReturnLogisticsQueue
} catch {
    Write-Host ("Exception occurred when calling Invoke-ReturnLogisticsQueue: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ReturnLogisticsQueueItem[]**](ReturnLogisticsQueueItem.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ReturnLogisticsSummary"></a>
# **Invoke-ReturnLogisticsSummary**
> ReturnLogisticsSummary Invoke-ReturnLogisticsSummary<br>

Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# Returns-logistics aggregation for the dashboard: quantities received, restocked and scrapped per warehouse.
try {
    $Result = Invoke-ReturnLogisticsSummary
} catch {
    Write-Host ("Exception occurred when calling Invoke-ReturnLogisticsSummary: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ReturnLogisticsSummary**](ReturnLogisticsSummary.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ReturnOrder"></a>
# **Update-ReturnOrder**
> ReturnOrder Update-ReturnOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReturnOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ReturnOrderId = "MyReturnOrderId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-ReturnOrder -ReturnOrderId $ReturnOrderId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-ReturnOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ReturnOrderId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**ReturnOrder**](ReturnOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ReturnOrderStatus"></a>
# **Update-ReturnOrderStatus**
> ReturnOrder Update-ReturnOrderStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReturnOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReturnOrderStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ReturnOrderId = "MyReturnOrderId" # String | 
$ReturnOrderStatusUpdate = Initialize-ReturnOrderStatusUpdate -Status "MyStatus" # ReturnOrderStatusUpdate | 

try {
    $Result = Update-ReturnOrderStatus -ReturnOrderId $ReturnOrderId -ReturnOrderStatusUpdate $ReturnOrderStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ReturnOrderStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ReturnOrderId** | **String**|  | 
 **ReturnOrderStatusUpdate** | [**ReturnOrderStatusUpdate**](ReturnOrderStatusUpdate.md)|  | 

### Return type

[**ReturnOrder**](ReturnOrder.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

