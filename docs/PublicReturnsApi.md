# PSOpenAPITools.PSOpenAPITools\Api.PublicReturnsApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Get-PublicReturnStatus**](PublicReturnsApi.md#Get-PublicReturnStatus) | **GET** /api/v1/public/returns/status | Customer checks the status of a return (public, no auth). The return is only revealed when its linked order&#39;s email matches.
[**Invoke-ListPublicReturns**](PublicReturnsApi.md#Invoke-ListPublicReturns) | **GET** /api/v1/public/returns/list | List all returns for an order (public, no auth).
[**Request-PublicReturn**](PublicReturnsApi.md#Request-PublicReturn) | **POST** /api/v1/public/returns/request | Customer requests a return for an order (public, no auth).


<a id="Get-PublicReturnStatus"></a>
# **Get-PublicReturnStatus**
> PublicReturnStatusResponse Get-PublicReturnStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Email] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReturnNumber] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ReturnOrderId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>

Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Email = "MyEmail" # String | 
$ReturnNumber = "MyReturnNumber" # String | Either return_number or return_order_id must be provided. (optional)
$ReturnOrderId = "MyReturnOrderId" # String |  (optional)
$OrderNumber = "MyOrderNumber" # String |  (optional)

# Customer checks the status of a return (public, no auth). The return is only revealed when its linked order's email matches.
try {
    $Result = Get-PublicReturnStatus -Email $Email -ReturnNumber $ReturnNumber -ReturnOrderId $ReturnOrderId -OrderNumber $OrderNumber
} catch {
    Write-Host ("Exception occurred when calling Get-PublicReturnStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Email** | **String**|  | 
 **ReturnNumber** | **String**| Either return_number or return_order_id must be provided. | [optional] 
 **ReturnOrderId** | **String**|  | [optional] 
 **OrderNumber** | **String**|  | [optional] 

### Return type

[**PublicReturnStatusResponse**](PublicReturnStatusResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListPublicReturns"></a>
# **Invoke-ListPublicReturns**
> PublicReturnStatusResponse[] Invoke-ListPublicReturns<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Email] <String><br>

List all returns for an order (public, no auth).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$OrderNumber = "MyOrderNumber" # String | 
$Email = "MyEmail" # String | 

# List all returns for an order (public, no auth).
try {
    $Result = Invoke-ListPublicReturns -OrderNumber $OrderNumber -Email $Email
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListPublicReturns: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **OrderNumber** | **String**|  | 
 **Email** | **String**|  | 

### Return type

[**PublicReturnStatusResponse[]**](PublicReturnStatusResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Request-PublicReturn"></a>
# **Request-PublicReturn**
> PublicReturnResponse Request-PublicReturn<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PublicReturnRequest] <PSCustomObject><br>

Customer requests a return for an order (public, no auth).

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$PublicReturnItem = Initialize-PublicReturnItem -Name "MyName" -ProductId "MyProductId" -Quantity 0 -Reason "MyReason"
$PublicReturnRequest = Initialize-PublicReturnRequest -Email "MyEmail" -Items $PublicReturnItem -Notes "MyNotes" -OrderNumber "MyOrderNumber" # PublicReturnRequest | 

# Customer requests a return for an order (public, no auth).
try {
    $Result = Request-PublicReturn -PublicReturnRequest $PublicReturnRequest
} catch {
    Write-Host ("Exception occurred when calling Request-PublicReturn: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PublicReturnRequest** | [**PublicReturnRequest**](PublicReturnRequest.md)|  | 

### Return type

[**PublicReturnResponse**](PublicReturnResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

