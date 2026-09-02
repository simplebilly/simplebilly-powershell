# PSOpenAPITools.PSOpenAPITools\Api.QuotationApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Quotation**](QuotationApi.md#New-Quotation) | **POST** /api/v1/quotations | 
[**Invoke-DeleteQuotation**](QuotationApi.md#Invoke-DeleteQuotation) | **DELETE** /api/v1/quotations/{quotation_id} | 
[**Invoke-DownloadQuotationPdf**](QuotationApi.md#Invoke-DownloadQuotationPdf) | **GET** /api/v1/quotations/{quotation_id}/pdf | 
[**Get-Quotation**](QuotationApi.md#Get-Quotation) | **GET** /api/v1/quotations/{quotation_id} | 
[**Invoke-ListQuotations**](QuotationApi.md#Invoke-ListQuotations) | **GET** /api/v1/quotations/ | 
[**Invoke-PursueQuotation**](QuotationApi.md#Invoke-PursueQuotation) | **POST** /api/v1/quotations/{quotation_id}/pursue | 
[**Invoke-QuotationRestore**](QuotationApi.md#Invoke-QuotationRestore) | **POST** /api/v1/quotations/{quotation_id}/restore | 
[**Update-Quotation**](QuotationApi.md#Update-Quotation) | **PUT** /api/v1/quotations/{quotation_id} | 


<a id="New-Quotation"></a>
# **New-Quotation**
> Quotation New-Quotation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-QuotationCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$QuotationCreate = Initialize-QuotationCreate -Address  -ContactId "MyContactId" -ContactName "MyContactName" -Currency "MyCurrency" -ExpirationDate (Get-Date) -Files  -Introduction "MyIntroduction" -LineItems  -PrecedingSalesVoucherId "MyPrecedingSalesVoucherId" -PrecedingSalesVoucherType "order_confirmation" -QuotationNumber "MyQuotationNumber" -Remark "MyRemark" -TaxCondition "MyTaxCondition" -Title "MyTitle" -VoucherDate (Get-Date) -VoucherStatus "open" # QuotationCreate | 

try {
    $Result = New-Quotation -QuotationCreate $QuotationCreate
} catch {
    Write-Host ("Exception occurred when calling New-Quotation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **QuotationCreate** | [**QuotationCreate**](QuotationCreate.md)|  | 

### Return type

[**Quotation**](Quotation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteQuotation"></a>
# **Invoke-DeleteQuotation**
> void Invoke-DeleteQuotation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-QuotationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$QuotationId = "MyQuotationId" # String | 

try {
    $Result = Invoke-DeleteQuotation -QuotationId $QuotationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteQuotation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **QuotationId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DownloadQuotationPdf"></a>
# **Invoke-DownloadQuotationPdf**
> void Invoke-DownloadQuotationPdf<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-QuotationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$QuotationId = "MyQuotationId" # String | 

try {
    $Result = Invoke-DownloadQuotationPdf -QuotationId $QuotationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DownloadQuotationPdf: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **QuotationId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Quotation"></a>
# **Get-Quotation**
> Quotation Get-Quotation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-QuotationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$QuotationId = "MyQuotationId" # String | 

try {
    $Result = Get-Quotation -QuotationId $QuotationId
} catch {
    Write-Host ("Exception occurred when calling Get-Quotation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **QuotationId** | **String**|  | 

### Return type

[**Quotation**](Quotation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListQuotations"></a>
# **Invoke-ListQuotations**
> Quotation[] Invoke-ListQuotations<br>
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
    $Result = Invoke-ListQuotations -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListQuotations: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**Quotation[]**](Quotation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PursueQuotation"></a>
# **Invoke-PursueQuotation**
> OrderConfirmation Invoke-PursueQuotation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-QuotationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$QuotationId = "MyQuotationId" # String | 

try {
    $Result = Invoke-PursueQuotation -QuotationId $QuotationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-PursueQuotation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **QuotationId** | **String**|  | 

### Return type

[**OrderConfirmation**](OrderConfirmation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-QuotationRestore"></a>
# **Invoke-QuotationRestore**
> Quotation Invoke-QuotationRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-QuotationId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$QuotationId = "MyQuotationId" # String | 

try {
    $Result = Invoke-QuotationRestore -QuotationId $QuotationId
} catch {
    Write-Host ("Exception occurred when calling Invoke-QuotationRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **QuotationId** | **String**|  | 

### Return type

[**Quotation**](Quotation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Quotation"></a>
# **Update-Quotation**
> Quotation Update-Quotation<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-QuotationId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$QuotationId = "MyQuotationId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-Quotation -QuotationId $QuotationId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-Quotation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **QuotationId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**Quotation**](Quotation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

