# PSOpenAPITools.PSOpenAPITools\Api.StockMovementApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-StockMovement**](StockMovementApi.md#Get-StockMovement) | **GET** /api/v1/stock-movements/{movement_id} | 
[**Invoke-ListStockMovements**](StockMovementApi.md#Invoke-ListStockMovements) | **GET** /api/v1/stock-movements/ | 


<a id="Get-StockMovement"></a>
# **Get-StockMovement**
> StockMovement Get-StockMovement<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-MovementId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$MovementId = "MyMovementId" # String | 

try {
    $Result = Get-StockMovement -MovementId $MovementId
} catch {
    Write-Host ("Exception occurred when calling Get-StockMovement: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **MovementId** | **String**|  | 

### Return type

[**StockMovement**](StockMovement.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListStockMovements"></a>
# **Invoke-ListStockMovements**
> StockMovement[] Invoke-ListStockMovements<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProductId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-MovementType] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-From] <System.Nullable[System.DateTime]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-To] <System.Nullable[System.DateTime]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$ProductId = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String |  (optional)
$WarehouseId = "MyWarehouseId" # String |  (optional)
$MovementType = "MyMovementType" # String |  (optional)
$From = (Get-Date) # System.DateTime | Only movements on or after this date (inclusive). (optional)
$To = (Get-Date) # System.DateTime | Only movements on or before this date (inclusive). (optional)

try {
    $Result = Invoke-ListStockMovements -Page $Page -PageSize $PageSize -ProductId $ProductId -WarehouseId $WarehouseId -MovementType $MovementType -From $From -To $To
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListStockMovements: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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
 **MovementType** | **String**|  | [optional] 
 **From** | **System.DateTime**| Only movements on or after this date (inclusive). | [optional] 
 **To** | **System.DateTime**| Only movements on or before this date (inclusive). | [optional] 

### Return type

[**StockMovement[]**](StockMovement.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

