# PSOpenAPITools.PSOpenAPITools\Api.ShipmentApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Shipment**](ShipmentApi.md#New-Shipment) | **POST** /api/v1/shipments | 
[**New-ShipmentFromOrder**](ShipmentApi.md#New-ShipmentFromOrder) | **POST** /api/v1/orders/{order_number}/shipments | Create a real shipment for an order: calls the configured carrier&#39;s label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.
[**Invoke-DeleteShipment**](ShipmentApi.md#Invoke-DeleteShipment) | **DELETE** /api/v1/shipments/{shipment_id} | 
[**Get-Shipment**](ShipmentApi.md#Get-Shipment) | **GET** /api/v1/shipments/{shipment_id} | 
[**Invoke-ListShipments**](ShipmentApi.md#Invoke-ListShipments) | **GET** /api/v1/shipments | 
[**Trace-OrderPublic**](ShipmentApi.md#Trace-OrderPublic) | **POST** /api/v1/public/track | Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).
[**Trace-ShipmentApi**](ShipmentApi.md#Trace-ShipmentApi) | **GET** /api/v1/shipments/{shipment_id}/tracking | 
[**Update-ShipmentStatus**](ShipmentApi.md#Update-ShipmentStatus) | **PUT** /api/v1/shipments/{shipment_id}/status | 


<a id="New-Shipment"></a>
# **New-Shipment**
> Shipment New-Shipment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Shipment] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Shipment = Initialize-Shipment -DeliveredAt (Get-Date) -LabelUrl "MyLabelUrl" -LineItemsShipment  -OrderId "MyOrderId" -RecipientAddress  -ShipmentDate (Get-Date) -ShippingCarrier "MyShippingCarrier" -ShippingCost "MyShippingCost" -ShippingMethod "MyShippingMethod" -SignedBy "MySignedBy" -Status "MyStatus" -TrackingEvents  -TrackingNumber "MyTrackingNumber" -TrackingUrl "MyTrackingUrl" -WeightKg 0 # Shipment | 

try {
    $Result = New-Shipment -Shipment $Shipment
} catch {
    Write-Host ("Exception occurred when calling New-Shipment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Shipment** | [**Shipment**](Shipment.md)|  | 

### Return type

[**Shipment**](Shipment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-ShipmentFromOrder"></a>
# **New-ShipmentFromOrder**
> Shipment New-ShipmentFromOrder<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CreateShipmentRequest] <PSCustomObject><br>

Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 
$CreateShipmentRequest = Initialize-CreateShipmentRequest -Carrier "MyCarrier" -Service "MyService" -WeightKg 0 # CreateShipmentRequest | 

# Create a real shipment for an order: calls the configured carrier's label API, stores the returned tracking/label on a new shipment row, and marks the order as shipped.
try {
    $Result = New-ShipmentFromOrder -OrderNumber $OrderNumber -CreateShipmentRequest $CreateShipmentRequest
} catch {
    Write-Host ("Exception occurred when calling New-ShipmentFromOrder: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 
 **CreateShipmentRequest** | [**CreateShipmentRequest**](CreateShipmentRequest.md)|  | 

### Return type

[**Shipment**](Shipment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteShipment"></a>
# **Invoke-DeleteShipment**
> void Invoke-DeleteShipment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShipmentId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ShipmentId = "MyShipmentId" # String | 

try {
    $Result = Invoke-DeleteShipment -ShipmentId $ShipmentId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteShipment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ShipmentId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Shipment"></a>
# **Get-Shipment**
> Shipment Get-Shipment<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShipmentId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ShipmentId = "MyShipmentId" # String | 

try {
    $Result = Get-Shipment -ShipmentId $ShipmentId
} catch {
    Write-Host ("Exception occurred when calling Get-Shipment: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ShipmentId** | **String**|  | 

### Return type

[**Shipment**](Shipment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListShipments"></a>
# **Invoke-ListShipments**
> Shipment[] Invoke-ListShipments<br>
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
    $Result = Invoke-ListShipments -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListShipments: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**Shipment[]**](Shipment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Trace-OrderPublic"></a>
# **Trace-OrderPublic**
> TrackOrderResponse Trace-OrderPublic<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-TrackOrderRequest] <PSCustomObject><br>

Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$TrackOrderRequest = Initialize-TrackOrderRequest -Email "MyEmail" -OrderNumber "MyOrderNumber" # TrackOrderRequest | 

# Customer-facing tracking lookup: order number + email → shipment status and live carrier events. No auth (public storefront API).
try {
    $Result = Trace-OrderPublic -TrackOrderRequest $TrackOrderRequest
} catch {
    Write-Host ("Exception occurred when calling Trace-OrderPublic: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **TrackOrderRequest** | [**TrackOrderRequest**](TrackOrderRequest.md)|  | 

### Return type

[**TrackOrderResponse**](TrackOrderResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Trace-ShipmentApi"></a>
# **Trace-ShipmentApi**
> TrackingInfo Trace-ShipmentApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShipmentId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ShipmentId = "MyShipmentId" # String | 

try {
    $Result = Trace-ShipmentApi -ShipmentId $ShipmentId
} catch {
    Write-Host ("Exception occurred when calling Trace-ShipmentApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ShipmentId** | **String**|  | 

### Return type

[**TrackingInfo**](TrackingInfo.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ShipmentStatus"></a>
# **Update-ShipmentStatus**
> Shipment Update-ShipmentStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShipmentId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ShipmentStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ShipmentId = "MyShipmentId" # String | 
$ShipmentStatusUpdate = Initialize-ShipmentStatusUpdate -DeliveredAt "MyDeliveredAt" -SignedBy "MySignedBy" -Status "MyStatus" -TrackingNumber "MyTrackingNumber" # ShipmentStatusUpdate | 

try {
    $Result = Update-ShipmentStatus -ShipmentId $ShipmentId -ShipmentStatusUpdate $ShipmentStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-ShipmentStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ShipmentId** | **String**|  | 
 **ShipmentStatusUpdate** | [**ShipmentStatusUpdate**](ShipmentStatusUpdate.md)|  | 

### Return type

[**Shipment**](Shipment.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

