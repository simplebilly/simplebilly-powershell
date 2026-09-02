# PSOpenAPITools.PSOpenAPITools\Api.WarehouseApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Warehouse**](WarehouseApi.md#New-Warehouse) | **POST** /api/v1/warehouses | 
[**Invoke-DeleteWarehouse**](WarehouseApi.md#Invoke-DeleteWarehouse) | **DELETE** /api/v1/warehouses/{warehouse_id} | 
[**Get-Warehouse**](WarehouseApi.md#Get-Warehouse) | **GET** /api/v1/warehouses/{warehouse_id} | 
[**Invoke-ListWarehouses**](WarehouseApi.md#Invoke-ListWarehouses) | **GET** /api/v1/warehouses/ | 
[**Update-Warehouse**](WarehouseApi.md#Update-Warehouse) | **PUT** /api/v1/warehouses/{warehouse_id} | 


<a id="New-Warehouse"></a>
# **New-Warehouse**
> Warehouse New-Warehouse<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Warehouse] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Warehouse = Initialize-Warehouse -AddressCity "MyAddressCity" -AddressCountry "ABW" -AddressStreet "MyAddressStreet" -AddressZip "MyAddressZip" -BinLocations  -Code "MyCode" -IsActive $false -IsDefault $false -Name "MyName" -Notes "MyNotes" # Warehouse | 

try {
    $Result = New-Warehouse -Warehouse $Warehouse
} catch {
    Write-Host ("Exception occurred when calling New-Warehouse: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Warehouse** | [**Warehouse**](Warehouse.md)|  | 

### Return type

[**Warehouse**](Warehouse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteWarehouse"></a>
# **Invoke-DeleteWarehouse**
> void Invoke-DeleteWarehouse<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WarehouseId = "MyWarehouseId" # String | 

try {
    $Result = Invoke-DeleteWarehouse -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteWarehouse: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WarehouseId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Warehouse"></a>
# **Get-Warehouse**
> Warehouse Get-Warehouse<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WarehouseId = "MyWarehouseId" # String | 

try {
    $Result = Get-Warehouse -WarehouseId $WarehouseId
} catch {
    Write-Host ("Exception occurred when calling Get-Warehouse: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WarehouseId** | **String**|  | 

### Return type

[**Warehouse**](Warehouse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListWarehouses"></a>
# **Invoke-ListWarehouses**
> Warehouse[] Invoke-ListWarehouses<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-IsActive] <System.Nullable[Boolean]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)
$IsActive = $true # Boolean |  (optional)

try {
    $Result = Invoke-ListWarehouses -Page $Page -PageSize $PageSize -Search $Search -IsActive $IsActive
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListWarehouses: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 
 **IsActive** | **Boolean**|  | [optional] 

### Return type

[**Warehouse[]**](Warehouse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Warehouse"></a>
# **Update-Warehouse**
> Warehouse Update-Warehouse<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$WarehouseId = "MyWarehouseId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-Warehouse -WarehouseId $WarehouseId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-Warehouse: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **WarehouseId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**Warehouse**](Warehouse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

