# PSOpenAPITools.PSOpenAPITools\Api.PackingApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Complete-Packing**](PackingApi.md#Complete-Packing) | **POST** /api/v1/packing/{order_number}/complete | Mark packing as complete and transition order to shipped
[**Get-PackingQueue**](PackingApi.md#Get-PackingQueue) | **GET** /api/v1/packing/queue | Get the packing queue - orders ready for packing
[**Invoke-PrintDeliveryNote**](PackingApi.md#Invoke-PrintDeliveryNote) | **POST** /api/v1/packing/{order_number}/print-delivery-note | Print delivery note (Lieferschein) for an order
[**Invoke-PrintLabel**](PackingApi.md#Invoke-PrintLabel) | **POST** /api/v1/packing/{order_number}/print-label | Print shipping label for an order
[**Invoke-RecordPackingVideo**](PackingApi.md#Invoke-RecordPackingVideo) | **POST** /api/v1/packing/{order_number}/record-video | Record video of packing process


<a id="Complete-Packing"></a>
# **Complete-Packing**
> PackingCompleteResponse Complete-Packing<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PackingCompleteRequest] <PSCustomObject><br>

Mark packing as complete and transition order to shipped

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 
$PackingCompleteRequest = Initialize-PackingCompleteRequest -Notes "MyNotes" -OrderNumber "MyOrderNumber" -ShipmentId "MyShipmentId" -VideoUrl "MyVideoUrl" # PackingCompleteRequest | 

# Mark packing as complete and transition order to shipped
try {
    $Result = Complete-Packing -OrderNumber $OrderNumber -PackingCompleteRequest $PackingCompleteRequest
} catch {
    Write-Host ("Exception occurred when calling Complete-Packing: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 
 **PackingCompleteRequest** | [**PackingCompleteRequest**](PackingCompleteRequest.md)|  | 

### Return type

[**PackingCompleteResponse**](PackingCompleteResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-PackingQueue"></a>
# **Get-PackingQueue**
> PackingQueue Get-PackingQueue<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Search] <String><br>

Get the packing queue - orders ready for packing

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Search = "MySearch" # String |  (optional)

# Get the packing queue - orders ready for packing
try {
    $Result = Get-PackingQueue -Page $Page -PageSize $PageSize -Search $Search
} catch {
    Write-Host ("Exception occurred when calling Get-PackingQueue: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Search** | **String**|  | [optional] 

### Return type

[**PackingQueue**](PackingQueue.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PrintDeliveryNote"></a>
# **Invoke-PrintDeliveryNote**
> PrintDeliveryNoteResponse Invoke-PrintDeliveryNote<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>

Print delivery note (Lieferschein) for an order

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 

# Print delivery note (Lieferschein) for an order
try {
    $Result = Invoke-PrintDeliveryNote -OrderNumber $OrderNumber
} catch {
    Write-Host ("Exception occurred when calling Invoke-PrintDeliveryNote: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 

### Return type

[**PrintDeliveryNoteResponse**](PrintDeliveryNoteResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PrintLabel"></a>
# **Invoke-PrintLabel**
> PrintLabelResponse Invoke-PrintLabel<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>

Print shipping label for an order

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 

# Print shipping label for an order
try {
    $Result = Invoke-PrintLabel -OrderNumber $OrderNumber
} catch {
    Write-Host ("Exception occurred when calling Invoke-PrintLabel: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 

### Return type

[**PrintLabelResponse**](PrintLabelResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-RecordPackingVideo"></a>
# **Invoke-RecordPackingVideo**
> PackingVideoResponse Invoke-RecordPackingVideo<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>

Record video of packing process

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 
$Body =  # AnyType | 

# Record video of packing process
try {
    $Result = Invoke-RecordPackingVideo -OrderNumber $OrderNumber -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-RecordPackingVideo: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**PackingVideoResponse**](PackingVideoResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

