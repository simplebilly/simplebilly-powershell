# PSOpenAPITools.PSOpenAPITools\Api.InvoiceApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Invoice**](InvoiceApi.md#New-Invoice) | **POST** /api/v1/invoices | 
[**Invoke-DeleteInvoice**](InvoiceApi.md#Invoke-DeleteInvoice) | **DELETE** /api/v1/invoices/{id} | 
[**Invoke-DownloadInvoicePdf**](InvoiceApi.md#Invoke-DownloadInvoicePdf) | **GET** /api/v1/invoices/{id}/pdf | 
[**Get-Invoice**](InvoiceApi.md#Get-Invoice) | **GET** /api/v1/invoices/{id} | 
[**Get-InvoicePdfUrl**](InvoiceApi.md#Get-InvoicePdfUrl) | **GET** /api/v1/invoices/{id}/pdf-url | 
[**Get-Invoices**](InvoiceApi.md#Get-Invoices) | **GET** /api/v1/invoices/ | 
[**ConvertTo-voiceRestore**](InvoiceApi.md#ConvertTo-voiceRestore) | **POST** /api/v1/invoices/{id}/restore | 
[**Update-Invoice**](InvoiceApi.md#Update-Invoice) | **PUT** /api/v1/invoices/{id} | 


<a id="New-Invoice"></a>
# **New-Invoice**
> Invoice New-Invoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-InvoiceCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$InvoiceCreate = Initialize-InvoiceCreate -Attachments  -BillingPeriodEnd (Get-Date) -BillingPeriodStart (Get-Date) -CancellationDate (Get-Date) -CancellationInvoiceId "MyCancellationInvoiceId" -CancellationReason "MyCancellationReason" -ContractId "MyContractId" -Currency "ADP" -CustomerId "MyCustomerId" -DiscountAmount "MyDiscountAmount" -DiscountDays 0 -DiscountPercentage "MyDiscountPercentage" -DocumentType "invoice" -DunningLevel 0 -InputVatAmount "MyInputVatAmount" -InputVatDeductible $false -InputVatPercentage "MyInputVatPercentage" -IntroductionText "MyIntroductionText" -InvoiceType "Invoice" -IsCancelled $false -IsDraft $false -IsEuAcquisition $false -IsEuDelivery $false -IsIntraCommunityAcquisition $false -IsReverseCharge $false -IssueDate (Get-Date) -LedgerAccount "MyLedgerAccount" -LineItems  -Margin25a $false -Margin25aGross "MyMargin25aGross" -Margin25aPurchasePrice "MyMargin25aPurchasePrice" -Notes "MyNotes" -OrderNumber "MyOrderNumber" -OriginalPdfPath "MyOriginalPdfPath" -PaidAmount "MyPaidAmount" -PaymentDueDate (Get-Date) -PaymentStatus "unpaid" -PaymentTermsText "MyPaymentTermsText" -PrecedingSalesVoucherId "MyPrecedingSalesVoucherId" -PrecedingSalesVoucherType "order_confirmation" -ReceiptConfirmationAvailable $false -RelatedInvoiceId "MyRelatedInvoiceId" -RelationshipType "MyRelationshipType" -SenderSnapshot  -SentAt (Get-Date) -ServicePeriodEnd (Get-Date) -ServicePeriodStart (Get-Date) -Status "Draft" -Subtotal "MySubtotal" -SupplierId "MySupplierId" -TaxExemptionReason "MyTaxExemptionReason" -TotalAmount "MyTotalAmount" -TotalTax "MyTotalTax" -VatCountry "ABW" -VatSpecialCase "MyVatSpecialCase" # InvoiceCreate | 

try {
    $Result = New-Invoice -InvoiceCreate $InvoiceCreate
} catch {
    Write-Host ("Exception occurred when calling New-Invoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **InvoiceCreate** | [**InvoiceCreate**](InvoiceCreate.md)|  | 

### Return type

[**Invoice**](Invoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteInvoice"></a>
# **Invoke-DeleteInvoice**
> void Invoke-DeleteInvoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 

try {
    $Result = Invoke-DeleteInvoice -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteInvoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DownloadInvoicePdf"></a>
# **Invoke-DownloadInvoicePdf**
> void Invoke-DownloadInvoicePdf<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 

try {
    $Result = Invoke-DownloadInvoicePdf -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-DownloadInvoicePdf: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Invoice"></a>
# **Get-Invoice**
> Invoice Get-Invoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 

try {
    $Result = Get-Invoice -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-Invoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**Invoice**](Invoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-InvoicePdfUrl"></a>
# **Get-InvoicePdfUrl**
> InvoicePdfUrlResponse Get-InvoicePdfUrl<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 

try {
    $Result = Get-InvoicePdfUrl -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Get-InvoicePdfUrl: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**InvoicePdfUrlResponse**](InvoicePdfUrlResponse.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Invoices"></a>
# **Get-Invoices**
> Invoice[] Get-Invoices<br>
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
    $Result = Get-Invoices -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-Invoices: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**Invoice[]**](Invoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="ConvertTo-voiceRestore"></a>
# **ConvertTo-voiceRestore**
> Invoice ConvertTo-voiceRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 

try {
    $Result = ConvertTo-voiceRestore -Id $Id
} catch {
    Write-Host ("Exception occurred when calling ConvertTo-voiceRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**Invoice**](Invoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Invoice"></a>
# **Update-Invoice**
> Invoice Update-Invoice<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 
$Body =  # AnyType | 

try {
    $Result = Update-Invoice -Id $Id -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Update-Invoice: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **Body** | **AnyType**|  | 

### Return type

[**Invoice**](Invoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

