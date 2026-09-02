# PSOpenAPITools.PSOpenAPITools\Api.ProformaInvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Convert-ProformaToInvoice**](ProformaInvoiceApi.md#Convert-ProformaToInvoice) | **POST** /api/v1/proforma-invoices/{proforma_id}/convert | 
[**New-ProformaInvoice**](ProformaInvoiceApi.md#New-ProformaInvoice) | **POST** /api/v1/proforma-invoices | 
[**Invoke-DeleteProformaInvoice**](ProformaInvoiceApi.md#Invoke-DeleteProformaInvoice) | **DELETE** /api/v1/proforma-invoices/{proforma_id} | 
[**Get-ProformaInvoice**](ProformaInvoiceApi.md#Get-ProformaInvoice) | **GET** /api/v1/proforma-invoices/{proforma_id} | 
[**Invoke-ListProformaInvoices**](ProformaInvoiceApi.md#Invoke-ListProformaInvoices) | **GET** /api/v1/proforma-invoices/ | 
[**Update-ProformaInvoice**](ProformaInvoiceApi.md#Update-ProformaInvoice) | **PUT** /api/v1/proforma-invoices/{proforma_id} | 


<a id="Convert-ProformaToInvoice"></a>
# **Convert-ProformaToInvoice**
> ConvertResponse Convert-ProformaToInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProformaId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProformaId = "MyProformaId" # String | 

try {
    $Result = Convert-ProformaToInvoice -ProformaId $ProformaId
} catch {
    Write-Host ("Exception occurred when calling Convert-ProformaToInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProformaId** | **String**|  | 

### Return type

[**ConvertResponse**](ConvertResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="New-ProformaInvoice"></a>
# **New-ProformaInvoice**
> ProformaInvoice New-ProformaInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProformaInvoice] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProformaInvoice = Initialize-ProformaInvoice -ConvertedAt (Get-Date) -ConvertedToInvoiceId "MyConvertedToInvoiceId" -Currency "ADP" -CustomerId "MyCustomerId" -CustomerSnapshot  -IssueDate (Get-Date) -LineItems  -Notes "MyNotes" -OrderNumber "MyOrderNumber" -PaymentDueDate (Get-Date) -QuotationId "MyQuotationId" -Status "draft" -Subtotal "MySubtotal" -TotalAmount "MyTotalAmount" -TotalTax "MyTotalTax" # ProformaInvoice | 

try {
    $Result = New-ProformaInvoice -ProformaInvoice $ProformaInvoice
} catch {
    Write-Host ("Exception occurred when calling New-ProformaInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProformaInvoice** | [**ProformaInvoice**](ProformaInvoice.md)|  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteProformaInvoice"></a>
# **Invoke-DeleteProformaInvoice**
> void Invoke-DeleteProformaInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProformaId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProformaId = "MyProformaId" # String | 

try {
    $Result = Invoke-DeleteProformaInvoice -ProformaId $ProformaId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteProformaInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProformaId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-ProformaInvoice"></a>
# **Get-ProformaInvoice**
> ProformaInvoice Get-ProformaInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProformaId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProformaId = "MyProformaId" # String | 

try {
    $Result = Get-ProformaInvoice -ProformaId $ProformaId
} catch {
    Write-Host ("Exception occurred when calling Get-ProformaInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProformaId** | **String**|  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ListProformaInvoices"></a>
# **Invoke-ListProformaInvoices**
> ProformaInvoice[] Invoke-ListProformaInvoices<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Page] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PageSize] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-OrderNumber] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Page = 56 # Int32 |  (optional)
$PageSize = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)
$CustomerId = "MyCustomerId" # String |  (optional)
$OrderNumber = "MyOrderNumber" # String |  (optional)

try {
    $Result = Invoke-ListProformaInvoices -Page $Page -PageSize $PageSize -Status $Status -CustomerId $CustomerId -OrderNumber $OrderNumber
} catch {
    Write-Host ("Exception occurred when calling Invoke-ListProformaInvoices: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Page** | **Int32**|  | [optional] 
 **PageSize** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 
 **CustomerId** | **String**|  | [optional] 
 **OrderNumber** | **String**|  | [optional] 

### Return type

[**ProformaInvoice[]**](ProformaInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-ProformaInvoice"></a>
# **Update-ProformaInvoice**
> ProformaInvoice Update-ProformaInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-ProformaId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ProformaId = "MyProformaId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-ProformaInvoice -ProformaId $ProformaId -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-ProformaInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ProformaId** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**ProformaInvoice**](ProformaInvoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

