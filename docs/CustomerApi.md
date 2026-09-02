# PSOpenAPITools.PSOpenAPITools\Api.CustomerApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**New-Customer**](CustomerApi.md#New-Customer) | **POST** /api/v1/customers | 
[**Invoke-CustomerRestore**](CustomerApi.md#Invoke-CustomerRestore) | **POST** /api/v1/customers/{customer_id}/restore | 
[**Invoke-DeleteCustomer**](CustomerApi.md#Invoke-DeleteCustomer) | **DELETE** /api/v1/customers/{customer_id} | 
[**Get-Customer**](CustomerApi.md#Get-Customer) | **GET** /api/v1/customers/{customer_id} | 
[**Get-Customers**](CustomerApi.md#Get-Customers) | **GET** /api/v1/customers/ | 
[**Update-Customer**](CustomerApi.md#Update-Customer) | **PUT** /api/v1/customers/{customer_id} | 


<a id="New-Customer"></a>
# **New-Customer**
> Customer New-Customer<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerCreate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerCreate = Initialize-CustomerCreate -Address  -ContactPerson "MyContactPerson" -Email "MyEmail" -ExternalOrderNumber "MyExternalOrderNumber" -Name "MyName" -PaymentGracePeriodDays 0 -Phone "MyPhone" -VatId "MyVatId" # CustomerCreate | 

try {
    $Result = New-Customer -CustomerCreate $CustomerCreate
} catch {
    Write-Host ("Exception occurred when calling New-Customer: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerCreate** | [**CustomerCreate**](CustomerCreate.md)|  | 

### Return type

[**Customer**](Customer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-CustomerRestore"></a>
# **Invoke-CustomerRestore**
> Customer Invoke-CustomerRestore<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerId = "MyCustomerId" # String | 

try {
    $Result = Invoke-CustomerRestore -CustomerId $CustomerId
} catch {
    Write-Host ("Exception occurred when calling Invoke-CustomerRestore: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerId** | **String**|  | 

### Return type

[**Customer**](Customer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-DeleteCustomer"></a>
# **Invoke-DeleteCustomer**
> void Invoke-DeleteCustomer<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerId = "MyCustomerId" # String | 

try {
    $Result = Invoke-DeleteCustomer -CustomerId $CustomerId
} catch {
    Write-Host ("Exception occurred when calling Invoke-DeleteCustomer: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerId** | **String**|  | 

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Customer"></a>
# **Get-Customer**
> Customer Get-Customer<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerId = "MyCustomerId" # String | 

try {
    $Result = Get-Customer -CustomerId $CustomerId
} catch {
    Write-Host ("Exception occurred when calling Get-Customer: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerId** | **String**|  | 

### Return type

[**Customer**](Customer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Get-Customers"></a>
# **Get-Customers**
> Customer[] Get-Customers<br>
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
    $Result = Get-Customers -Page $Page -PageSize $PageSize -Search $Search -IncludeDeleted $IncludeDeleted
} catch {
    Write-Host ("Exception occurred when calling Get-Customers: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
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

[**Customer[]**](Customer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Update-Customer"></a>
# **Update-Customer**
> Customer Update-Customer<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerId] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CustomerUpdate] <PSCustomObject><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$CustomerId = "MyCustomerId" # String | 
$CustomerUpdate = Initialize-CustomerUpdate -Address  -ContactPerson "MyContactPerson" -Email "MyEmail" -ExternalOrderNumber "MyExternalOrderNumber" -Name "MyName" -PaymentGracePeriodDays 0 -Phone "MyPhone" -VatId "MyVatId" # CustomerUpdate | 

try {
    $Result = Update-Customer -CustomerId $CustomerId -CustomerUpdate $CustomerUpdate
} catch {
    Write-Host ("Exception occurred when calling Update-Customer: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **CustomerId** | **String**|  | 
 **CustomerUpdate** | [**CustomerUpdate**](CustomerUpdate.md)|  | 

### Return type

[**Customer**](Customer.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

