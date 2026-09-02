# PSOpenAPITools.PSOpenAPITools\Api.DeliveryAppointmentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-DeliveryAppointment**](DeliveryAppointmentApi.md#New-DeliveryAppointment) | **POST** /api/v1/delivery-appointments | 
[**Invoke-DeleteDeliveryAppointment**](DeliveryAppointmentApi.md#Invoke-DeleteDeliveryAppointment) | **DELETE** /api/v1/delivery-appointments/{appointment_id} | 
[**Get-DeliveryAppointment**](DeliveryAppointmentApi.md#Get-DeliveryAppointment) | **GET** /api/v1/delivery-appointments/{appointment_id} | 
[**Get-PublicDeliveryAppointmentStatus**](DeliveryAppointmentApi.md#Get-PublicDeliveryAppointmentStatus) | **GET** /api/v1/public/delivery-appointments/status | Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
[**Invoke-ListDeliveryAppointments**](DeliveryAppointmentApi.md#Invoke-ListDeliveryAppointments) | **GET** /api/v1/delivery-appointments | 
[**Request-PublicDeliveryAppointment**](DeliveryAppointmentApi.md#Request-PublicDeliveryAppointment) | **POST** /api/v1/public/delivery-appointments/request | Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by &#x60;code&#x60; — never from the request.
[**Update-DeliveryAppointment**](DeliveryAppointmentApi.md#Update-DeliveryAppointment) | **PUT** /api/v1/delivery-appointments/{appointment_id} | 
[**Update-DeliveryAppointmentStatus**](DeliveryAppointmentApi.md#Update-DeliveryAppointmentStatus) | **PUT** /api/v1/delivery-appointments/{appointment_id}/status | 


<a id="New-DeliveryAppointment"></a>
# **New-DeliveryAppointment**
> DeliveryAppointment New-DeliveryAppointment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-DeliveryAppointmentCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$DeliveryAppointmentCreate = Initialize-DeliveryAppointmentCreate -Email "MyEmail" -Notes "MyNotes" -Phone "MyPhone" -RequestedDate (Get-Date) -Status "requested" -SupplierName "MySupplierName" -TimeSlot "MyTimeSlot" -WarehouseId "MyWarehouseId" # DeliveryAppointmentCreate | 

try {
    $Result = New-DeliveryAppointment -DeliveryAppointmentCreate $DeliveryAppointmentCreate
} catch {
    Write-Host ("Exception occurred when calling New-DeliveryAppointment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **DeliveryAppointmentCreate** | [**DeliveryAppointmentCreate**](DeliveryAppointmentCreate.md)|  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteDeliveryAppointment"></a>
# **Invoke-DeleteDeliveryAppointment**
> void Invoke-DeleteDeliveryAppointment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AppointmentId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AppointmentId = "MyAppointmentId" # String | 

try {
    $Result = Invoke-DeleteDeliveryAppointment -AppointmentId $AppointmentId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteDeliveryAppointment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AppointmentId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-DeliveryAppointment"></a>
# **Get-DeliveryAppointment**
> DeliveryAppointment Get-DeliveryAppointment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AppointmentId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AppointmentId = "MyAppointmentId" # String | 

try {
    $Result = Get-DeliveryAppointment -AppointmentId $AppointmentId
} catch {
    Write-Host ("Exception occurred when calling Get-DeliveryAppointment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AppointmentId** | **String**|  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-PublicDeliveryAppointmentStatus"></a>
# **Get-PublicDeliveryAppointmentStatus**
> PublicDeliveryAppointmentStatusResponse Get-PublicDeliveryAppointmentStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AppointmentId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Email] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Token] <String><br>

Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AppointmentId = "MyAppointmentId" # String | 
$Email = "MyEmail" # String | 
$Token = "MyToken" # String | 

# Supplier/carrier checks appointment status (public, no auth). The appointment is only revealed when email AND token match.
try {
    $Result = Get-PublicDeliveryAppointmentStatus -AppointmentId $AppointmentId -Email $Email -Token $Token
} catch {
    Write-Host ("Exception occurred when calling Get-PublicDeliveryAppointmentStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AppointmentId** | **String**|  | 
 **Email** | **String**|  | 
 **Token** | **String**|  | 

### Return type

[**PublicDeliveryAppointmentStatusResponse**](PublicDeliveryAppointmentStatusResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListDeliveryAppointments"></a>
# **Invoke-ListDeliveryAppointments**
> DeliveryAppointment[] Invoke-ListDeliveryAppointments<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-WarehouseId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-From] <System.Nullable[System.DateTime]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-To] <System.Nullable[System.DateTime]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$WarehouseId = "MyWarehouseId" # String |  (optional)
$From = (Get-Date) # System.DateTime |  (optional)
$To = (Get-Date) # System.DateTime |  (optional)

try {
    $Result = Invoke-ListDeliveryAppointments -Page $Page -PageSize $PageSize -Status $Status -WarehouseId $WarehouseId -From $From -To $To
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListDeliveryAppointments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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
 **From** | **System.DateTime**|  | [optional] 
 **To** | **System.DateTime**|  | [optional] 

### Return type

[**DeliveryAppointment[]**](DeliveryAppointment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Request-PublicDeliveryAppointment"></a>
# **Request-PublicDeliveryAppointment**
> PublicDeliveryAppointmentResponse Request-PublicDeliveryAppointment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PublicDeliveryAppointmentRequest] <PSCustomObject><br>

Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PublicDeliveryAppointmentRequest = Initialize-PublicDeliveryAppointmentRequest -Email "MyEmail" -Notes "MyNotes" -RequestedDate (Get-Date) -SupplierName "MySupplierName" -TimeSlot "MyTimeSlot" -WarehouseCode "MyWarehouseCode" # PublicDeliveryAppointmentRequest | 

# Supplier/carrier requests an inbound delivery slot (public, no auth). The tenant is derived from the warehouse found by `code` — never from the request.
try {
    $Result = Request-PublicDeliveryAppointment -PublicDeliveryAppointmentRequest $PublicDeliveryAppointmentRequest
} catch {
    Write-Host ("Exception occurred when calling Request-PublicDeliveryAppointment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PublicDeliveryAppointmentRequest** | [**PublicDeliveryAppointmentRequest**](PublicDeliveryAppointmentRequest.md)|  | 

### Return type

[**PublicDeliveryAppointmentResponse**](PublicDeliveryAppointmentResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-DeliveryAppointment"></a>
# **Update-DeliveryAppointment**
> DeliveryAppointment Update-DeliveryAppointment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AppointmentId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AppointmentId = "MyAppointmentId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-DeliveryAppointment -AppointmentId $AppointmentId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-DeliveryAppointment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AppointmentId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-DeliveryAppointmentStatus"></a>
# **Update-DeliveryAppointmentStatus**
> DeliveryAppointment Update-DeliveryAppointmentStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AppointmentId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AppointmentStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AppointmentId = "MyAppointmentId" # String | 
$AppointmentStatusUpdate = Initialize-AppointmentStatusUpdate -Status "MyStatus" # AppointmentStatusUpdate | 

try {
    $Result = Update-DeliveryAppointmentStatus -AppointmentId $AppointmentId -AppointmentStatusUpdate $AppointmentStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-DeliveryAppointmentStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AppointmentId** | **String**|  | 
 **AppointmentStatusUpdate** | [**AppointmentStatusUpdate**](AppointmentStatusUpdate.md)|  | 

### Return type

[**DeliveryAppointment**](DeliveryAppointment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

