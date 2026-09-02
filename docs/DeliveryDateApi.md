# PSOpenAPITools.PSOpenAPITools\Api.DeliveryDateApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-DeliveryDate**](DeliveryDateApi.md#New-DeliveryDate) | **POST** /api/v1/delivery-dates | 
[**Invoke-DeleteDeliveryDate**](DeliveryDateApi.md#Invoke-DeleteDeliveryDate) | **DELETE** /api/v1/delivery-dates/{delivery_date_id} | 
[**Get-DeliveryDate**](DeliveryDateApi.md#Get-DeliveryDate) | **GET** /api/v1/delivery-dates/{delivery_date_id} | 
[**Get-DeliveryPerformance**](DeliveryDateApi.md#Get-DeliveryPerformance) | **GET** /api/v1/delivery-dates/performance | On-time performance summary: how many promised delivery dates were met within a period.
[**Invoke-ListDeliveryDates**](DeliveryDateApi.md#Invoke-ListDeliveryDates) | **GET** /api/v1/delivery-dates/ | 
[**Update-DeliveryDate**](DeliveryDateApi.md#Update-DeliveryDate) | **PUT** /api/v1/delivery-dates/{delivery_date_id} | 
[**Update-DeliveryDateStatus**](DeliveryDateApi.md#Update-DeliveryDateStatus) | **PUT** /api/v1/delivery-dates/{delivery_date_id}/status | 


<a id="New-DeliveryDate"></a>
# **New-DeliveryDate**
> DeliveryDate New-DeliveryDate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryDateCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryDateCreate = Initialize-DeliveryDateCreate -CustomerId "MyCustomerId" -FulfilledDate (Get-Date) -Note "MyNote" -OrderNumber "MyOrderNumber" -OriginalDate (Get-Date) -ProductId "MyProductId" -PromisedDate (Get-Date) -Status "promised" # DeliveryDateCreate | 

try {
    $Result = New-DeliveryDate -DeliveryDateCreate $DeliveryDateCreate
} catch {
    Write-Host ("Exception occurred when calling New-DeliveryDate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryDateCreate** | [**DeliveryDateCreate**](DeliveryDateCreate.md)|  | 

### Return type

[**DeliveryDate**](DeliveryDate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteDeliveryDate"></a>
# **Invoke-DeleteDeliveryDate**
> void Invoke-DeleteDeliveryDate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryDateId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryDateId = "MyDeliveryDateId" # String | 

try {
    $Result = Invoke-DeleteDeliveryDate -DeliveryDateId $DeliveryDateId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteDeliveryDate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryDateId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-DeliveryDate"></a>
# **Get-DeliveryDate**
> DeliveryDate Get-DeliveryDate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryDateId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryDateId = "MyDeliveryDateId" # String | 

try {
    $Result = Get-DeliveryDate -DeliveryDateId $DeliveryDateId
} catch {
    Write-Host ("Exception occurred when calling Get-DeliveryDate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryDateId** | **String**|  | 

### Return type

[**DeliveryDate**](DeliveryDate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-DeliveryPerformance"></a>
# **Get-DeliveryPerformance**
> AnyType Get-DeliveryPerformance<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-From] <System.Nullable[System.DateTime]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-To] <System.Nullable[System.DateTime]><br>

On-time performance summary: how many promised delivery dates were met within a period.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$OrderNumber = "MyOrderNumber" # String |  (optional)
$Status = "MyStatus" # String |  (optional)
$From = (Get-Date) # System.DateTime | Only dates on or after this date. (optional)
$To = (Get-Date) # System.DateTime | Only dates on or before this date. (optional)

# On-time performance summary: how many promised delivery dates were met within a period.
try {
    $Result = Get-DeliveryPerformance -Page $Page -PageSize $PageSize -OrderNumber $OrderNumber -Status $Status -From $From -To $To
} catch {
    Write-Host ("Exception occurred when calling Get-DeliveryPerformance: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **OrderNumber** | **String**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **From** | **System.DateTime**| Only dates on or after this date. | [optional] 
 **To** | **System.DateTime**| Only dates on or before this date. | [optional] 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListDeliveryDates"></a>
# **Invoke-ListDeliveryDates**
> DeliveryDate[] Invoke-ListDeliveryDates<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-From] <System.Nullable[System.DateTime]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-To] <System.Nullable[System.DateTime]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$OrderNumber = "MyOrderNumber" # String |  (optional)
$Status = "MyStatus" # String |  (optional)
$From = (Get-Date) # System.DateTime | Only dates on or after this date. (optional)
$To = (Get-Date) # System.DateTime | Only dates on or before this date. (optional)

try {
    $Result = Invoke-ListDeliveryDates -Page $Page -PageSize $PageSize -OrderNumber $OrderNumber -Status $Status -From $From -To $To
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListDeliveryDates: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **OrderNumber** | **String**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **From** | **System.DateTime**| Only dates on or after this date. | [optional] 
 **To** | **System.DateTime**| Only dates on or before this date. | [optional] 

### Return type

[**DeliveryDate[]**](DeliveryDate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-DeliveryDate"></a>
# **Update-DeliveryDate**
> DeliveryDate Update-DeliveryDate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryDateId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryDateId = "MyDeliveryDateId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-DeliveryDate -DeliveryDateId $DeliveryDateId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-DeliveryDate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryDateId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**DeliveryDate**](DeliveryDate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-DeliveryDateStatus"></a>
# **Update-DeliveryDateStatus**
> DeliveryDate Update-DeliveryDateStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryDateId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryDateStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryDateId = "MyDeliveryDateId" # String | 
$DeliveryDateStatusUpdate = Initialize-DeliveryDateStatusUpdate -Status "MyStatus" # DeliveryDateStatusUpdate | 

try {
    $Result = Update-DeliveryDateStatus -DeliveryDateId $DeliveryDateId -DeliveryDateStatusUpdate $DeliveryDateStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-DeliveryDateStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryDateId** | **String**|  | 
 **DeliveryDateStatusUpdate** | [**DeliveryDateStatusUpdate**](DeliveryDateStatusUpdate.md)|  | 

### Return type

[**DeliveryDate**](DeliveryDate.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

