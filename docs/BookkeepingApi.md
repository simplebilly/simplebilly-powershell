# PSOpenAPITools.PSOpenAPITools\Api.BookkeepingApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-PaymentApi**](BookkeepingApi.md#New-PaymentApi) | **POST** /api/v1/payments/allocate | Allocate a payment to an invoice
[**Invoke-BwaReportApi**](BookkeepingApi.md#Invoke-BwaReportApi) | **GET** /api/v1/bookkeeping/bwa | Get BWA (Betriebswirtschaftliche Auswertung) report
[**Invoke-ElsterStatusApi**](BookkeepingApi.md#Invoke-ElsterStatusApi) | **GET** /api/v1/bookkeeping/elster/status | 
[**Invoke-ElsterValidateApi**](BookkeepingApi.md#Invoke-ElsterValidateApi) | **POST** /api/v1/bookkeeping/ustva/elster-validate | 
[**Invoke-ElsterXmlApi**](BookkeepingApi.md#Invoke-ElsterXmlApi) | **GET** /api/v1/bookkeeping/ustva/elster-xml | 
[**Get-Cashflow**](BookkeepingApi.md#Get-Cashflow) | **GET** /api/v1/bookkeeping/cashflow | GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
[**Get-Liquidity**](BookkeepingApi.md#Get-Liquidity) | **GET** /api/v1/bookkeeping/liquidity | GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
[**Get-OpenInvoicesApi**](BookkeepingApi.md#Get-OpenInvoicesApi) | **GET** /api/v1/payments/open-invoices/{customer_id} | Get open invoices for a customer
[**Get-Verfahrensdokumentation**](BookkeepingApi.md#Get-Verfahrensdokumentation) | **GET** /api/v1/bookkeeping/verfahrensdokumentation | GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
[**Invoke-RunDunningApi**](BookkeepingApi.md#Invoke-RunDunningApi) | **POST** /api/v1/bookkeeping/dunning | 


<a id="New-PaymentApi"></a>
# **New-PaymentApi**
> void New-PaymentApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-AllocatePaymentRequest] <PSCustomObject><br>

Allocate a payment to an invoice

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$AllocatePaymentRequest = Initialize-AllocatePaymentRequest -Amount 0 -InvoiceId "MyInvoiceId" -PaymentId "MyPaymentId" # AllocatePaymentRequest | 

# Allocate a payment to an invoice
try {
    $Result = New-PaymentApi -AllocatePaymentRequest $AllocatePaymentRequest
} catch {
    Write-Host ("Exception occurred when calling New-PaymentApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **AllocatePaymentRequest** | [**AllocatePaymentRequest**](AllocatePaymentRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-BwaReportApi"></a>
# **Invoke-BwaReportApi**
> BWAReport Invoke-BwaReportApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Month] <System.Nullable[Int32]><br>

Get BWA (Betriebswirtschaftliche Auswertung) report

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 |  (optional)
$Month = 56 # Int32 |  (optional)

# Get BWA (Betriebswirtschaftliche Auswertung) report
try {
    $Result = Invoke-BwaReportApi -Year $Year -Month $Month
} catch {
    Write-Host ("Exception occurred when calling Invoke-BwaReportApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | [optional] 
 **Month** | **Int32**|  | [optional] 

### Return type

[**BWAReport**](BWAReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ElsterStatusApi"></a>
# **Invoke-ElsterStatusApi**
> ElsterStatus Invoke-ElsterStatusApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-ElsterStatusApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-ElsterStatusApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ElsterStatus**](ElsterStatus.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ElsterValidateApi"></a>
# **Invoke-ElsterValidateApi**
> void Invoke-ElsterValidateApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Zeitraum] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Zeitraum = "MyZeitraum" # String | 

try {
    $Result = Invoke-ElsterValidateApi -Zeitraum $Zeitraum
} catch {
    Write-Host ("Exception occurred when calling Invoke-ElsterValidateApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Zeitraum** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-ElsterXmlApi"></a>
# **Invoke-ElsterXmlApi**
> void Invoke-ElsterXmlApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Zeitraum] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Zeitraum = "MyZeitraum" # String | 

try {
    $Result = Invoke-ElsterXmlApi -Zeitraum $Zeitraum
} catch {
    Write-Host ("Exception occurred when calling Invoke-ElsterXmlApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Zeitraum** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Cashflow"></a>
# **Get-Cashflow**
> CashflowReport Get-Cashflow<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Month] <System.Nullable[Int32]><br>

GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 |  (optional)
$Month = 56 # Int32 |  (optional)

# GET /api/v1/bookkeeping/cashflow Returns operating, investing, and financing cashflow for the given period.
try {
    $Result = Get-Cashflow -Year $Year -Month $Month
} catch {
    Write-Host ("Exception occurred when calling Get-Cashflow: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | [optional] 
 **Month** | **Int32**|  | [optional] 

### Return type

[**CashflowReport**](CashflowReport.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Liquidity"></a>
# **Get-Liquidity**
> LiquidityPosition Get-Liquidity<br>

GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# GET /api/v1/bookkeeping/liquidity Returns current liquidity position with ratios.
try {
    $Result = Get-Liquidity
} catch {
    Write-Host ("Exception occurred when calling Get-Liquidity: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**LiquidityPosition**](LiquidityPosition.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-OpenInvoicesApi"></a>
# **Get-OpenInvoicesApi**
> Invoice[] Get-OpenInvoicesApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>

Get open invoices for a customer

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerId = "MyCustomerId" # String | 

# Get open invoices for a customer
try {
    $Result = Get-OpenInvoicesApi -CustomerId $CustomerId
} catch {
    Write-Host ("Exception occurred when calling Get-OpenInvoicesApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerId** | **String**|  | 

### Return type

[**Invoice[]**](Invoice.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Verfahrensdokumentation"></a>
# **Get-Verfahrensdokumentation**
> Verfahrensdokumentation Get-Verfahrensdokumentation<br>

GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.

### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


# GET /api/v1/bookkeeping/verfahrensdokumentation Returns the complete compliance catalog of all documented modules.
try {
    $Result = Get-Verfahrensdokumentation
} catch {
    Write-Host ("Exception occurred when calling Get-Verfahrensdokumentation: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**Verfahrensdokumentation**](Verfahrensdokumentation.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-RunDunningApi"></a>
# **Invoke-RunDunningApi**
> DunningResult Invoke-RunDunningApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-RunDunningApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-RunDunningApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**DunningResult**](DunningResult.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

