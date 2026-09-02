# PSOpenAPITools.PSOpenAPITools\Api.RfqApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Convert-Rfq**](RfqApi.md#Convert-Rfq) | **POST** /api/v1/rfqs/{rfq_id}/convert | Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as &#x60;converted&#x60;.
[**New-Rfq**](RfqApi.md#New-Rfq) | **POST** /api/v1/rfqs | 
[**Invoke-DeleteRfq**](RfqApi.md#Invoke-DeleteRfq) | **DELETE** /api/v1/rfqs/{rfq_id} | 
[**Get-Rfq**](RfqApi.md#Get-Rfq) | **GET** /api/v1/rfqs/{rfq_id} | 
[**Invoke-ListRfqs**](RfqApi.md#Invoke-ListRfqs) | **GET** /api/v1/rfqs/ | 
[**Update-Rfq**](RfqApi.md#Update-Rfq) | **PUT** /api/v1/rfqs/{rfq_id} | 
[**Update-RfqStatus**](RfqApi.md#Update-RfqStatus) | **PUT** /api/v1/rfqs/{rfq_id}/status | 


<a id="Convert-Rfq"></a>
# **Convert-Rfq**
> AnyType Convert-Rfq<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RfqId] <String><br>

Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RfqId = "MyRfqId" # String | 

# Convert an RFQ into a draft purchase order using the quoted unit prices (falling back to the requested prices, then leaving them blank). Marks the RFQ as `converted`.
try {
    $Result = Convert-Rfq -RfqId $RfqId
} catch {
    Write-Host ("Exception occurred when calling Convert-Rfq: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RfqId** | **String**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-Rfq"></a>
# **New-Rfq**
> Rfq New-Rfq<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Rfq] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Rfq = Initialize-Rfq -Currency "MyCurrency" -LineItems  -Notes "MyNotes" -RequestedDate (Get-Date) -ResponseDate (Get-Date) -RfqNumber "MyRfqNumber" -Status "draft" -SupplierContactId "MySupplierContactId" -SupplierName "MySupplierName" # Rfq | 

try {
    $Result = New-Rfq -Rfq $Rfq
} catch {
    Write-Host ("Exception occurred when calling New-Rfq: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Rfq** | [**Rfq**](Rfq.md)|  | 

### Return type

[**Rfq**](Rfq.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteRfq"></a>
# **Invoke-DeleteRfq**
> void Invoke-DeleteRfq<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RfqId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RfqId = "MyRfqId" # String | 

try {
    $Result = Invoke-DeleteRfq -RfqId $RfqId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteRfq: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RfqId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Rfq"></a>
# **Get-Rfq**
> Rfq Get-Rfq<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RfqId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RfqId = "MyRfqId" # String | 

try {
    $Result = Get-Rfq -RfqId $RfqId
} catch {
    Write-Host ("Exception occurred when calling Get-Rfq: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RfqId** | **String**|  | 

### Return type

[**Rfq**](Rfq.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListRfqs"></a>
# **Invoke-ListRfqs**
> Rfq[] Invoke-ListRfqs<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-SupplierName] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$SupplierName = "MySupplierName" # String |  (optional)

try {
    $Result = Invoke-ListRfqs -Page $Page -PageSize $PageSize -Status $Status -SupplierName $SupplierName
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListRfqs: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **SupplierName** | **String**|  | [optional] 

### Return type

[**Rfq[]**](Rfq.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Rfq"></a>
# **Update-Rfq**
> Rfq Update-Rfq<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RfqId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RfqId = "MyRfqId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-Rfq -RfqId $RfqId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-Rfq: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RfqId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**Rfq**](Rfq.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-RfqStatus"></a>
# **Update-RfqStatus**
> Rfq Update-RfqStatus<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RfqId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-RfqStatusUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$RfqId = "MyRfqId" # String | 
$RfqStatusUpdate = Initialize-RfqStatusUpdate -Status "MyStatus" # RfqStatusUpdate | 

try {
    $Result = Update-RfqStatus -RfqId $RfqId -RfqStatusUpdate $RfqStatusUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-RfqStatus: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **RfqId** | **String**|  | 
 **RfqStatusUpdate** | [**RfqStatusUpdate**](RfqStatusUpdate.md)|  | 

### Return type

[**Rfq**](Rfq.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

