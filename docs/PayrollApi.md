# PSOpenAPITools.PSOpenAPITools\Api.PayrollApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-PayrollApprove**](PayrollApi.md#Invoke-PayrollApprove) | **POST** /api/v1/payroll/{id}/approve | 
[**Invoke-PayrollAutopay**](PayrollApi.md#Invoke-PayrollAutopay) | **POST** /api/v1/payroll/{id}/autopay | 
[**Invoke-PayrollCalculate**](PayrollApi.md#Invoke-PayrollCalculate) | **POST** /api/v1/payroll/{id}/calculate | 
[**Invoke-PayrollCreate**](PayrollApi.md#Invoke-PayrollCreate) | **POST** /api/v1/payroll | 
[**Invoke-PayrollDelete**](PayrollApi.md#Invoke-PayrollDelete) | **DELETE** /api/v1/payroll/{id} | 
[**Invoke-PayrollElsterExport**](PayrollApi.md#Invoke-PayrollElsterExport) | **POST** /api/v1/payroll/{id}/elster-export | 
[**Invoke-PayrollEmail**](PayrollApi.md#Invoke-PayrollEmail) | **POST** /api/v1/payroll/{id}/email | 
[**Invoke-PayrollEntryPdf**](PayrollApi.md#Invoke-PayrollEntryPdf) | **GET** /api/v1/payroll/{id}/entries/{entry_id}/pdf | 
[**Invoke-PayrollGet**](PayrollApi.md#Invoke-PayrollGet) | **GET** /api/v1/payroll/{id} | 
[**Invoke-PayrollList**](PayrollApi.md#Invoke-PayrollList) | **GET** /api/v1/payroll | 
[**Invoke-PayrollPay**](PayrollApi.md#Invoke-PayrollPay) | **POST** /api/v1/payroll/{id}/pay | 
[**Invoke-PayrollPdf**](PayrollApi.md#Invoke-PayrollPdf) | **GET** /api/v1/payroll/{id}/pdf | 
[**Invoke-PayrollSummary**](PayrollApi.md#Invoke-PayrollSummary) | **GET** /api/v1/payroll/summary/{year} | 
[**Invoke-PayrollSvMeldungen**](PayrollApi.md#Invoke-PayrollSvMeldungen) | **POST** /api/v1/payroll/{id}/sv-meldungen | 


<a id="Invoke-PayrollApprove"></a>
# **Invoke-PayrollApprove**
> PayrollRunApi Invoke-PayrollApprove<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PayrollApprove -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollApprove: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollAutopay"></a>
# **Invoke-PayrollAutopay**
> AnyType Invoke-PayrollAutopay<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Body] <System.Nullable[AnyType]><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 
$Body =  # AnyType |  (optional)

try {
    $Result = Invoke-PayrollAutopay -Id $Id -Body $Body
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollAutopay: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **Body** | **AnyType**|  | [optional] 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollCalculate"></a>
# **Invoke-PayrollCalculate**
> PayrollRunApi Invoke-PayrollCalculate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PayrollCalculate -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollCalculate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollCreate"></a>
# **Invoke-PayrollCreate**
> PayrollRunApi Invoke-PayrollCreate<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PayrollCreatePayload] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$ExtraPayment = Initialize-ExtraPayment -Amount "MyAmount" -EmployeeId "MyEmployeeId" -Reason "MyReason"
$PayrollCreatePayload = Initialize-PayrollCreatePayload -EmployeeIds "MyEmployeeIds" -ExtraPayments $ExtraPayment -Month 0 -Year 0 # PayrollCreatePayload | 

try {
    $Result = Invoke-PayrollCreate -PayrollCreatePayload $PayrollCreatePayload
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollCreate: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **PayrollCreatePayload** | [**PayrollCreatePayload**](PayrollCreatePayload.md)|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollDelete"></a>
# **Invoke-PayrollDelete**
> void Invoke-PayrollDelete<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PayrollDelete -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollDelete: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollElsterExport"></a>
# **Invoke-PayrollElsterExport**
> void Invoke-PayrollElsterExport<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PayrollElsterExport -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollElsterExport: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollEmail"></a>
# **Invoke-PayrollEmail**
> AnyType Invoke-PayrollEmail<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 

try {
    $Result = Invoke-PayrollEmail -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollEmail: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollEntryPdf"></a>
# **Invoke-PayrollEntryPdf**
> void Invoke-PayrollEntryPdf<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-EntryId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 
$EntryId = "MyEntryId" # String | 

try {
    $Result = Invoke-PayrollEntryPdf -Id $Id -EntryId $EntryId
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollEntryPdf: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **EntryId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/pdf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollGet"></a>
# **Invoke-PayrollGet**
> PayrollRunApi Invoke-PayrollGet<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PayrollGet -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollGet: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollList"></a>
# **Invoke-PayrollList**
> PayrollRunApi[] Invoke-PayrollList<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <System.Nullable[Int32]><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Status] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 |  (optional)
$Status = "MyStatus" # String |  (optional)

try {
    $Result = Invoke-PayrollList -Year $Year -Status $Status
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollList: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | [optional] 
 **Status** | **String**|  | [optional] 

### Return type

[**PayrollRunApi[]**](PayrollRunApi.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollPay"></a>
# **Invoke-PayrollPay**
> PayrollRunApi Invoke-PayrollPay<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-PayrollPayPayload] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 
$PayrollPayPayload = Initialize-PayrollPayPayload -PaymentDate (Get-Date) # PayrollPayPayload | 

try {
    $Result = Invoke-PayrollPay -Id $Id -PayrollPayPayload $PayrollPayPayload
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollPay: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 
 **PayrollPayPayload** | [**PayrollPayPayload**](PayrollPayPayload.md)|  | 

### Return type

[**PayrollRunApi**](PayrollRunApi.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollPdf"></a>
# **Invoke-PayrollPdf**
> void Invoke-PayrollPdf<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "MyId" # String | 

try {
    $Result = Invoke-PayrollPdf -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollPdf: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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
 - **Accept**: application/pdf

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollSummary"></a>
# **Invoke-PayrollSummary**
> YearlyPayrollSummary Invoke-PayrollSummary<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Year] <Int32><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Year = 56 # Int32 | 

try {
    $Result = Invoke-PayrollSummary -Year $Year
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollSummary: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Year** | **Int32**|  | 

### Return type

[**YearlyPayrollSummary**](YearlyPayrollSummary.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-PayrollSvMeldungen"></a>
# **Invoke-PayrollSvMeldungen**
> AnyType Invoke-PayrollSvMeldungen<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Id] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Id = "38400000-8cf0-11bd-b23e-10b96e4ef00d" # String | 

try {
    $Result = Invoke-PayrollSvMeldungen -Id $Id
} catch {
    Write-Host ("Exception occurred when calling Invoke-PayrollSvMeldungen: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Id** | **String**|  | 

### Return type

[**AnyType**](AnyType.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

