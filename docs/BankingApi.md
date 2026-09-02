# PSOpenAPITools.PSOpenAPITools\Api.BankingApi

All URIs are relative to *https://demo.simplebilly.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**Invoke-BankLookupApi**](BankingApi.md#Invoke-BankLookupApi) | **GET** /api/v1/bookkeeping/banking/lookup | 
[**Invoke-BankTransactionsApi**](BankingApi.md#Invoke-BankTransactionsApi) | **GET** /api/v1/bookkeeping/banking/transactions | 
[**Invoke-HebesatzLookupApi**](BankingApi.md#Invoke-HebesatzLookupApi) | **GET** /api/v1/bookkeeping/hebesatz | 


<a id="Invoke-BankLookupApi"></a>
# **Invoke-BankLookupApi**
> BankLookup Invoke-BankLookupApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Iban] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Iban = "MyIban" # String | 

try {
    $Result = Invoke-BankLookupApi -Iban $Iban
} catch {
    Write-Host ("Exception occurred when calling Invoke-BankLookupApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Iban** | **String**|  | 

### Return type

[**BankLookup**](BankLookup.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-BankTransactionsApi"></a>
# **Invoke-BankTransactionsApi**
> void Invoke-BankTransactionsApi<br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration


try {
    $Result = Invoke-BankTransactionsApi
} catch {
    Write-Host ("Exception occurred when calling Invoke-BankTransactionsApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

<a id="Invoke-HebesatzLookupApi"></a>
# **Invoke-HebesatzLookupApi**
> HebesatzLookup[] Invoke-HebesatzLookupApi<br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Gemeindeschluessel] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Plz] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Name] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-Stichtag] <String><br>
> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[-CountryCode] <String><br>



### Example
```powershell
# general setting of the PowerShell module, e.g. base URL, authentication, etc
$Configuration = Get-Configuration

$Gemeindeschluessel = "MyGemeindeschluessel" # String |  (optional)
$Plz = "MyPlz" # String |  (optional)
$Name = "MyName" # String |  (optional)
$Stichtag = "MyStichtag" # String | Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from <= date <= valid_to. (optional)
$CountryCode = "MyCountryCode" # String |  (optional)

try {
    $Result = Invoke-HebesatzLookupApi -Gemeindeschluessel $Gemeindeschluessel -Plz $Plz -Name $Name -Stichtag $Stichtag -CountryCode $CountryCode
} catch {
    Write-Host ("Exception occurred when calling Invoke-HebesatzLookupApi: {0}" -f ($_.ErrorDetails | ConvertFrom-Json))
    Write-Host ("Response headers: {0}" -f ($_.Exception.Response.Headers | ConvertTo-Json))
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **Gemeindeschluessel** | **String**|  | [optional] 
 **Plz** | **String**|  | [optional] 
 **Name** | **String**|  | [optional] 
 **Stichtag** | **String**| Stichtag for validity (YYYY-MM-DD); defaults to today. Picks row where valid_from &lt;&#x3D; date &lt;&#x3D; valid_to. | [optional] 
 **CountryCode** | **String**|  | [optional] 

### Return type

[**HebesatzLookup[]**](HebesatzLookup.md) (PSCustomObject)

### Authorization

[bearer_token](../README.md#bearer_token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

